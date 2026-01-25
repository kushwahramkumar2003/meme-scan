# MemeScan Verifier Documentation

> Comprehensive research and design documentation for the MemeScan on-chain trust score protocol.

---

## 📚 Documentation Index

| # | Document | Description |
|---|----------|-------------|
| 1 | [Problem Statement](./01-PROBLEM-STATEMENT.md) | The memecoin rug-pull crisis, market statistics, and why this problem needs solving |
| 2 | [Theory & Scoring](./02-THEORY-SCORING-EXPLAINED.md) | How the scoring algorithm works, Gini coefficient explained, worked examples |
| 3 | [Architecture](./03-ARCHITECTURE.md) | System design, data flows, on-chain program structure, API design |
| 4 | [Solution Overview](./04-SOLUTION-OVERVIEW.md) | Complete solution summary, user journeys, competitive advantage |

---

## 🎯 Quick Summary

### The Problem
- **98.6%** of Pump.fun tokens are rug pulls or scams
- **$6 billion+** lost in Q1 2025 to memecoin scams
- Traders have no reliable way to verify token safety before buying

### Our Solution
**MemeScan Verifier** - An on-chain oracle that computes cryptographically verified trust scores (0-100) for Solana memecoins.

### How It Works
```
1. User submits token address
2. Oracle fetches holder data from Solana
3. Algorithm calculates trust score based on:
   - Token distribution (Gini coefficient) - 40%
   - Top 10 holder concentration - 20%
   - Mint/Freeze authority status - 30%
   - Wallet age diversity - 10%
4. Score stored ON-CHAIN (verifiable by anyone)
5. User gets instant risk assessment
```

### Key Differentiators
| Feature | MemeScan | Competitors |
|---------|----------|-------------|
| Speed | <30 seconds | 5-15 minutes |
| Verification | On-chain ✅ | Off-chain ❌ |
| Composable | Yes ✅ | No ❌ |
| Gini Analysis | Yes ✅ | No ❌ |

---

## 📖 Reading Order (Recommended)

1. **Start with Problem Statement** → Understand why this matters
2. **Read Theory & Scoring** → Understand HOW we score tokens
3. **Review Architecture** → Understand the technical design
4. **Finish with Solution Overview** → See the complete picture

---

## 🔑 Key Concepts

| Term | Definition |
|------|------------|
| **Trust Score** | 0-100 rating indicating token safety |
| **Gini Coefficient** | Mathematical measure of distribution inequality |
| **PDA** | Program Derived Address - on-chain storage |
| **Oracle** | Service that computes and submits scores |
| **Rug Pull** | Scam where developers abandon project after collecting funds |

---

## 📊 Score Interpretation

| Score Range | Risk Level | Action |
|-------------|------------|--------|
| 80-100 | ✅ Low | Safe to buy |
| 60-79 | ⚠️ Medium | Caution |
| 40-59 | 🟠 High | Small position only |
| 0-39 | ❌ Extreme | Avoid |

---

## 🏗️ Project Structure

```
MemeScan/
├── docs/                    # 📚 This documentation
│   ├── README.md
│   ├── 01-PROBLEM-STATEMENT.md
│   ├── 02-THEORY-SCORING-EXPLAINED.md
│   ├── 03-ARCHITECTURE.md
│   └── 04-SOLUTION-OVERVIEW.md
├── programs/                # ⛓️ Solana/Anchor program (to be created)
├── oracle/                  # ⚡ Oracle backend (to be created)
├── api/                     # 🔌 API server (to be created)
├── app/                     # 🌐 Web dashboard (to be created)
└── bot/                     # 🤖 Telegram bot (to be created)
```

---

## 📈 Implementation Roadmap

- **Phase 1 (Weeks 1-4):** MVP on Devnet
- **Phase 2 (Weeks 5-8):** Beta launch on Mainnet
- **Phase 3 (Weeks 9-12):** Public launch
- **Phase 4 (Months 4-12):** Scale and partnerships

---

*For the original design document, see the user request that initiated this project.*
