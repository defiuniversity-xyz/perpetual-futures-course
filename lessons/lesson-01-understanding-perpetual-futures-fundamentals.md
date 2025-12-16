---
module: 1
lesson_number: 1
course: perpetual-futures
---


## 🎧 Lesson Podcast

{% embed url="https://storage.googleapis.com/perpetual-futures-media/lesson-01/audio/lesson1%20Mastering_DeFi_Perpetual_Futures_Trading_Risk.m4a" %}

## 🎬 Video Overview

{% embed url="https://storage.googleapis.com/perpetual-futures-media/lesson-01/video/Lesson1%20What_Are_Perpetual_Futures_.mp4" %}

# Lesson 1: Understanding Perpetual Futures Fundamentals

## 🎯 Core Concept: What is a Perpetual Future?

A perpetual future (or "perp") is a derivative contract that allows you to speculate on the price of an asset without an expiration date. Unlike traditional futures that settle on a specific date, perpetuals use a "funding rate" mechanism to keep the contract price aligned with the spot price indefinitely.

### Why Perpetual Futures Matter

Before perpetual futures, if you wanted to trade with leverage:
- You needed centralized exchanges (like Binance or BitMEX)
- You had to trust the exchange to hold your funds
- You were exposed to counterparty risk (as seen with FTX collapse)
- You had limited transparency into order matching

Perpetual futures on decentralized exchanges changed everything by:
- **Eliminating counterparty risk**: Self-custody of funds via smart contracts
- **Enabling permissionless trading**: Trade any asset, anywhere, anytime
- **Providing transparency**: All trades and prices are on-chain, verifiable
- **Offering leverage**: Amplify your position size with borrowed capital
- **Creating composability**: Integrate with other DeFi protocols

## 📚 The Evolution: From CEX to DEX Perpetuals

### Traditional Futures (CEX Model)

Traditional futures contracts have:
- **Expiration dates**: Contracts settle on a specific date (weekly, monthly, quarterly)
- **Physical or cash settlement**: You must close or roll positions before expiry
- **Centralized matching**: Orders matched by exchange servers
- **Custodial risk**: Exchange holds your funds

**Example**: A BTC futures contract expiring on December 31st must be closed or rolled to the next contract before that date.

### The Perpetual Revolution

Perpetual futures eliminate expiration dates by using a **funding rate mechanism**:
- **No expiry**: Hold positions indefinitely (as long as you maintain margin)
- **Funding payments**: Long and short positions pay/receive funding to keep price aligned
- **Continuous trading**: No need to roll contracts
- **On-chain settlement**: Smart contracts handle everything

**Key Innovation**: Instead of forcing price convergence through expiration, perpetuals use periodic funding payments to incentivize arbitrage and maintain price parity with spot markets.

## 🔄 Perpetual Futures vs Traditional Futures

| Feature | Traditional Futures | Perpetual Futures |
|---------|-------------------|-------------------|
| **Expiration** | Yes (weekly/monthly) | No (perpetual) |
| **Settlement** | Physical or cash on expiry | Continuous funding payments |
| **Price Convergence** | Forced at expiration | Maintained via funding rate |
| **Position Management** | Must roll before expiry | Hold indefinitely |
| **Complexity** | Lower (simple expiry) | Higher (funding mechanics) |


![Perpetual Futures vs Traditional Futures Comparison](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_01/pf01_01_perpetual_futures_vs_traditional_futures_comparison.png)


## 💰 Core Concepts: The Foundation

### Funding Rates

The funding rate is the mechanism that keeps perpetual prices aligned with spot prices:

- **Positive Funding**: When perpetual price > spot price
  - Long positions pay short positions
  - Discourages buying, encourages selling
  - Drives perpetual price down toward spot

- **Negative Funding**: When perpetual price < spot price
  - Short positions pay long positions
  - Discourages selling, encourages buying
  - Drives perpetual price up toward spot

**Frequency**: Most protocols calculate funding every hour or every 8 hours. High-performance chains like Hyperliquid calculate funding continuously or every block.

**Strategic Implication**: Funding rates can be significant. In strong trends, annualized funding rates can exceed 100%. Holding a position against the funding rate can erode capital, turning a profitable price move into a net loss.


![Funding Rate Mechanism Diagram](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_01/pf01_02_funding_rate_mechanism_diagram.png)


### Leverage

Leverage allows you to control a larger position with less capital:

- **Example**: With 10x leverage, $1,000 controls a $10,000 position
- **Amplification**: Profits and losses are multiplied by the leverage factor
- **Risk**: Higher leverage = higher liquidation risk

**Common Leverage Levels**:
- **Conservative**: 2-5x (recommended for beginners)
- **Moderate**: 5-10x (intermediate traders)
- **Aggressive**: 10-50x+ (advanced traders, high risk)

### Margin

Margin is the collateral you deposit to open and maintain a position:

- **Initial Margin**: Required to open a position (e.g., 10% for 10x leverage)
- **Maintenance Margin**: Minimum required to keep position open (e.g., 5%)
- **Margin Call**: When margin falls below maintenance, position is liquidated

**Example**: 
- Open 10x long BTC with $1,000 margin
- Position size: $10,000
- If BTC drops 10%, you lose $1,000 (100% of margin)
- If BTC drops 11%, you're liquidated (below maintenance margin)

## 🏗️ The Two Main Models: CLOB vs Oracle Pools

