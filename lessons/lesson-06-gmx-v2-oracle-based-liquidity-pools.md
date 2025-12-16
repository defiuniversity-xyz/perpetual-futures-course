---
module: 2
lesson_number: 6
course: perpetual-futures
---

## 🎧 Lesson Podcast

{% embed url="https://storage.googleapis.com/perpetual-futures-media/lesson-06/audio/lesson6_GMX_V2_Isolated_Pools_Risk_and_Fees.m4a" %}

## 🎬 Video Overview

{% embed url="https://storage.googleapis.com/perpetual-futures-media/lesson-06/video/lesson6_GMX_V2__Future_of_Trading_.mp4" %}

# Lesson 6: GMX V2 - Oracle-Based Liquidity Pools

## 🎯 Core Concept: Zero Slippage Through Oracle Pricing

GMX V2 represents the evolution from a unified liquidity pool (GLP) to isolated market pools (GM), while maintaining the core innovation: **zero price impact execution** at oracle prices. This model eliminates order books entirely, allowing traders to execute any size at the oracle price, provided the pool has sufficient depth.

### Why GMX V2 Matters

GMX V2 solved critical limitations of V1:
- **Risk Isolation**: Each market has its own pool (no contagion)
- **Permissionless Listings**: Can list volatile assets without threatening core markets
- **Dynamic Fees**: Price impact fees balance Open Interest
- **Chainlink Data Streams**: Low-latency oracle integration
- **Capital Efficiency**: LPs choose exposure (not forced into all assets)

## 📚 The Evolution: GLP to GM Pools

### GMX V1: The GLP Model

**How It Worked**:
- Single unified pool (GLP token)
- ~50% stablecoins, ~50% volatile assets
- All markets shared same liquidity
- Zero price impact execution

**Strengths**:
- ✅ Deep liquidity (all assets pooled)
- ✅ Simple for LPs (one token: GLP)
- ✅ Zero slippage execution

