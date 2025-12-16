# Exercise 7: Drift Market Creation and Strategy Analysis

⏰ Time Investment: 45-60 minutes  
🎯 Goal: Understand Drift's hybrid architecture and cross-margin system for advanced strategies

📚 Required Reading Integration  
📖 Primary: Lesson 7: Drift Protocol - Solana's Hybrid Architecture  
📖 Supporting: Lesson 3: Architecture Types and Market Structure

## 🔍 Phase 1: Liquidity Trifecta Understanding (15 minutes)



![Cross-Margin Strategy Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_07/ex07_02_cross_margin_strategy_template.png)



![Drift Market Analysis Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_07/ex07_01_drift_market_analysis_template.png)

### Exercise 1: Execution Flow Analysis

**Scenario**: Market order to buy 100 SOL-PERP

**Trace the Execution**:
1. Order submitted → Enters _______ (Layer 1)
2. Duration: _______ seconds
3. If filled: Best price from _______
4. If not filled: Moves to _______ (Layer 2)
5. If still not filled: Routes to _______ (Layer 3)

**Question**: Why does this protect LPs?
- Your answer: _________________________________

### Exercise 2: JIT Auction Mechanics

**Auction Parameters**:
- Duration: _______ seconds
- Starting price: $_______
- AMM price: $_______

**Maker Competition**:
- Maker 1 bid: $_______
- Maker 2 bid: $_______
- Winner: Maker _______
- Price improvement: $_______

**Question**: How does JIT internalize MEV?
- Your answer: _________________________________

### Exercise 3: DLOB vs. DAMM Comparison

**Fill in the table**:

| Feature | DLOB | DAMM |
|---------|------|------|
| Order Types | _______ | _______ |
| Price Precision | _______ | _______ |
| Liquidity Source | _______ | _______ |
| Execution Speed | _______ | _______ |
| Primary Use | _______ | _______ |

## 💰 Phase 2: Cross-Margin System (20 minutes)

### Exercise 4: Unified Margin Calculation

**Portfolio Composition**:
- USDC: $5,000 (weight: 1.0x)
- SOL: $3,000 (weight: 0.8x)
- ETH: $2,000 (weight: 0.8x)

**Calculate**:
- Total Portfolio Value: $_______
- Weighted Buying Power: $_______
- Available for Trading: $_______

### Exercise 5: Cross-Margin Hedging Strategy

**Setup**:
- Long BTC-PERP: $10,000
- Short ETH-PERP: $10,000
- Collateral: $5,000 USDC

**Scenario 1**: BTC +5%, ETH -3%
- BTC P&L: $_______
- ETH P&L: $_______
- Net P&L: $_______
- Portfolio Health: Improved / Worsened

**Scenario 2**: BTC -5%, ETH +3%
- BTC P&L: $_______
- ETH P&L: $_______
- Net P&L: $_______
- Portfolio Health: Improved / Worsened

**Question**: How does cross-margin help in this scenario?
- Your answer: _________________________________

### Exercise 6: Asset Weighting Impact

**Collateral Options**:

| Asset | Amount | Weight | Buying Power |
|-------|--------|--------|--------------|
| USDC | $10,000 | 1.0x | $_______ |
| SOL | $10,000 | 0.8x | $_______ |
| BONK | $10,000 | 0.5x | $_______ |

**Question**: Which collateral is most capital efficient?
- Your answer: _______
- Why: _________________________________

## 🎯 Phase 3: Advanced Order Types (15 minutes)

### Exercise 7: Oracle-Pegged Orders

**Use Case**: Market maker wants to provide liquidity without constant updates

**Order Setup**:
- Type: Oracle-Pegged
- Offset: Oracle - $0.50
- Current Oracle: $150
- Your Order Price: $_______

**If Oracle moves to $155**:
- Your Order Price: $_______
- Benefit: _______

**Question**: When would you use oracle-pegged orders?
- Your answer: _________________________________

### Exercise 8: Stop Loss Strategy

**Position**: Long SOL-PERP at $150

**Stop Loss Options**:
- Stop-Market: $145
- Stop-Limit: $145 (limit: $144.50)

**Scenario**: Flash crash to $140, then recovery to $150

**Stop-Market Result**: Filled at $_______
**Stop-Limit Result**: Filled at $_______ / Not Filled

**Question**: Which is better for volatile markets?
- Your answer: _______
- Why: _________________________________

## 🔬 Phase 4: Strategy Design (15 minutes)

### Exercise 9: Multi-Product Strategy

**Design a cross-margin strategy using**:
- Spot trading
- Perpetual swaps
- Lending (if available)

**Your Strategy**:
1. _________________________________
2. _________________________________
3. _________________________________

**Capital Efficiency**:
- Total Capital: $_______
- Positions: $_______
- Utilization: _______%

**Question**: How does cross-margin improve capital efficiency?
- Your answer: _________________________________

### Exercise 10: JIT Participation Strategy

**For Market Makers**:

**Setup Requirements**:
- [ ] Keeper bot running
- [ ] CEX price feed access
- [ ] Capital for fills
- [ ] Risk management system

**Expected Benefits**:
- Access to flow: _______
- Rebates/fees: _______%
- Price improvement opportunities: _______

**Question**: What infrastructure do you need to participate in JIT?
- Your answer: _________________________________

## ✅ Self-Assessment

Rate your Drift proficiency (1 = Beginner, 5 = Expert):

- [ ] Liquidity Trifecta understanding: __/5
- [ ] Cross-margin calculations: __/5
- [ ] Advanced order types: __/5
- [ ] Strategy design: __/5
- [ ] Risk management: __/5

**Areas needing more practice**: _________________________________

## 🎯 Next Steps

If you scored < 4 on any topic:
- Review Lesson 7 on that topic
- Explore Drift documentation
- Practice on Drift testnet (if available)
- Study cross-margin examples

If all topics ≥ 4:
- Proceed to Exercise 8 (Multi-Protocol Comparison)
- You're ready for advanced Drift strategies!

---

[← Back to Summary](../SUMMARY.md) | [Next: Lesson 8 →](../lessons/lesson-08-alternative-chain-protocols.md)

