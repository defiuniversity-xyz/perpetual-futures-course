# Exercise 9: Funding Rate Arbitrage Framework

⏰ Time Investment: 60-75 minutes  
🎯 Goal: Design and analyze funding rate arbitrage strategies

📚 Required Reading Integration  
📖 Primary: Lesson 9: Funding Rate Arbitrage Strategies  
📖 Supporting: Lesson 2: The Mathematics of Perpetual Trading

## 🔍 Phase 1: Opportunity Identification (20 minutes)

### Exercise 1: Funding Rate Analysis

**Current Market Conditions**:

| Market | Spot Price | Perp Price | Basis | Funding Rate (per hour) | Annualized |
|--------|------------|------------|-------|-------------------------|------------|
| ETH | $2,500 | $2,550 | $_______ | 0.03% | _______% |
| BTC | $50,000 | $50,200 | $_______ | 0.015% | _______% |
| SOL | $150 | $152 | $_______ | 0.05% | _______% |

**Question**: Which market offers the best arbitrage opportunity?
- Your choice: _______
- Reasoning: _________________________________

### Exercise 2: Delta-Neutral Setup

**Scenario**: ETH funding rate is 0.05% per hour (very high)

**Your Capital**: $10,000

**Design Your Strategy**:
1. Spot position: Buy _______ ETH at $_______
2. Perp position: Short _______ ETH at $_______
3. Total capital used: $_______
4. Expected daily funding: $_______
5. Expected monthly return: $_______

**Delta Check**:
- Spot delta: +_______
- Perp delta: -_______
- Net delta: _______ (should be ~0)

**Question**: How will you maintain delta neutrality?
- Your answer: _________________________________

### Exercise 3: Risk Assessment

**For Your Arbitrage Strategy**:

**Risk Factors**:
- [ ] Funding rate flips negative
- [ ] Execution slippage
- [ ] Smart contract risk
- [ ] Delta drift
- [ ] Gas costs (if applicable)

**Mitigation Plan**:
1. _________________________________
2. _________________________________
3. _________________________________

**Maximum Acceptable Loss**: $_______
**Exit Conditions**: _________________________________


![Arbitrage Opportunity Scanner Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_09/ex09_01_arbitrage_opportunity_scanner_template.png)


## 📊 Phase 2: Strategy Design (20 minutes)

### Exercise 4: Cash and Carry Trade

**Setup**:
- Spot ETH: $2,500
- Perp ETH: $2,600
- Basis: $100 (4%)
- Funding: 0.1% per hour

**Your Strategy**:
1. Buy spot: _______ ETH at $_______
2. Short perp: _______ ETH at $_______
3. Initial profit (basis): $_______
4. Expected funding (7 days): $_______
5. Total expected profit: $_______

**Convergence Plan**:
- Target convergence: When perp = spot
- Expected time: _______ days
- Exit strategy: _________________________________

### Exercise 5: Cross-Protocol Arbitrage

**Opportunity**:
- Protocol A (GMX): Funding 0.02% per hour
- Protocol B (Hyperliquid): Funding 0.05% per hour
- Difference: 0.03% per hour

**Your Strategy**:
- Long on Protocol A: $_______ (paying 0.02%)
- Short on Protocol B: $_______ (receiving 0.05%)
- Net funding received: _______% per hour

**Calculate**:
- Daily net profit: $_______
- Monthly net profit: $_______
- Annualized return: _______%

**Challenges**:
- Bridge costs: $_______
- Monitoring complexity: _______
- Capital requirements: $_______

**Is it worth it?** Yes / No
- Reasoning: _________________________________


![Delta-Neutral Setup Calculator](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_09/ex09_02_delta_neutral_setup_calculator.png)


## 💡 Phase 3: Execution Planning (15 minutes)

### Exercise 6: Execution Sequence

**For Delta-Neutral Strategy**:

**Step-by-Step Plan**:
1. [ ] Check funding rate (acceptable?)
2. [ ] Calculate position sizes
3. [ ] Execute spot buy: _______
4. [ ] Execute perp short: _______
5. [ ] Verify delta neutrality
6. [ ] Set monitoring alerts
7. [ ] Plan exit conditions

**Timing Considerations**:
- Execute simultaneously? Yes / No
- If not, which first? _______
- Maximum time gap: _______ minutes

**Slippage Management**:
- Expected slippage: $_______
- Acceptable slippage: $_______
- Mitigation: _________________________________

### Exercise 7: Monitoring Plan

**Daily Checks**:
- [ ] Funding rate (has it changed?)
- [ ] Delta (still neutral?)
- [ ] Basis (converging?)
- [ ] P&L (on track?)

**Alert Thresholds**:
- Funding rate flips: [ ] Alert set
- Delta drifts >5%: [ ] Alert set
- Basis converges: [ ] Alert set

**Exit Triggers**:
1. _________________________________
2. _________________________________
3. _________________________________

## 📈 Phase 4: Performance Projection (15 minutes)

### Exercise 8: Return Calculation

**Your Arbitrage Setup**:
- Capital: $10,000
- Strategy: Delta-neutral funding capture
- Funding rate: 0.03% per hour
- Position size: $10,000 perp

**Calculate**:
- Hourly funding: $_______
- Daily funding: $_______
- Weekly funding: $_______
- Monthly funding: $_______

**After Costs**:
- Trading fees: $_______
- Gas costs: $_______
- Net monthly: $_______
- ROI: _______%



![Arbitrage Risk Assessment Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_09/ex09_03_arbitrage_risk_assessment_template.png)

### Exercise 9: Scenario Analysis

**Best Case**:
- Funding stays high: 0.03% per hour
- Hold for 30 days
- Net profit: $_______

**Worst Case**:
- Funding flips to -0.01% per hour
- Hold for 7 days before exit
- Net profit/loss: $_______

**Realistic Case**:
- Funding averages 0.02% per hour
- Hold for 14 days
- Net profit: $_______

**Question**: Is the risk/reward acceptable?
- Your answer: Yes / No
- Reasoning: _________________________________

## ✅ Self-Assessment

Rate your arbitrage strategy design (1 = Beginner, 5 = Expert):

- [ ] Opportunity identification: __/5
- [ ] Strategy design: __/5
- [ ] Risk assessment: __/5
- [ ] Execution planning: __/5
- [ ] Performance projection: __/5

**Areas needing more review**: _________________________________

## 🎯 Next Steps

If you scored < 4 on any topic:
- Review Lesson 9 on that topic
- Study delta-neutral strategies
- Practice with paper trading
- Start with very small positions

If all topics ≥ 4:
- Proceed to Exercise 10 (Risk Management)
- You're ready to implement arbitrage strategies!

---

[← Back to Summary](../SUMMARY.md) | [Next: Lesson 10 →](../lessons/lesson-10-risk-management-and-position-protection.md)

