# Exercise 3: Architecture Analysis and Selection

⏰ Time Investment: 30-45 minutes  
🎯 Goal: Learn to identify protocol architectures and select the right one for your strategy

📚 Required Reading Integration  
📖 Primary: Lesson 3: Architecture Types and Market Structure  
📖 Supporting: Lesson 1: Understanding Perpetual Futures Fundamentals

## 🔍 Phase 1: Architecture Identification (10 minutes)



![Use Case Analysis Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_03/ex03_02_use_case_analysis_template.png)



![Architecture Comparison Matrix Template](https://storage.googleapis.com/perpetual-futures-gitbook-images/exercises/exercise_03/ex03_01_architecture_comparison_matrix_template.png)

### Exercise 1: Protocol Classification

Classify each protocol by architecture type:

| Protocol | Architecture Type | Reasoning |
|----------|-------------------|-----------|
| Hyperliquid | _______ | _______ |
| GMX V2 | _______ | _______ |
| dYdX v4 | _______ | _______ |
| Drift Protocol | _______ | _______ |
| Perpetual Protocol | _______ | _______ |
| Vertex | _______ | _______ |

### Exercise 2: Architecture Characteristics

Fill in the table comparing architectures:

| Feature | CLOB | Oracle Pools | vAMM |
|---------|------|--------------|------|
| Price Discovery | _______ | _______ | _______ |
| Slippage | _______ | _______ | _______ |
| Liquidity Source | _______ | _______ | _______ |
| Trader Experience | _______ | _______ | _______ |
| Main Risk | _______ | _______ | _______ |

## 📊 Phase 2: Use Case Matching (15 minutes)

### Exercise 3: Strategy to Architecture Matching

Match each trading strategy to the best architecture:

**Strategies**:
1. Large position trading ($100k+)
2. Scalping (many small trades)
3. Funding rate arbitrage
4. Limit order trading
5. Simple swap-like execution

**Architectures**:
- A. CLOB
- B. Oracle Pools
- C. vAMM

| Strategy | Best Architecture | Reasoning |
|----------|-------------------|-----------|
| Large position trading | _______ | _______ |
| Scalping | _______ | _______ |
| Funding rate arbitrage | _______ | _______ |
| Limit order trading | _______ | _______ |
| Simple execution | _______ | _______ |

### Exercise 4: Risk Assessment by Architecture

**Scenario**: You want to open a $50,000 long ETH position

**Analyze risks for each architecture**:

**CLOB (Hyperliquid)**:
- Primary Risk: _________________________________
- How to Mitigate: _________________________________

**Oracle Pool (GMX)**:
- Primary Risk: _________________________________
- How to Mitigate: _________________________________

**vAMM (Perpetual Protocol)**:
- Primary Risk: _________________________________
- How to Mitigate: _________________________________

**Question**: Which architecture would you choose and why?
- Your choice: _______
- Reasoning: _________________________________

## 💡 Phase 3: Real-World Scenario Analysis (15 minutes)

### Exercise 5: Protocol Selection Scenario

**Your Situation**:
- Trading Experience: Beginner (first 10 trades)
- Capital: $5,000
- Strategy: Swing trading (hold 3-7 days)
- Priority: Safety and simplicity

**Options**:

**Option A: GMX V2 (Oracle Pool)**
- Zero slippage
- Simple interface
- Oracle risk
- Good liquidity

**Option B: Hyperliquid (CLOB)**
- Limit orders
- CEX-like experience
- Slippage on large orders
- Very fast execution

**Option C: Drift (Hybrid)**
- Multiple liquidity sources
- More complex
- Solana ecosystem
- Good for active trading

**Exercise**: Rank these options (1 = Best, 3 = Least suitable):

- Option A: ___
- Option B: ___
- Option C: ___

**Reasoning for #1**: _________________________________

### Exercise 6: Architecture Comparison Matrix

Create a comparison for your use case:

**Your Use Case**: [Fill in your trading style]

| Factor | CLOB | Oracle Pool | vAMM | Your Priority |
|--------|------|-------------|------|---------------|
| Execution Speed | | | | High/Med/Low |
| Slippage | | | | High/Med/Low |
| Complexity | | | | High/Med/Low |
| Risk Profile | | | | High/Med/Low |
| Capital Efficiency | | | | High/Med/Low |

**Best Match**: _______

**Why**: _________________________________

## 📝 Phase 4: Hybrid Architecture Understanding (10 minutes)

### Exercise 7: Drift's Liquidity Trifecta

**Question**: How does Drift's three-layer system protect LPs?

1. JIT Auction: _________________________________

2. DLOB: _________________________________

3. DAMM: _________________________________

**Question**: Why is this better than a simple AMM?
- Your answer: _________________________________

### Exercise 8: GMX V2 Evolution

**Question**: Why did GMX move from unified pool (GLP) to isolated pools (GM)?

- Your answer: _________________________________

**Question**: What are the benefits and drawbacks?

| Benefit | Drawback |
|---------|----------|
| _______ | _______ |
| _______ | _______ |

## ✅ Self-Assessment

Rate your understanding (1 = Need more review, 5 = Fully understand):

- [ ] Architecture types (CLOB, Oracle, vAMM): __/5
- [ ] Identifying protocols by architecture: __/5
- [ ] Matching strategy to architecture: __/5
- [ ] Risk assessment by architecture: __/5
- [ ] Hybrid models: __/5

**Areas needing more review**: _________________________________

## 🎯 Next Steps

If you scored < 4 on any topic:
- Review Lesson 3 architecture sections
- Study the comparison table
- Research specific protocols
- Practice identifying architectures

If all topics ≥ 4:
- Proceed to Exercise 4 (First Position Setup)
- You're ready to open your first position!

---

[← Back to Summary](../SUMMARY.md) | [Next: Lesson 4 →](../lessons/lesson-04-your-first-perpetual-position.md)

