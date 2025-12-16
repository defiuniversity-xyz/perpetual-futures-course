# Exercise 4: First Position Setup and Management

⏰ Time Investment: 45-60 minutes  
🎯 Goal: Create a complete plan for your first perpetual position with proper risk management

📚 Required Reading Integration  
📖 Primary: Lesson 4: Your First Perpetual Position  
📖 Supporting: Lesson 2: The Mathematics of Perpetual Trading, Lesson 3: Architecture Types

## 📋 Phase 1: Pre-Trade Planning (15 minutes)

### Exercise 1: Position Planning Worksheet

**Fill out this worksheet before opening any position**:

**Protocol Selection**:
- Chosen Protocol: _______
- Architecture Type: _______
- Why this protocol: _________________________________

**Market Selection**:
- Trading Pair: _______
- Current Spot Price: $_______
- Current Perpetual Price: $_______
- Funding Rate: _______% per hour
- Annualized Funding: _______%

**Position Configuration**:
- Direction: Long / Short
- Available Capital: $_______
- Risk Per Trade: _______% (recommended: 1-5%)
- Margin to Use: $_______
- Leverage: _______x
- Position Size: $_______

**Risk Parameters**:
- Entry Price: $_______
- Liquidation Price: $_______
- Safety Buffer: _______%
- Stop Loss: $_______
- Take Profit: $_______

### Exercise 2: Pre-Trade Checklist

**Complete this checklist before executing**:

- [ ] Funding rate checked and acceptable (< 0.05% per hour)
- [ ] Open interest checked (healthy and growing)
- [ ] Liquidation price calculated
- [ ] Safety buffer verified (20-30% minimum)
- [ ] Stop loss set
- [ ] Position size appropriate (1-5% of capital)
- [ ] Leverage conservative (3x-5x for first trade)
- [ ] Margin mode: Isolated (not cross)
- [ ] Network configured correctly
- [ ] Gas fees accounted for

**Any unchecked items?** List them and address before trading:
- _________________________________

## 📊 Phase 2: Position Setup Calculations (15 minutes)

### Exercise 3: Complete Position Math

**Your Plan**:
- Protocol: GMX V2
- Market: ETH/USD
- Direction: Long
- Available Capital: $10,000
- Risk Per Trade: 2%

**Calculate**:
- Maximum Risk: $_______
- Margin to Use: $_______
- Leverage: 5x
- Position Size: $_______
- Entry Price: $2,500 (current)
- Liquidation Price: $_______
- Safety Buffer: _______%

**Funding Analysis**:
- Current Funding Rate: 0.01% per hour
- Daily Funding Cost: $_______
- Weekly Funding Cost: $_______

**Break-Even Analysis**:
- Trading Fees (0.05%): $_______
- Weekly Funding: $_______
- Total Costs: $_______
- Break-Even Price Movement: _______%

### Exercise 4: Risk Scenario Planning

**Plan for different outcomes**:

| Price Movement | Unrealized P&L | Funding Cost (7 days) | Net P&L | Action Plan |
|----------------|----------------|----------------------|---------|-------------|
| +5% | $_______ | $_______ | $_______ | _______ |
| +2% | $_______ | $_______ | $_______ | _______ |
| 0% | $_______ | $_______ | $_______ | _______ |
| -2% | $_______ | $_______ | $_______ | _______ |
| -5% | $_______ | $_______ | $_______ | _______ |
| -10% (liquidation) | $_______ | $_______ | $_______ | _______ |

**Question**: At what price would you add margin? Why?
- Price: $_______
- Reasoning: _________________________________

## 💡 Phase 3: Execution Plan (10 minutes)

### Exercise 5: Step-by-Step Execution

**Write out your exact execution steps**:

1. **Wallet Setup**:
   - Wallet: _______
   - Network: _______
   - Status: [ ] Connected

2. **Deposit**:
   - Amount: $_______
   - Asset: _______
   - Status: [ ] Deposited

3. **Market Analysis**:
   - Funding Rate: _______% (acceptable? Yes/No)
   - Open Interest: $_______ (healthy? Yes/No)
   - Current Price: $_______

4. **Order Configuration**:
   - Type: Market / Limit
   - Price: $_______
   - Size: $_______
   - Leverage: _______x
   - Margin Mode: Isolated / Cross

5. **Risk Controls**:
   - Stop Loss: $_______
   - Take Profit: $_______

6. **Execution**:
   - [ ] Review all parameters
   - [ ] Execute order
   - [ ] Confirm transaction
   - [ ] Verify position opened

