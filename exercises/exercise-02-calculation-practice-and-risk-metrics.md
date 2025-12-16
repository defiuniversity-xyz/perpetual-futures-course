# Exercise 2: Calculation Practice and Risk Metrics

⏰ Time Investment: 45-60 minutes  
🎯 Goal: Master the mathematical calculations needed for safe perpetual trading

📚 Required Reading Integration  
📖 Primary: Lesson 2: The Mathematics of Perpetual Trading  
📖 Supporting: Lesson 1: Understanding Perpetual Futures Fundamentals

## 🔢 Phase 1: Funding Rate Calculations (15 minutes)



![Risk Metrics Summary Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_02/ex02_03_risk_metrics_summary_template.png)



![P&L Calculation Worksheet](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_02/ex02_02_pl_calculation_worksheet.png)



![Liquidation Price Calculator Worksheet](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_02/ex02_01_liquidation_price_calculator_worksheet.png)

### Exercise 1: Basic Funding Payment

**Scenario**: Long ETH perpetual position
- Position Size: $5,000
- Funding Rate: 0.01% per hour
- Holding Period: 12 hours

**Calculate**:
- Hourly payment: $_______
- Total payment (12 hours): $_______
- Annualized rate: _______%

### Exercise 2: Funding Cost Comparison

Compare funding costs across different rates:

| Funding Rate | Hourly | Daily (24h) | Weekly | Annualized |
|--------------|--------|-------------|--------|------------|
| 0.005% | $_______ | $_______ | $_______ | _______% |
| 0.01% | $_______ | $_______ | $_______ | _______% |
| 0.02% | $_______ | $_______ | $_______ | _______% |

**Position**: $10,000 notional size

**Question**: Which funding rate would make a trade unprofitable if price only moves 1% in your favor over 7 days?
- Your answer: _________________________________

### Exercise 3: Break-Even Analysis

**Setup**:
- Position Size: $8,000
- Trading Fees: 0.05% ($4)
- Funding Rate: 0.015% per hour
- Holding Period: 48 hours

**Calculate**:
- Total fees: $_______
- Total funding: $_______
- Total costs: $_______
- Break-even price movement: _______%

**Interpretation**: You need at least _______% price movement just to break even.

## 📊 Phase 2: Margin and Leverage Calculations (15 minutes)

### Exercise 4: Position Sizing

**Scenario**: You have $2,000 available for trading

**Calculate position size for each leverage**:

| Leverage | Position Size | Initial Margin Required |
|----------|---------------|-------------------------|
| 2x | $_______ | $_______ |
| 5x | $_______ | $_______ |
| 10x | $_______ | $_______ |

**Question**: If you want to risk only $500, what leverage should you use for a $2,000 position?
- Your answer: _______

### Exercise 5: Liquidation Price Calculations

**Scenario**: Long ETH position
- Entry Price: $2,500
- Margin: $1,000
- Leverage: 10x
- Maintenance Margin: 0.5%

**Calculate**:
- Position Size: $_______
- Liquidation Price: $_______
- Safety Buffer: _______%

**Scenario**: Short ETH position
- Entry Price: $2,500
- Margin: $1,000
- Leverage: 10x
- Maintenance Margin: 0.5%

**Calculate**:
- Position Size: $_______
- Liquidation Price: $_______
- Safety Buffer: _______%

### Exercise 6: Margin Ratio Analysis

**Current Position**:
- Position Size: $10,000
- Current Margin: $1,500
- Entry Price: $2,500
- Current Price: $2,400

**Calculate**:
- Current Margin Ratio: _______%
- Unrealized P&L: $_______
- Remaining Margin: $_______
- New Margin Ratio: _______%
- Distance to Liquidation: _______%

## ⚠️ Phase 3: Risk Assessment (15 minutes)

### Exercise 7: Liquidation Risk Analysis

**Position Details**:
- Long BTC at $50,000
- Margin: $5,000
- Leverage: 10x
- Maintenance Margin: 0.5%

**Calculate**:
- Position Size: $_______
- Liquidation Price: $_______
- Maximum Drawdown Before Liquidation: _______%

**Risk Scenarios**:

