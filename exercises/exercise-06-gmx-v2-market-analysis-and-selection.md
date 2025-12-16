# Exercise 6: GMX V2 Market Analysis and Selection

⏰ Time Investment: 45-60 minutes  
🎯 Goal: Learn to analyze GM pools and select optimal markets for trading and LP provision

📚 Required Reading Integration  
📖 Primary: Lesson 6: GMX V2 - Oracle-Based Liquidity Pools  
📖 Supporting: Lesson 3: Architecture Types and Market Structure

## 🔍 Phase 1: Pool Analysis (20 minutes)

### Exercise 1: Standard vs. Synthetic Market Identification

**Analyze These Markets**:

| Market | Backing Assets | Type | Risk Level |
|--------|----------------|------|------------|
| ETH/USD | ETH + USDC | _______ | _______ |
| BTC/USD | BTC + USDC | _______ | _______ |
| DOGE/USD | ETH + USDC | _______ | _______ |
| SOL/USD | SOL + USDC | _______ | _______ |

**Question**: Why are synthetic markets riskier?
- Your answer: _________________________________

### Exercise 2: Pool Health Assessment

**Select a GM Pool** (e.g., GM-ETH-USDC):

**Pool Metrics**:
- Total TVL: $_______
- Current OI: $_______
- Long/Short Ratio: _______% / _______%
- Utilization: _______%

**Health Indicators**:
- [ ] OI is balanced (40-60% each side)
- [ ] Utilization is healthy (50-70%)
- [ ] TVL is sufficient for your size
- [ ] Pool is standard (not synthetic)

**Assessment**: Healthy / Moderate Risk / High Risk
- Reasoning: _________________________________

### Exercise 3: GM Token Valuation

**Current GM Token Price**: $_______

**Components**:
- Asset Value: $_______
- Pending PnL (trader losses = positive): $_______
- Accrued Fees: $_______

**Question**: If traders have $1M unrealized profits, what happens to GM token value?
- Your answer: _________________________________

## 📊 Phase 2: Fee Structure Analysis (15 minutes)

### Exercise 4: Trading Fee Calculation

**Scenario**: Open $10,000 Long ETH position

**Pool State**:
- Current OI: 70% Long, 30% Short
- Your trade: Adds to Long side

**Calculate**:
- Base trading fee: _______% (0.05% or 0.07%?)
- Fee amount: $_______
- Reasoning: _________________________________

### Exercise 5: Price Impact Fee Estimation

**Pool Imbalance**:
- Before trade: 70% Long, 30% Short
- Your trade: $10,000 Long
- After trade: 75% Long, 25% Short



![GLP Investment Analysis Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_06/ex06_02_glp_investment_analysis_template.png)



![GMX V2 Market Comparison Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_06/ex06_01_gmx_v2_market_comparison_template.png)

**Price Impact Fee**:
- Estimated fee: _______%
- Fee amount: $_______

**Question**: How can you reduce price impact fees?
- Your answer: _________________________________

### Exercise 6: Funding Rate Analysis

**Current Funding Rate**: _______% per hour

**Calculate**:
- Daily funding: _______%
- Annualized: _______%
- Cost for $10,000 position (24h): $_______

**OI Imbalance Impact**:
- If OI becomes 80% Long, funding rate will: Increase / Decrease
- Reasoning: _________________________________

## 💰 Phase 3: LP Strategy Development (15 minutes)

### Exercise 7: Pool Selection for LP

**Your LP Goals**: [Fill in]
- Risk tolerance: Conservative / Moderate / Aggressive
- Capital: $_______
- Time horizon: Short-term / Long-term

**Pool Comparison**:

| Pool | TVL | OI Balance | Utilization | APY | Your Choice |
|------|-----|------------|-------------|-----|-------------|
| GM-ETH-USDC | $_______ | _______% | _______% | _______% | Yes/No |
| GM-BTC-USDC | $_______ | _______% | _______% | _______% | Yes/No |
| GM-SOL-USDC | $_______ | _______% | _______% | _______% | Yes/No |

**Selected Pool**: _______
**Reasoning**: _________________________________

### Exercise 8: Delta-Neutral Strategy Design

**Scenario**: Deposit $10,000 into GM-ETH-USDC pool

**Pool Composition**: 50% ETH, 50% USDC
**Your Exposure**: $5,000 ETH delta

**Hedge Strategy**:
- [ ] Short ETH on CEX: $5,000
- [ ] Short ETH on another DEX: $5,000
- [ ] Other: _______

**Expected Outcome**:
- If ETH rises 10%: GM gains $_______, Hedge loses $_______, Net: $_______
- If ETH drops 10%: GM loses $_______, Hedge gains $_______, Net: $_______

**Net Yield**: Trading fees + Funding - Hedge costs = _______%

## 🎯 Phase 4: Trader vs. LP Perspective (10 minutes)

### Exercise 9: Trader Analysis

**For Trading**:
- Best pools: _______
- Why: _________________________________

**Fee Optimization**:
- [ ] Trade when OI is balanced (lower fees)
- [ ] Avoid high price impact (smaller trades)
- [ ] Monitor funding rates
- [ ] Use contrarian trades (rebalancing)

### Exercise 10: LP Analysis

**For LP Provision**:
- Best pools: _______
- Why: _________________________________

**Risk Management**:
- [ ] Avoid pools with extreme OI imbalance
- [ ] Monitor GM token value
- [ ] Consider delta-neutral hedging
- [ ] Diversify across multiple pools

## ✅ Self-Assessment

Rate your GMX V2 understanding (1 = Beginner, 5 = Expert):

- [ ] Pool analysis and selection: __/5
- [ ] Fee structure understanding: __/5
- [ ] LP strategy development: __/5
- [ ] Trader optimization: __/5
- [ ] Risk assessment: __/5

**Areas needing more review**: _________________________________

## 🎯 Next Steps

If you scored < 4 on any topic:
- Review Lesson 6 on that topic
- Explore GMX V2 analytics dashboard
- Practice with small positions
- Study GM token mechanics

If all topics ≥ 4:
- Proceed to Exercise 7 (Drift Analysis)
- You're ready to use GMX V2 effectively!

---

[← Back to Summary](../SUMMARY.md) | [Next: Lesson 7 →](../lessons/lesson-07-drift-protocol-solanas-hybrid-architecture.md)