### Exercise 6: Monitoring Plan

**Create your monitoring schedule**:

**Immediate (First Hour)**:
- Check: [ ] Position opened correctly
- Check: [ ] Liquidation price correct
- Check: [ ] Funding rate hasn't changed

**Daily Checks**:
- [ ] Current price vs entry
- [ ] Unrealized P&L
- [ ] Distance to liquidation
- [ ] Funding costs accumulated

**Weekly Review**:
- [ ] Overall P&L including fees
- [ ] Whether to hold or close
- [ ] Lessons learned

**Alert Thresholds**:
- Price within 5% of liquidation: [ ] Alert set
- Funding rate > 0.05%/hour: [ ] Alert set
- Unrealized loss > 50% of margin: [ ] Alert set

## 🎯 Phase 4: Position Management Scenarios (15 minutes)

### Exercise 7: Scenario Response Planning

**Scenario 1: Price Moves Against You**

- Entry: $2,500
- Current: $2,450 (-2%)
- Liquidation: $2,000
- Unrealized Loss: $_______

**Your Response**:
- [ ] Close position (cut losses)
- [ ] Add margin (if still confident)
- [ ] Do nothing (if within plan)
- [ ] Other: _______

**Reasoning**: _________________________________

**Scenario 2: Price Moves in Your Favor**

- Entry: $2,500
- Current: $2,600 (+4%)
- Unrealized Profit: $_______

**Your Response**:
- [ ] Close 50% (lock profits)
- [ ] Move stop loss to break-even
- [ ] Let it run to take profit
- [ ] Other: _______

**Reasoning**: _________________________________

**Scenario 3: Funding Rate Spikes**

- Original: 0.01% per hour
- Current: 0.05% per hour (5x increase)
- Daily cost now: $_______

**Your Response**:
- [ ] Close position immediately
- [ ] Monitor closely
- [ ] Do nothing (short-term spike)
- [ ] Other: _______

**Reasoning**: _________________________________

### Exercise 8: Exit Strategy Planning

**Define your exit conditions**:

**Take Profit Exits**:
- Target 1 (partial): $_______ (close 50%)
- Target 2 (full): $_______ (close remaining)

**Stop Loss Exits**:
- Hard Stop: $_______
- Trailing Stop: Yes / No (if yes, explain: _______)

**Time-Based Exits**:
- Maximum Hold Time: _______ days
- Reason: _________________________________

**Condition-Based Exits**:
- Close if funding > _______% per hour
- Close if liquidation within _______%
- Close if fundamental change: _______

## ✅ Phase 5: Post-Trade Reflection (10 minutes)

### Exercise 9: Trade Journal Entry

**After closing your position, complete this**:



![Position Monitoring Log](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_04/ex04_02_position_monitoring_log.png)



![Position Planning Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_04/ex04_01_position_planning_template.png)

**Trade Summary**:
- Entry: $_______
- Exit: $_______
- Duration: _______ days
- Final P&L: $_______
- ROI: _______%

**What Went Well**:
- _________________________________

**What Could Improve**:
- _________________________________

**Lessons Learned**:
- _________________________________

**Would You Trade This Again?** Yes / No
- Why: _________________________________

### Exercise 10: Risk Management Review

**Assess your risk management**:

- [ ] Position size was appropriate
- [ ] Leverage was conservative
- [ ] Stop loss was set and respected
- [ ] Funding costs were accounted for
- [ ] Monitoring was adequate
- [ ] Exit strategy was followed

**Areas for Improvement**:
- _________________________________

## 🎯 Self-Assessment

Rate your readiness (1 = Not ready, 5 = Fully ready):

- [ ] Understanding of position mechanics: __/5
- [ ] Ability to calculate risks: __/5
- [ ] Confidence in execution: __/5
- [ ] Risk management plan: __/5
- [ ] Monitoring strategy: __/5

**Ready to open first position?** Yes / No
- If no, what do you need to review? _________________________________

## 🚀 Next Steps

**Before Opening Position**:
1. Complete all exercises above
2. Review any areas scoring < 4
3. Practice on testnet if available
4. Start with smallest position possible
5. Monitor closely for first few trades

**After First Position**:
1. Complete trade journal
2. Review what you learned
3. Adjust plan for next trade
4. Proceed to Module 2 (Protocol Mastery)

---

[← Back to Summary](../SUMMARY.md) | [Next: Module 2 →](../lessons/lesson-05-hyperliquid-the-l1-performance-leader.md)