| Price Movement | Unrealized P&L | Remaining Margin | Margin Ratio | Status |
|----------------|----------------|------------------|--------------|--------|
| -5% | $_______ | $_______ | _______% | _______ |
| -8% | $_______ | $_______ | _______% | _______ |
| -9% | $_______ | $_______ | _______% | _______ |
| -10% | $_______ | $_______ | _______% | _______ |

### Exercise 8: Funding Rate Impact

**Scenario**: Holding long position during high funding period

**Setup**:
- Position Size: $20,000
- Funding Rate: 0.02% per hour (very high)
- Holding Period: 30 days

**Calculate**:
- Daily funding cost: $_______
- 30-day funding cost: $_______
- Annualized rate: _______%

**Question**: If ETH only moves 2% in your favor over 30 days, what is your net P&L?
- Price gain: $_______
- Funding cost: $_______
- Net P&L: $_______
- ROI: _______%

**Interpretation**: Is this trade profitable? (Yes / No)
- Reasoning: _________________________________

## 💰 Phase 4: Profit and Loss Calculations (15 minutes)

### Exercise 9: Complete P&L Analysis

**Long Position**:
- Entry: $2,500
- Exit: $2,600
- Position Size: $10,000 (5x leverage on $2,000 margin)
- Trading Fees: 0.05% (entry + exit = $10)
- Funding: 0.01% per hour for 48 hours

**Calculate**:
- Price gain: $_______
- Trading fees: $_______
- Funding costs: $_______
- Net P&L: $_______
- ROI on margin: _______%

### Exercise 10: Short Position P&L

**Short Position**:
- Entry: $2,500
- Exit: $2,400
- Position Size: $8,000 (4x leverage on $2,000 margin)
- Trading Fees: 0.05% (entry + exit = $8)
- Funding: -0.005% per hour (you receive) for 72 hours

**Calculate**:
- Price gain: $_______
- Trading fees: $_______
- Funding received: $_______
- Net P&L: $_______
- ROI on margin: _______%

### Exercise 11: Break-Even Price

**Setup**:
- Long ETH at $2,500
- Position Size: $10,000
- Margin: $2,000
- Trading Fees: 0.05% ($10 total)
- Funding: 0.01% per hour
- Target Holding: 7 days

**Calculate**:
- Total funding (7 days): $_______
- Total costs: $_______
- Break-even price: $_______
- Break-even price movement: _______%

**Question**: If you exit at $2,550, what is your net profit?
- Your calculation: _________________________________
- Net profit: $_______

## 📈 Phase 5: Position Management Scenarios (15 minutes)

### Exercise 12: Adding Margin

**Current Position**:
- Entry: $2,500
- Current Price: $2,450
- Position Size: $10,000
- Current Margin: $1,000
- Leverage: 10x
- Liquidation Price: $2,250

**You add $500 margin**:

**Calculate**:
- New Total Margin: $_______
- New Position Size: $_______ (unchanged)
- New Leverage: _______x
- New Liquidation Price: $_______
- New Safety Buffer: _______%

**Question**: How much did the safety buffer improve?
- Improvement: _______%

### Exercise 13: Partial Close

**Current Position**:
- Entry: $2,500
- Current Price: $2,600
- Position Size: $10,000
- Margin: $2,000
- Unrealized P&L: +$400

**You close 50% of position**:

**Calculate**:
- Amount closed: $_______
- Realized P&L: $_______
- Remaining Position Size: $_______
- Remaining Margin: $_______
- Remaining Unrealized P&L: $_______

## ✅ Self-Assessment

Rate your calculation skills (1 = Need more practice, 5 = Fully confident):

- [ ] Funding rate calculations: __/5
- [ ] Liquidation price calculations: __/5
- [ ] Position sizing: __/5
- [ ] P&L calculations: __/5
- [ ] Risk metrics: __/5

**Areas needing more practice**: _________________________________

## 🎯 Next Steps

If you struggled with any calculations:
- Review Lesson 2 formulas
- Practice with different scenarios
- Use a spreadsheet to verify answers
- Re-calculate until confident

If all calculations correct:
- Proceed to Exercise 3 (Architecture Analysis)
- You're ready for practical trading!

---

[← Back to Summary](../SUMMARY.md) | [Next: Lesson 3 →](../lessons/lesson-03-architecture-types-and-market-structure.md)

