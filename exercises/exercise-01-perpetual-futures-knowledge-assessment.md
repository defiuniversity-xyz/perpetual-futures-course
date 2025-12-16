# Exercise 1: Perpetual Futures Knowledge Assessment

⏰ Time Investment: 30-45 minutes  
🎯 Goal: Test your understanding of perpetual futures fundamentals and identify knowledge gaps

📚 Required Reading Integration  
📖 Primary: Lesson 1: Understanding Perpetual Futures Fundamentals  
📖 Supporting: Lesson 2: The Mathematics of Perpetual Trading

## 🔍 Phase 1: Knowledge Check (10 minutes)

### Understanding Check

Answer these questions to assess your comprehension:

**1. What is the fundamental difference between perpetual futures and traditional futures?**
   - Your answer: _________________________________

**2. How do funding rates keep perpetual prices aligned with spot prices?**
   - Your answer: _________________________________

**3. What happens when funding rate is positive and you're holding a long position?**
   - Your answer: _________________________________

**4. What is the difference between isolated margin and cross margin?**
   - Your answer: _________________________________

**5. Why can perpetual futures exist without expiration dates?**
   - Your answer: _________________________________


![Knowledge Assessment Answer Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_01/ex01_01_knowledge_assessment_answer_template.png)


## 📊 Phase 2: Scenario Analysis (15 minutes)

### Funding Rate Scenario

**Scenario**: You're considering a long ETH perpetual position.

**Market Conditions**:
- ETH Spot Price: $2,500
- ETH Perpetual Price: $2,550
- Funding Rate: 0.02% per hour (positive)
- Your Position: $10,000 notional (5x leverage on $2,000 margin)

**Exercise 1**: Calculate the funding cost:
- Hourly payment: $_______
- Daily payment (24 hours): $_______
- Annualized rate: _______%

**Exercise 2**: If ETH price stays flat at $2,500 for 7 days, what is your net P&L?
- Funding paid over 7 days: $_______
- Price movement: $_______
- Net P&L: $_______
- ROI: _______%

**Exercise 3**: What does this tell you about the importance of funding rates?
- Your answer: _________________________________

### Leverage Scenario

**Scenario**: You want to open a position with different leverage levels.

**Setup**:
- Available Margin: $1,000
- Entry Price: $2,500
- Maintenance Margin: 0.5%

**Exercise 4**: Calculate position size and liquidation price for each leverage:

| Leverage | Position Size | Liquidation Price | Safety Buffer |
|----------|---------------|-------------------|---------------|
| 2x | $_______ | $_______ | _______% |
| 5x | $_______ | $_______ | _______% |
| 10x | $_______ | $_______ | _______% |

**Exercise 5**: Which leverage would you choose for your first trade and why?
- Your choice: _______
- Reasoning: _________________________________


![Funding Rate Scenario Calculator](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_01/ex01_02_funding_rate_scenario_calculator.png)


## 💡 Phase 3: Risk Identification (10 minutes)

### Common Mistakes Exercise

Identify the mistake in each scenario:

**Scenario 1**: 
Trader opens 20x long position on ETH, thinking "I'm safe until price drops 5%."

**The Mistake**: _________________________________

**Why It's Wrong**: _________________________________

**Scenario 2**:
Trader holds long position for 30 days, pays 0.01% per hour funding, says "funding is negligible."

**The Mistake**: _________________________________

**Why It's Wrong**: _________________________________

**Scenario 3**:
Trader uses cross margin for first trade, opens long BTC and long ETH, both get liquidated when market crashes.

**The Mistake**: _________________________________

**Why It's Wrong**: _________________________________

## 📝 Phase 4: Key Concepts Review (10 minutes)

### Fill in the Blanks

**1. Perpetual futures use _______________ to keep prices aligned with spot, instead of expiration dates.**

**2. When perpetual price is above spot price, _______________ positions pay _______________ positions.**

**3. With _______________ margin, your maximum loss is limited to the margin you allocate to that position.**

**4. _______________ amplifies both profits and losses, making liquidation risk higher.**

**5. The _______________ is the price at which your position will be automatically closed by the protocol.**

### True or False

**1. Perpetual futures never expire.** (True / False)

**2. Funding rates are always paid by long positions.** (True / False)

**3. Higher leverage always means higher profits.** (True / False)

**4. Isolated margin is safer than cross margin for beginners.** (True / False)

**5. You can lose more than your margin with isolated margin.** (True / False)

## ✅ Self-Assessment

Rate your understanding (1 = Need more review, 5 = Fully understand):

- [ ] Perpetual futures fundamentals: __/5
- [ ] Funding rate mechanics: __/5
- [ ] Margin types (isolated vs cross): __/5
- [ ] Leverage and liquidation: __/5
- [ ] Risk management basics: __/5

**Areas needing more review**: _________________________________

## 🎯 Next Steps

If you scored < 4 on any topic:
- Review Lesson 1 material on that topic
- Re-read the Beginner's Corner sections
- Practice calculations from Lesson 2
- Look up additional resources on unclear concepts

If all topics ≥ 4:
- Proceed to Exercise 2 (Calculation Practice)
- Move forward with confidence!

---

[← Back to Summary](../SUMMARY.md) | [Next: Lesson 2 →](../lessons/lesson-02-the-mathematics-of-perpetual-trading.md)

