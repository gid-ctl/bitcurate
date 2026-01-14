# BitCurate: Bitcoin-Native Content Discovery & Reward Protocol

> A decentralized content curation protocol built on Stacks Layer 2, leveraging Bitcoin's security for community-driven content discovery and creator rewards.

[![Stacks](https://img.shields.io/badge/Built%20on-Stacks-5546FF?style=flat-square)](https://stacks.co)
[![Bitcoin](https://img.shields.io/badge/Secured%20by-Bitcoin-FF9500?style=flat-square)](https://bitcoin.org)
[![Clarity](https://img.shields.io/badge/Language-Clarity-blue?style=flat-square)](https://clarity-lang.org)

## 🌟 Overview

BitCurate transforms content discovery through a trustless ecosystem where quality content rises via collective intelligence. The protocol incentivizes both curators and creators through a sophisticated reputation system backed by Bitcoin's immutable security model.

### Key Features

- **🔐 Bitcoin-Secured Curation**: All content submissions and votes secured by Bitcoin's proof-of-work
- **💰 Creator Economics**: Direct STX payments to content creators with transparent reward tracking
- **⭐ Reputation Mining**: Users earn credibility scores through accurate content evaluation
- **🛡️ Spam Resistance**: Economic barriers and community moderation prevent low-quality submissions
- **🏛️ Decentralized Governance**: Community-driven content categories and moderation decisions
- **📜 Immutable Audit Trail**: All curation activities permanently recorded on Bitcoin blockchain
- **⚡ Layer 2 Efficiency**: Fast, low-cost transactions while maintaining Bitcoin's security guarantees

## 🏗️ System Architecture

### High-Level Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                        BitCurate Protocol                       │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐ │
│  │   Content       │  │   Reputation    │  │   Economic      │ │
│  │   Curation      │  │   System        │  │   Layer         │ │
│  │                 │  │                 │  │                 │ │
│  │ • Submit Items  │  │ • Vote Weight   │  │ • STX Rewards   │ │
│  │ • Community     │  │ • Credibility   │  │ • Submission    │ │
│  │   Voting        │  │   Tracking      │  │   Fees          │ │
│  │ • Flagging      │  │ • Sybil         │  │ • Creator       │ │
│  │   System        │  │   Resistance    │  │   Payments      │ │
│  └─────────────────┘  └─────────────────┘  └─────────────────┘ │
│                                                                 │
├─────────────────────────────────────────────────────────────────┤
│                    Stacks Layer 2 Blockchain                   │
├─────────────────────────────────────────────────────────────────┤
│                    Bitcoin Security Layer                      │
└─────────────────────────────────────────────────────────────────┘
```

### Contract Architecture

```
BitCurate Smart Contract
├── State Management
│   ├── Content Registry (curated-items)
│   ├── Voting History (participant-appraisals)
│   └── Reputation System (participant-credibility)
├── Core Functions
│   ├── Content Submission (contribute-item)
│   ├── Quality Evaluation (appraise-item)
│   ├── Creator Rewards (reward-originator)
│   └── Content Moderation (flag-item)
├── Query Interface
│   ├── Content Retrieval (retrieve-item-details)
│   ├── Reputation Queries (retrieve-participant-credibility)
│   └── Top Content (retrieve-top-items)
└── Administrative Layer
    ├── Fee Management (adjust-submission-charge)
    ├── Content Moderation (expunge-item)
    └── Category Management (introduce-topic)
```

## 🔄 Data Flow

### Content Submission Flow

```
User Intent → Fee Payment → Content Validation → Registry Update → Event Emission
     │              │              │                   │              │
     │              │              │                   │              │
     ▼              ▼              ▼                   ▼              ▼
Submit Content → Pay STX Fee → Check Parameters → Store on Chain → Notify Network
```

### Reputation & Voting Flow

```
User Votes → Reputation Check → Update Scores → Influence Ranking → Reward Distribution
     │              │               │               │                    │
     │              │               │               │                    │
     ▼              ▼               ▼               ▼                    ▼
Cast Vote → Weight by Rep → Update Both → Content Rises → Creators Earn
```

### Economic Flow

```
Community Rewards Creators → STX Transfer → Reputation Update → Quality Incentive
        │                        │              │                     │
        │                        │              │                     │
        ▼                        ▼              ▼                     ▼
   Direct Payment → On-Chain Transfer → Rep Boost → Better Content
```

## 🚀 Getting Started

### Prerequisites

- Stacks wallet (Hiro, Xverse, or Leather)
- STX tokens for transactions
- Clarity development environment (optional, for development)

### Deployment

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-org/bitcurate
   cd bitcurate
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Deploy to testnet**

   ```bash
   clarinet deploy --testnet
   ```

4. **Deploy to mainnet**

   ```bash
   clarinet deploy --mainnet
   ```

### Usage Examples

#### Submit Content

```clarity
(contract-call? .bitcurate contribute-item 
  "Revolutionary Bitcoin L2 Solution" 
  "https://example.com/article" 
  "Technology")
```

#### Vote on Content

```clarity
(contract-call? .bitcurate appraise-item u1 1) ;; Upvote
(contract-call? .bitcurate appraise-item u1 -1) ;; Downvote
```

#### Reward Creator

```clarity
(contract-call? .bitcurate reward-originator u1 u1000000) ;; 1 STX reward
```

## 📊 Protocol Economics

### Fee Structure

- **Submission Fee**: 0.00001 STX (configurable)
- **Voting**: Free (gas only)
- **Rewards**: User-determined amounts
- **Administration**: Protocol owner only

### Reputation System

- **Positive Votes**: +1 reputation
- **Negative Votes**: -1 reputation
- **Quality Threshold**: Items need ≥0 net votes to appear in top lists
- **Sybil Resistance**: Reputation weighting prevents spam

### Economic Incentives

- **Content Creators**: Direct STX rewards from community
- **Quality Curators**: Reputation building for future influence
- **Community**: High-quality content discovery
- **Protocol**: Sustainable fee collection

## 🛡️ Security Features

### Bitcoin Security Inheritance

- **Immutable Records**: All transactions secured by Bitcoin's proof-of-work
- **Decentralized Consensus**: No single point of failure
- **Transparent Operations**: All actions publicly verifiable

### Anti-Spam Measures

- **Economic Barriers**: Submission fees deter low-quality content
- **Community Moderation**: Flagging system for inappropriate content
- **Reputation Weighting**: Established users have more influence
- **Administrative Oversight**: Protocol owner can remove violating content

## 📈 Roadmap

### Phase 1: Core Protocol ✅

- [x] Basic content submission and voting
- [x] Reputation system implementation
- [x] Creator reward mechanism
- [x] Community moderation tools

### Phase 2: Enhanced Features 🔄

- [ ] Advanced reputation algorithms
- [ ] Multi-token reward support
- [ ] Category-specific governance
- [ ] Mobile-friendly interface

### Phase 3: Ecosystem Growth 📋

- [ ] Third-party integrations
- [ ] Analytics dashboard
- [ ] API for developers
- [ ] Cross-chain compatibility

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

### Code Style

- Follow Clarity best practices
- Use descriptive function names
- Include comprehensive comments
- Maintain consistent formatting

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