Understanding the architecture of a perpetual DEX is critical for risk assessment and strategy selection.

### Central Limit Order Book (CLOB)

**How It Works**:
- Market makers post buy/sell orders at specific prices
- Traders execute against the order book
- Price discovery happens through supply and demand

**Examples**: Hyperliquid, dYdX v4, EdgeX

**Benefits**:
- ✅ CEX-like experience (limit orders, stop losses)
- ✅ Transparent price discovery
- ✅ Deep liquidity (if market makers are active)

**Risks**:
- ❌ Slippage on large orders
- ❌ Front-running risk
- ❌ Requires active market makers

### Oracle-Based Shared Liquidity Pools

**How It Works**:
- Traders trade against a unified liquidity pool (not other traders)
- Prices come from external oracles (Chainlink, Pyth)
- Zero price impact (executed at oracle price)

**Examples**: GMX V2, Gains Network, Jupiter

**Benefits**:
- ✅ Zero slippage (executed at oracle price)
- ✅ Simple execution (swap-like interface)
- ✅ No need for market makers

**Risks**:
- ❌ Oracle latency arbitrage
- ❌ Pool insolvency risk
- ❌ Limited price discovery


![CLOB vs Oracle Pools Architecture Comparison](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_01/pf01_03_clob_vs_oracle_pools_architecture_comparison.png)


## 🎓 Beginner's Corner: Common Questions

**Q: What's the difference between perpetuals and spot trading?**
A: Spot trading means you own the asset. Perpetuals let you speculate on price without owning it, using leverage. You can go long (bet price goes up) or short (bet price goes down).

**Q: Why do I pay funding rates?**
A: Funding rates keep the perpetual price aligned with the spot price. If you're long and funding is positive, you pay shorts. This prevents the perpetual from trading too far above spot.

**Q: Can I lose more than I deposit?**
A: With isolated margin, your maximum loss is limited to your margin. With cross margin, one losing position can drain your entire account.

**Q: What happens if I get liquidated?**
A: The protocol automatically closes your position and seizes your remaining collateral. You lose your margin (minus liquidation fees).

**Q: Are perpetuals safer than CEX trading?**
A: Perpetuals on DEXs eliminate counterparty risk (no exchange can steal your funds), but you still face liquidation risk, smart contract risk, and oracle risk.

## ⚠️ Critical Differences from Spot Trading

| Feature | Spot Trading | Perpetual Futures |
|---------|-------------|-------------------|
| **Ownership** | You own the asset | You speculate on price |
| **Leverage** | 1x (no leverage) | 2x-100x+ available |
| **Funding Costs** | None | Periodic funding payments |
| **Liquidation Risk** | None (you own it) | High (if margin insufficient) |
| **Short Selling** | Difficult/expensive | Easy (just open short) |
| **Capital Efficiency** | Low (need full value) | High (need only margin) |


![Spot Trading vs Perpetual Futures Comparison](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_01/pf01_04_spot_trading_vs_perpetual_futures_comparison.png)


## 🔬 Advanced Deep-Dive: The Economics of Perpetuals

### Why Perpetuals Exist

Traditional futures require expiration because:
1. Physical delivery forces price convergence
2. Cash settlement forces price convergence
3. Without convergence, arbitrage opportunities emerge

Perpetuals solve this by:
1. Using funding rates to incentivize arbitrage
2. Making funding payments continuous (not just at expiry)
3. Allowing positions to exist indefinitely

### The Funding Rate Formula

Most protocols calculate funding as:

```
Funding Rate = (Perpetual Price - Spot Price) / Spot Price × Adjustment Factor
```

- **Positive**: Perp > Spot → Longs pay shorts
- **Negative**: Perp < Spot → Shorts pay longs

The adjustment factor varies by protocol and market conditions.

### Market Maker vs Trader Dynamics

In CLOB models:
- Market makers provide liquidity (earn spread)
- Traders pay spread + funding
- Competition tightens spreads

In Oracle pool models:
- LPs provide liquidity (earn fees)
- Traders pay fees + funding
- Pool absorbs all risk

## 📊 Real-World Example: Opening a Position

**Scenario**: You want to go long ETH at $2,500 with 5x leverage

1. **Deposit Margin**: $1,000 USDC
2. **Position Size**: $5,000 (5x leverage)
3. **Entry Price**: $2,500
4. **Liquidation Price**: ~$2,000 (depends on maintenance margin)

**If ETH goes to $3,000**:
- Profit: ($3,000 - $2,500) × 5 = $2,500
- ROI: 250% on your $1,000 margin

**If ETH goes to $2,000**:
- Loss: ($2,500 - $2,000) × 5 = $2,500
- But you only have $1,000 margin → **LIQUIDATED**

**Key Takeaway**: Leverage amplifies both profits and losses. A 20% price move against you with 5x leverage = 100% loss.

## 🔑 Key Takeaways

- Perpetual futures are derivative contracts without expiration dates
- Funding rates keep perpetual prices aligned with spot prices
- Leverage amplifies both profits and losses
- Two main architectures: CLOB (order book) and Oracle pools
- Margin requirements protect the protocol from insolvency
- Liquidation risk is real and can result in total loss

## 🚀 Next Steps

- Proceed to Lesson 2 to dive deeper into the mathematics of funding rates, margin, and liquidations
- Explore a perpetual DEX interface (Hyperliquid, GMX, or Drift) to see these concepts in action
- Start with small positions and low leverage to learn safely

