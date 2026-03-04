 💘 BitMatch — Tinder on Bitcoin

> Swipe right. Match. Mine $HEART. Built on BOB L2.

**BitMatch** is Tinder, but on Bitcoin. Swipe right, send a ❤️, and when it's mutual — boom, you both mine **$HEART** tokens on the spot. Your profile photo is a real Bitcoin Ordinal inscription, so your face literally lives on the blockchain. The more you match, the more you earn. Spend **$HEART** to boost your profile, send Super Hearts, or unlock features. It's the same addictive swipe loop you already know — except now every match has real Bitcoin value behind it.

**Swipe. Match. Mine. 🧡**

---

## How It Works

```
You swipe right on someone       →   +1 $HEART minted to you
They swipe right back            →   💘 MATCH — both of you get +10 $HEART
Boost your profile               →   spend 5 $HEART for 24h visibility
Send a Super Heart               →   spend 1 $HEART for priority notification
Ghost after a match              →   on-chain reputation takes a hit
```

---

## Stack

| Layer | Tech |
|-------|------|
| Profile photos | Bitcoin Ordinal Inscriptions (L1) |
| App logic | Solidity smart contracts on BOB L2 |
| Governance token | $HEART (OP-20) |
| Frontend | Next.js + Viem + Wagmi |
| Payments | Native BTC / Lightning Network |
| Testing | Hardhat + Chai |

---

## Smart Contracts

### `HeartToken.sol` — $HEART Token
- OP-20 token (ERC-20 compatible on BOB L2)
- Max supply: **100,000,000 $HEART**
- Minting controlled exclusively by `BitMatch.sol`
- Used for boosts, governance votes, and Super Hearts

### `BitMatch.sol` — Core App Logic
- Register profile with your Ordinal inscription ID
- `sendHeart(address)` — like someone, mint +1 $HEART
- Auto-detects mutual match → mints +10 $HEART to both
- `activateBoost()` — spend $HEART to boost visibility
- Full on-chain stats: hearts sent/received, match count, reputation

---

## $HEART Tokenomics

| Action | $HEART |
|--------|--------|
| Send a heart ❤️ | +1 |
| Mutual match 💘 | +10 (both users) |
| Activate boost 🚀 | -5 (24h) |
| Super Heart ⚡ | -1 |

---

## Setup

```bash
# Install dependencies
npm install

# Copy env vars
cp .env.example .env
# Add your PRIVATE_KEY to .env

# Compile
npm run compile

# Run tests
npm run test

# Deploy to BOB Testnet
npm run deploy:testnet
```

---

## BOB Testnet

| | |
|-|-|
| RPC | `https://testnet.rpc.gobob.xyz` |
| Chain ID | `111` |
| Explorer | https://testnet-explorer.gobob.xyz |
| Faucet | https://faucet.gobob.xyz |

---

## Project Structure

```
bitmatch/
├── contracts/
│   ├── HeartToken.sol      # $HEART OP-20 token
│   └── BitMatch.sol        # Swipe / match / boost logic
├── scripts/
│   └── deploy.ts           # Deploy to BOB
├── test/
│   └── BitMatch.test.ts    # Full test suite
└── frontend/               # Next.js swipe UI (coming soon)
```

---

## Roadmap

- [x] Smart contracts — $HEART token + match logic
- [x] Swipe UI — drag cards, heart animations, match modal
- [ ] Ordinals indexer — load real inscription images
- [ ] Lightning tips — send sats to profiles you like
- [ ] On-chain messaging — via XMTP
- [ ] Governance — vote with $HEART on Snapshot
- [ ] Match DAOs — couples with many matches can form a mini-DAO

---

## Built at BOB Hackathon

> *"Not your keys, not your matches."*
