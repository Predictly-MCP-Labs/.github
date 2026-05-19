# Predictly 

<img width="1710" height="930" alt="image" src="https://github.com/user-attachments/assets/2e7da370-ea66-4761-ae6e-a1204ff1b3e3" />


---

**Social-First Decentralized Prediction Markets - Built with $MOVE**

Unlock the power of collective intelligence through prediction markets with your friends and communities. The first social prediction platform on Movement Network that combines transparency, gamification, and zero-loss markets.

---

## 🎥 Live Demo

- 🔗 [Try Predictly App](https://predictly-movement.vercel.app) - Experience the platform
- 📚 [Read Documentation](https://predictly-labs.gitbook.io/predictly-labs-docs) - Complete technical docs
- 🔍 [View Contract](https://explorer.movementnetwork.xyz/account/0x9161980be9b78e96ddae98ceb289f6f4cda5e4af70667667ff9af8438a94e565/modules/run/market?network=bardock+testnet) - Explore on-chain

---

## 🎯 What is Predictly?

**Predictly** is a decentralized prediction market platform built on Movement Network where users can create and participate in prediction markets with friends and communities, staking MOVE tokens on YES/NO outcomes.

Unlike traditional prediction markets, Predictly is **social-first** - designed for friend groups and communities to make predictions together, compete on leaderboards, and earn rewards in a transparent, decentralized environment.

### Key Innovation

- **🎲 Full Degen Markets** - High risk, high reward prediction markets where winners take all
- **🛡️ Zero Loss Markets** - Protected markets using DeFi yield farming
- **👥 Private Groups** - Create exclusive prediction communities with invite codes
- **⚖️ Judge System** - Fair, transparent market resolution through trusted community judges
- **🎮 Gamification** - Leaderboards, badges, and competitive prediction tournaments

---

## 🔥 The Problem

Traditional prediction markets face critical challenges:

| Problem                     | Impact                                                      |
| --------------------------- | ----------------------------------------------------------- |
| **Lack of Transparency**    | Users cannot verify outcomes or trust centralized platforms |
| **High Barriers to Entry**  | Complex onboarding, KYC requirements, high minimum stakes   |
| **Limited Social Features** | No friend groups, communities, or social engagement         |
| **Platform Control**        | Centralized decision-making and opaque resolution processes |
| **No Principal Protection** | Users risk losing everything with no safety nets            |

### The Market Gap is Massive

Prediction markets have proven valuable for forecasting, but existing platforms are either:

- **Too Complex** - Designed for professional traders, not casual users
- **Too Centralized** - Single point of failure, trust required
- **Too Isolated** - No social features, no community engagement

### Impact

This prevents mainstream adoption and limits prediction markets to a small niche of sophisticated users, missing the opportunity to harness collective intelligence from broader communities.

---

## 💡 Our Solution

Predictly addresses these problems with a **decentralized, social-first approach**:

### 1. Transparent & Decentralized 🔗

| Traditional Markets | Predictly                              |
| ------------------- | -------------------------------------- |
| Centralized control | Smart contracts on Movement blockchain |
| Opaque resolution   | Transparent judge system               |
| Trust required      | Verifiable on-chain                    |
| Platform custody    | Non-custodial, user-controlled funds   |

### 2. Low Barriers to Entry 🚀

- **Wallet-based Auth** - No KYC, just connect your wallet
- **Free Market Creation** - Backend pays gas for initialization
- **Low Minimums** - Start with small amounts of MOVE
- **Simple YES/NO** - Easy to understand binary predictions

### 3. Social-First Design 👥

- **Private Groups** - Create prediction communities with friends
- **Invite Codes** - Control who joins your group
- **Leaderboards** - Compete and track performance
- **Judge System** - Fair community-driven resolution
- **Role Management** - Admin, Judge, Moderator, Member roles

### 4. Principal Protection 🛡️

- **Zero Loss Markets** - Your principal is always protected
- **Yield-based Rewards** - Winners earn from DeFi yield, not losses
- **Risk-Free Participation** - Perfect for risk-averse users

---

## ⚙️ How It Works

### User Flow: Creating & Participating in Markets

```
1. Connect Wallet (Nightly/Petra/Martian)
   ↓
2. Join or Create a Group
   - Get invite code from friends
   - Or create your own group
   ↓
3. Create a Prediction Market
   - Set question (e.g., "Will ETH hit $5000 by March?")
   - Choose deadline
   - Upload image
   - Backend initializes on-chain
   ↓
4. Place Your Vote
   - Choose YES or NO
   - Stake MOVE tokens
   - Transaction signed by wallet
   - Tokens locked in smart contract
   ↓
5. Wait for Resolution
   - Market closes at deadline
   - Judge reviews outcome
   - Resolution recorded on-chain
   ↓
6. Claim Rewards
   - Winners claim proportional share
   - Rewards distributed automatically
   - Leaderboard updated
```

### Market Resolution & Rewards

- **Judge Assignment** - Group admins assign trusted judges
- **Fair Resolution** - Judges resolve based on real-world outcomes
- **On-Chain Recording** - All resolutions are transparent and verifiable
- **Automatic Distribution** - Smart contracts handle reward calculations
- **Proportional Shares** - Winners earn based on their stake percentage

---

## 🏗️ Architecture

### System Overview

Predictly uses a **hybrid on-chain/off-chain architecture** to balance decentralization with user experience:

```
┌─────────────────────────────────────────────────────────────────┐
│                         FRONTEND                                 │
│                   (Next.js 16 + React 19)                        │
│                                                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐        │
│  │ Landing  │  │Dashboard │  │  Groups  │  │ Markets  │        │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘        │
│                                                                  │
│  ┌────────────────────────────────────────────────────┐         │
│  │         Movement SDK (Client-side)                 │         │
│  │       Direct blockchain interactions               │         │
│  └────────────────────────────────────────────────────┘         │
└───────────────┬─────────────────────────┬───────────────────────┘
                │                         │
    REST API    │                         │  Direct Blockchain TX
                │                         │
                ▼                         ▼
┌────────────────────────┐    ┌────────────────────────┐
│   BACKEND              │    │  MOVEMENT NETWORK      │
│   (Express.js)         │    │                        │
│                        │    │  ┌──────────────────┐  │
│  ┌──────────────────┐  │    │  │ Smart Contracts  │  │
│  │   API Routes     │  │    │  │  (Move Language) │  │
│  │                  │  │    │  │                  │  │
│  │  /api/groups     │  │    │  │  - Market Logic  │  │
│  │  /api/users      │  │    │  │  - Escrow        │  │
│  │  /api/markets    │  │    │  │  - Rewards       │  │
│  │  /api/upload     │  │    │  │  - Resolution    │  │
│  └──────────────────┘  │    │  └──────────────────┘  │
│                        │    │                        │
│  ┌──────────────────┐  │    │                        │
│  │    Services      │◄─┼────┼──  Events              │
│  │                  │  │    │                        │
│  │  - GroupService  │  │    └────────────────────────┘
│  │  - UserService   │  │
│  │  - MarketService │  │
│  │  - PinataService │  │
│  │  - EventIndexer  │  │
│  └──────────────────┘  │
│                        │
└───────┬────────────────┘
        │
        ▼
┌────────────────┐    ┌────────────────┐
│   PostgreSQL   │    │  Pinata (IPFS) │
│                │    │                │
│  - Users       │    │  - Images      │
│  - Groups      │    │  - Avatars     │
│  - Markets     │    │  - Icons       │
│  - Votes       │    │  - Metadata    │
│  - Leaderboard │    │                │
└────────────────┘    └────────────────┘
```

### Data Flow: Market Lifecycle

**Creating a Market:**

1. User fills form (Frontend)
2. POST /api/markets (Backend) - Validate, save to DB, upload to IPFS
3. Initialize on-chain (Frontend) - User signs transaction
4. Sync back (Backend) - Listen for MarketCreated event, update DB

**Voting on a Market:**

1. User selects YES/NO + amount (Frontend)
2. Direct blockchain call - place_vote(), user signs, tokens locked
3. Event indexer (Backend) - Detect VotePlaced event, update cache, leaderboard

---

## 🛠️ Technology Stack

### Frontend

| Technology        | Purpose                            |
| ----------------- | ---------------------------------- |
| **Next.js 16**    | React framework with App Router    |
| **React 19**      | UI components and state management |
| **TypeScript**    | Type-safe development              |
| **Tailwind CSS**  | Utility-first styling              |
| **Framer Motion** | Smooth animations                  |
| **Recharts**      | Data visualization                 |

### Backend

| Technology     | Purpose                |
| -------------- | ---------------------- |
| **Node.js**    | JavaScript runtime     |
| **Express.js** | REST API framework     |
| **TypeScript** | Type-safe backend code |
| **Prisma ORM** | Database management    |
| **PostgreSQL** | Relational database    |

### Blockchain

| Technology           | Purpose                         |
| -------------------- | ------------------------------- |
| **Movement Network** | Layer 2 blockchain (Move-based) |
| **Move Language**    | Smart contract development      |
| **Aptos SDK**        | Blockchain interactions         |

### Storage & Services

| Service           | Purpose                    |
| ----------------- | -------------------------- |
| **Pinata (IPFS)** | Decentralized file storage |
| **Vercel**        | Frontend hosting           |
| **Render**        | Backend hosting            |

### Supported Wallets

- **Nightly Wallet** - Primary wallet integration
- **Petra Wallet** - Aptos ecosystem wallet
- **Martian Wallet** - Multi-chain wallet support

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn
- PostgreSQL database
- Movement Network wallet (Nightly/Petra/Martian)
- MOVE tokens from [faucet](https://faucet.movementnetwork.xyz/)

### 1. Clone Repository

```bash
git clone https://github.com/Predictly-Labs/Predictly-Labs.git
cd Predictly-Labs
```

### 2. Smart Contracts Setup

```bash
cd contracts
aptos init --network testnet
aptos move compile
aptos move publish
```

### 3. Backend Setup

```bash
cd backend
npm install
cp .env.example .env
# Configure environment variables
npx prisma migrate dev
npm run dev
```

### 4. Frontend Setup

```bash
cd web
npm install
cp .env.example .env.local
# Configure environment variables
npm run dev
```

Visit `http://localhost:3000` to see the app running locally.

---

## 📍 Deployed Contracts (Movement Testnet)

| Property     | Value                                                                                                                                                                       |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Network**  | Movement Testnet (Bardock)                                                                                                                                                  |
| **Contract** | `0x9161980be9b78e96ddae98ceb289f6f4cda5e4af70667667ff9af8438a94e565`                                                                                                        |
| **Module**   | `predictly::market`                                                                                                                                                         |
| **RPC**      | `https://testnet.movementnetwork.xyz/v1`                                                                                                                                    |
| **Explorer** | [View Contract](https://explorer.movementnetwork.xyz/account/0x9161980be9b78e96ddae98ceb289f6f4cda5e4af70667667ff9af8438a94e565/transactions?network=bardock+testnet) |
| **Faucet**   | [Get MOVE Tokens](https://faucet.movementnetwork.xyz/)                                                                                                                      |

---

## 🔒 Security Features

### 1. Smart Contract Security

- **Move Language** - Resource-oriented, prevents common vulnerabilities
- **Formal Verification** - Mathematical proof of correctness
- **Access Control** - Role-based permissions
- **Reentrancy Guards** - Protection against attacks

### 2. Backend Security

- **JWT Authentication** - Secure API access
- **Rate Limiting** - Prevent abuse
- **Input Validation** - Sanitize all inputs
- **CORS** - Restrict cross-origin requests

### 3. Frontend Security

- **Wallet Signing** - All transactions signed by user
- **No Private Keys** - Never store or transmit keys
- **HTTPS Only** - Encrypted communication
- **CSP Headers** - Content Security Policy

---

## 🗺️ Roadmap

### Phase 1: Hackathon MVP (COMPLETED ✅)

- ✅ Prediction market core logic
- ✅ Group management system
- ✅ Wallet integration (Nightly, Petra, Martian)
- ✅ Judge-based resolution
- ✅ Deployed to Movement Testnet
- ✅ Zero Loss Markets with DeFi yield
- ✅ NFT-based roles and badges

### Phase 2: Launch (Q1 2025)

- 📋 Mobile app (PWA)
- 📋 Push notifications
- 📋 Mainnet deployment

### Phase 3: Growth (Q2 2025)

- Multi-outcome markets (beyond YES/NO)
- Group chat integration
- Tournament mode
- Referral rewards
- Advanced analytics

### Phase 4: Ecosystem (Q3-Q4 2025)

- API for third-party apps
- SDK for easy integration
- Automated market makers (AMM)
- DAO governance
- Protocol upgrades

---

## 👥 Team

Built with ❤️ by the Predictly Labs team for Movement M1 Hackathon.

**Tracks:**

- Best Consumer App built on Movement
- The People's Choice
- Best New Defi App or Defi built on top of existing Movement Protocols

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🔗 Links

- **Live App:** [predictly-movement.vercel.app](https://predictly-movement.vercel.app)
- **Documentation:** [predictly-labs.gitbook.io](https://predictly-labs.gitbook.io/predictly-labs-docs)
- **Backend API:** [backend-3ufs.onrender.com](https://backend-3ufs.onrender.com)
- **GitHub:** [github.com/Predictly-Labs](https://github.com/Predictly-Labs)
- **Gitbook:** [gitbook](https://predictly-labs.gitbook.io/predictly-labs-docs/introduction/overview)

---

## 📞 Support

For support and questions:

- 📖 [Documentation](https://predictly-labs.gitbook.io/predictly-labs-docs)
- 🐛 [GitHub Issues](https://github.com/Predictly-Labs/Predictly-Labs/issues)
- 💬 Community Discord (Coming Soon)

---

## ⭐ Star Us!

If you find Predictly useful, please consider giving us a star ⭐ on GitHub!

---

<div align="center">
  <p><strong>Predictly Labs</strong></p>
  <p><em>Where Prediction Markets Meet Social Communities</em></p>
  <p>Built with $MOVE on Movement Network 🚀</p>
</div>






