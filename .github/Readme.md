# 🐸 $SLERF Token Protocol

![Slerf Banner](https://i.imgur.com/QglUVfb.jpg)

> *“Stake. Laugh. Earn. Repeat.”*  
> $SLERF is a loyalty-first meme token engineered for daily quests, referrals, and cross-platform on-chain engagement.

---

## 🧬 Token Overview

| Property        | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| **Token Name**  | SLERF Token                                                                 |
| **Symbol**      | `$SLERF`                                                                    |
| **Decimals**    | 18                                                                          |
| **Chain**       | Base Mainnet (Chain ID: 8453)                                               |
| **Contract**    | [`0x233df63325933fa3f2dac8e695cd84bb2f91ab07`](https://basescan.org/address/0x233df63325933fa3f2dac8e695cd84bb2f91ab07) |
| **Standard**    | ERC-20 (OpenZeppelin)                                                       |
| **Issuer**      | Boomchainlab                                                                |

---

## 📦 Project Structure
slerf/
├── contracts/            # Solidity smart contracts (ERC20)
├── backend/              # FastAPI quest + claim engine
├── slerf-ui/             # Next.js wallet-connected claim portal
├── telegram-bot/         # @Boombot Telegram bot integration
├── claim-engine/         # Loyalty scoring + task tracking
├── cli/                  # Minimal terminal claim interface (iSH, Termux)
├── quests/               # JSON-based dynamic quest registry
├── .env.template         # Example environment config
└── README.md             # This file

---

## 🔥 Key Features

- ✅ Verified ERC20 contract deployed on Base
- 🎯 Daily quests, streaks, and referrals
- 🧠 Loyalty-based reward tiers with streak bonuses
- 🤖 Telegram bot with @Boombot for direct submissions
- 🌐 Frontend wallet-based claim UI with on-chain sync
- 📊 Leaderboard, wallet insights, and airdrop mechanics

---

## 🌐 Live Resources

| Component      | URL                                      |
|----------------|------------------------------------------|
| Claim UI       | https://token.boomchainlab.com           |
| Telegram Bot   | [@Boombot](https://t.me/Boombot)         |
| API            | https://api.boomchainlab.com/slerf       |
| Contract Scan  | [View on BaseScan](https://basescan.org/address/0x233df63325933fa3f2dac8e695cd84bb2f91ab07) |

---

## 🛠 Quickstart

### 1. Clone & Setup

```bash
git clone https://github.com/Boomchainlab/slerf.git
cd slerf
cp .env.template .env

2. Configure .env
BASE_RPC_URL=https://mainnet.base.org
SLERF_CONTRACT_ADDRESS=0x233df63325933fa3f2dac8e695cd84bb2f91ab07
DATABASE_URL=postgresql://...
TELEGRAM_BOT_TOKEN=...
NEXT_PUBLIC_CHAIN_ID=8453
NEXT_PUBLIC_SLERC_ADDRESS=0x233df63325933fa3f2dac8e695cd84bb2f91ab07

3. Run Backend
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

4. Run Frontend
cd slerf-ui
npm install
npm run dev

🤖 Submit a Quest (via CLI or Bot)
curl -X POST https://api.boomchainlab.com/slerf/submit \
  -H "Authorization: Bearer <signed_jwt>" \
  -d '{"wallet": "0xYourWallet", "task": "daily_login"}'

Or interact directly with @Boombot.

⸻

📈 Loyalty Engine

Each wallet’s score increases by completing:
	•	✅ Daily quests
	•	🔁 Consecutive logins
	•	👥 Verified referrals
	•	🎯 Telegram task flows

Top scorers are rewarded weekly with extra $SLERF, special NFTs, and leaderboard trophies.


🧪 Dev/Test
# Contract (Hardhat)
cd contracts && npm install && npx hardhat test

# Backend (FastAPI)
cd backend && pytest

# Frontend (Next.js)
cd slerf-ui && npm run dev

🔐 Security Model
	•	🔒 Signature validation for each quest
	•	🚫 Rate-limited submissions
	•	🧱 Token contract uses OpenZeppelin secure standards
	•	✅ CI/CD with GitHub Actions + test suite enforcement

⸻

📬 Community & Contact
	•	🌐 Twitter: @BoomchainLabs
	•	🧪 Telegram Bot: @Boombot
	•	💌 Email: support@boomchainlab.com

⸻

🧾 License

MIT © 2025 Boomchainlab.
Built for frog lovers, trivia champs, and degens who grind.

⸻

Ready to Slerf?
Join the leaderboard, claim your $SLERF, and let the streaks begin.