**Weaknesses**:
- ❌ Risk contagion (one asset failure affects all)
- ❌ Limited asset listings (couldn't list risky assets)
- ❌ OI imbalances (no sophisticated rebalancing)
- ❌ Forced exposure (LPs exposed to all assets)

### GMX V2: The GM Pool Model

**How It Works**:
- Each market has dedicated pool (GM-ETH-USDC, GM-BTC-USDC, etc.)
- Risk completely isolated
- LPs choose which pools to deposit into
- Permissionless market creation

**Key Innovation**: Moving from "communal" to "siloed" liquidity model.

## 🏗️ GM Pool Architecture

### Structural Isolation

**Example Markets**:
- ETH/USD → GM-ETH-USDC pool (ETH + USDC)
- BTC/USD → GM-BTC-USDC pool (BTC + USDC)
- SOL/USD → GM-SOL-USDC pool (SOL + USDC)

**Isolation is Absolute**:
- Assets in ETH pool cannot settle SOL trades
- If SOL pool fails, ETH pool unaffected
- Each pool operates independently

### Standard vs. Synthetic Markets

#### Standard Markets (Fully Backed)

**How It Works**:
- Pool holds actual tokens being traded
- ETH/USD pool holds ETH (Long Token) + USDC (Short Token)
- Trader opens Long ETH = "rents" upside of pool's ETH

**Example**: 
- Pool has 1,000 ETH and 2,500,000 USDC
- Trader opens $10,000 Long ETH position
- If ETH rises 10%, trader profits from pool's ETH reserves

**Use Cases**: Blue-chip assets (BTC, ETH) with deep on-chain liquidity

#### Synthetic Markets (Partially Backed)

**How It Works**:
- Pool backing doesn't match index token
- DOGE/USD market backed by ETH + USDC (not DOGE)
- Oracle tracks DOGE price, but settles using ETH/USDC

**Example**:
- DOGE/USD market backed by ETH and USDC
- Trader opens Long DOGE
- If DOGE pumps 50% but ETH stays flat, pool faces delta mismatch

**Risk Profile**:
- Higher risk (delta mismatch)
- Stricter OI caps
- Higher fees to discourage manipulation

**Use Cases**: Assets not native to chain, low on-chain liquidity

### GM Token Valuation

**GM Token Components**:
1. **Asset Value**: Real-time value of Long + Short tokens in pool
2. **Pending PnL**: Net profit/loss of all open positions
   - If traders have $1M unrealized profit → GM token value decreases
   - If traders have $1M unrealized loss → GM token value increases
3. **Accrued Fees**: Auto-compounded trading fees

**Key Insight**: GM token holders are the "house" for that market—they earn fees but absorb trader PnL volatility.

## 🔗 The Oracle Engine: Chainlink Data Streams

### Push vs. Pull Architecture

**V1 Push Model**:
- Chainlink nodes push updates when price deviates 0.1% or heartbeat expires
- Creates latency gap (on-chain price can lag CEX)
- Toxic arbitrageurs exploit stale prices

**V2 Pull Model (Data Streams)**:
- Chainlink aggregates prices off-chain at sub-second intervals
- When trade occurs, latest price is "pulled" on-chain
- Price data is seconds old (not hours)
- Gas efficient (only updates when needed)

### Two-Step Execution Process

**Step 1: Order Submission**
- Trader submits transaction to "request" trade
- Request queued in smart contract

**Step 2: Order Execution**
- Keeper network monitors request queue
- Keeper fetches latest Chainlink price signature
- Keeper submits execution transaction
- Trader pays execution fee (covers keeper gas)

**Verification**: Smart contract verifies Chainlink signature and timestamp. If stale or invalid, transaction reverts.

### Zero Price Impact: Reality vs. Perception

**What "Zero Price Impact" Means**:
- Trade executes at oracle Index Price
- No spread widening due to order book depth
- $10M order executes at same base price as $10 order

**What It Doesn't Mean**:
- Total cost is not zero
- Price Impact Fees apply (simulated slippage)
- Large trades that unbalance pool pay higher fees

**Key Distinction**: GMX V2 simulates market depth via fees, not price spread.

## 💰 The Multi-Layered Fee Structure

### Base Trading Fees

**V1**: Flat 0.1% (10 bps)

**V2**: Dynamic 0.05% - 0.07% (5-7 bps)
- **Rebate Logic**: Fee depends on trade's impact on pool balance
- If trade increases imbalance (adds Longs to Long-heavy pool): 0.07%
- If trade decreases imbalance (adds Shorts to Long-heavy pool): 0.05%

**Purpose**: Incentivize trades that rebalance the pool.

### Price Impact Fee

**The Innovation**: Simulates market depth without order book.

**How It Works**:
- Function of initial imbalance and target imbalance after trade
- Large trades that unbalance pool pay higher fees
- Small trades or rebalancing trades pay lower fees

![GLP Token Mechanics](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_06/pf06_04_glp_token_mechanics.png)

![GMX V2 Fee Structure Breakdown](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_06/pf06_03_gmx_v2_fee_structure_breakdown.png)

![Oracle Pull vs Push Mechanism](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_06/pf06_02_oracle_pull_vs_push_mechanism.png)

![GMX V2 Pool Structure Diagram](https://storage.googleapis.com/perpetual-futures-gitbook-images/lessons/lesson_06/pf06_01_gmx_v2_pool_structure_diagram.png)

**Example**:
- Pool is 80% Long, 20% Short
- Trader opens large Long position → High price impact fee
- Trader opens Short position → Low price impact fee (rebalancing)

**Purpose**: Discourage toxic flow, reward arbitrageurs.

### Funding Rate

**V1**: No funding rate (only borrow fee paid by both sides)

**V2**: Velocity-based funding rate
- Responds to OI imbalance velocity
- Fast imbalance growth → Higher funding
- Encourages contrarian traders to rebalance

### Borrow Fee

**How It Works**:
- Utilization-based fee
- High pool utilization → Higher borrow fee
- Encourages LPs to deposit more capital

## 🎓 Beginner's Corner: Using GMX V2

### Getting Started

**Step 1: Network Configuration**
1. Set MetaMask to Arbitrum One network
2. Add network if needed (Chainlist.org)

**Step 2: Acquire Assets**
1. Buy USDC on CEX or swap on DEX
2. Bridge to Arbitrum (official bridge or Synapse/Stargate)
3. Keep some ETH for gas

**Step 3: Navigate to GMX**
1. Go to GMX V2 interface
2. Connect wallet
3. Select "Trade" tab

### Opening a Position

**Step-by-Step**:
1. **Select Market**: Choose ETH/USD (or other)
2. **Check Pool**: View pool depth and current OI
3. **Choose Direction**: Long or Short
4. **Set Size**: Enter collateral amount
5. **Review Fees**: See price impact fee estimate
6. **Check Funding**: Review current funding rate
7. **Execute**: Click "Open Position"
8. **Approve**: Sign transaction in wallet
9. **Wait for Keeper**: Keeper executes (usually <1 minute)

**Key Metrics to Check**:
- Pool depth (sufficient liquidity?)
- Open Interest (balanced or skewed?)
- Funding rate (acceptable?)
- Price impact fee (reasonable for your size?)

## 🔬 Advanced Deep-Dive: LP Strategy

### Pool Selection

**For Conservative LPs**:
- Standard markets (ETH, BTC)
- Large pool depth
- Balanced OI
- Lower fees but safer

**For Aggressive LPs**:
- Synthetic markets (higher risk/reward)
- Smaller pools (higher fee share)
- Volatile assets (more trading = more fees)

### Delta-Neutral Strategies

**The Concept**: Eliminate price exposure while earning fees.

**How It Works**:
1. Deposit into GM pool (e.g., GM-ETH-USDC)
2. Hedge ETH exposure on CEX or spot market
3. Earn GM fees while price-neutral

**Example**:
- Deposit $10,000 into GM-ETH-USDC pool
- Short $10,000 ETH on CEX
- Net exposure: ~0 (delta neutral)
- Earn: GM trading fees + funding (if favorable)

**Risk**: Basis risk (GM price vs CEX price divergence)

### GMX Liquidity Vaults (GLV)

**What They Are**: Automated vaults that manage GM exposure.

**How They Work**:
- Deposit into GLV
- Vault automatically:
  - Selects pools
  - Manages delta exposure
  - Rebalances as needed

**Benefits**:
- Passive management
- Professional strategies
- Diversification

**Risks**:
- Vault manager risk
- Strategy risk
- Fees (management + performance)

## ⚠️ Risks and Considerations

### Oracle Risk

**Latency Arbitrage**:
- Even with Data Streams, small latency exists
- Sophisticated arbitrageurs can exploit
- LPs bear the cost (toxic flow)

**Oracle Manipulation**:
- Rare but possible
- Chainlink has safeguards
- Monitor for unusual price movements

### Pool Insolvency Risk

**When It Happens**:
- Traders win big (pool pays out)
- Pool assets insufficient to cover
- GM token value decreases

**Mitigation**:
- OI caps prevent excessive exposure
- Price impact fees discourage large imbalanced trades
- Funding rates incentivize rebalancing

### Keeper Centralization

**Risk**: If keeper network is centralized or colludes:
- Could censor transactions
- Could delay execution
- Could manipulate timing

**Mitigation**:
- Multiple keeper networks
- Decentralization efforts
- Monitor keeper performance

## 📊 Real-World Example: Trading on GMX V2

**Scenario**: Open $10,000 Long ETH position

**Setup**:
- Protocol: GMX V2 (Arbitrum)
- Market: ETH/USD
- Collateral: $2,000 USDC
- Leverage: 5x

**Execution**:
1. Navigate to GMX V2, connect wallet
2. Select ETH/USD market
3. Check pool depth: $50M (sufficient)
4. Check OI: 60% Long, 40% Short (slightly imbalanced)
5. Check funding: 0.01% per hour (acceptable)
6. Enter $2,000 collateral, 5x leverage
7. Review price impact fee: 0.02% ($2)
8. Click "Open Position"
9. Approve transaction
10. Keeper executes within 30 seconds
11. Position opened at oracle price ($2,500)

**Advantages**:
- Zero slippage (executed at oracle price)
- Simple execution (no order book)
- Large size capability (pool has depth)

**Costs**:
- Trading fee: 0.06% ($6)
- Price impact fee: 0.02% ($2)
- Funding: 0.01% per hour
- Total upfront: $8

## ⚖️ Compare Protocols

See how GMX V2 compares to other perpetual DEXs:

## 🔑 Key Takeaways

- GMX V2 uses isolated pools (no risk contagion)
- Zero price impact execution at oracle prices
- Chainlink Data Streams enable low-latency pricing
- Dynamic fees (price impact, funding, borrow) balance OI
- Standard markets (backed) vs Synthetic markets (delta mismatch)
- GM tokens represent pool equity (asset value + PnL + fees)
- Best for: Large position traders, LPs seeking yield, simple execution

## 🚀 Next Steps

- Proceed to Lesson 7 to learn about Drift's hybrid architecture
- Complete Exercise 6 to practice GMX V2 market analysis
- Explore GMX V2 interface to see oracle-based execution
- Consider GM pools for liquidity provision strategies

