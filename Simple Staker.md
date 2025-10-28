# Simple Staking

The **Simple Staking Contract** lets you stake **BUDDY tokens** and earn rewards based on how long you lock them.  
Pick a commitment level, stake your tokens, and watch your rewards grow over time — all on Base.

> **Note:** BUDDY is a free, test-only token with no real-world or monetary value. It’s used purely for learning and experimenting within BaseBuddy.

---

## Contract Info

| Item | Address |
|------|----------|
| **Staking Contract** | `0x6aE789F61c5B12038ab73Af41D63C6E3899B429e` |
| **BUDDY Token** | `0xF89CE9396A7eD0e634cCd7C52eA3D0FA21b8863a` |

---

## What It Does

Simple Staking is a **time-based rewards system**:

- Lock your BUDDY tokens for a set period  
- Earn rewards that build up over time  
- Claim your rewards anytime (even while still staked)  
- After your lock ends, claim everything — tokens + rewards  

It’s like earning **interest** on your BUDDY tokens by committing to hold them.

---

## Lock Periods & Rewards

| Lock Period | APY | Reward Rate |
|--------------|-----|--------------|
| **1 Week** | 50% | 50,000 basis points |
| **1 Month** | 100% | 100,000 basis points |
| **3 Months** | 200% | 200,000 basis points |

**Example:**  
If you stake **1,000 BUDDY** for **3 months (200% APY)**  
→ You’ll earn up to **2,000 BUDDY** over the full period.  
Rewards grow **linearly**, so you can claim partial rewards anytime before the end.

---

## How It Works

### Staking Steps

1. **Get BUDDY tokens** (from the faucet or BaseBuddy airdrops)  
2. **Approve** the staking contract to use your tokens  
3. **Choose a lock period** (1 week, 1 month, or 3 months)  
4. **Stake** your tokens  
5. **Earn rewards** automatically over time  

### Claiming Rewards

You can:

- **Claim Rewards Only:** collect your earned BUDDY anytime while staying staked  
- **Unstake Everything:** after the lock ends, claim all tokens + rewards in one go  

---

## Faucet (Free BUDDY)

No tokens? No problem.

| Feature | Details |
|----------|----------|
| **Amount** | 1,000 BUDDY per claim |
| **Cooldown** | Once every 24 hours |
| **Eligibility** | Anyone on BaseBuddy |

**How to use it:**
1. Click **Claim Faucet** in the BaseBuddy app  
2. Wait for the transaction to confirm  
3. 1,000 BUDDY appears in your wallet  
4. Claim again after 24 hours  

The faucet helps new users test staking and onchain actions — no purchase required.

---

## Reward Growth

Rewards increase based on **how long you’ve been staked**.  
They’re calculated proportionally to time passed vs total lock period.

| Time Elapsed | Example (3-Month Stake of 1,000 BUDDY @ 200% APY) | Claimable Reward |
|---------------|--------------------------------------------------|------------------|
| 0 days | Just staked | 0 BUDDY |
| 15 days | Half a month | ~333 BUDDY |
| 45 days | Halfway | ~1,000 BUDDY |
| 90 days | Full term | 2,000 BUDDY |

You can **claim anytime** — rewards build up gradually and reset after each claim.

---

## Multiple Stakes

You can create **multiple stakes** with different:
- Lock periods  
- Start times  
- Amounts  

Example strategies:

**Diversified:**  
- 500 BUDDY for 1 week (fast rewards)  
- 1,000 BUDDY for 1 month (steady growth)  
- 2,000 BUDDY for 3 months (maximum rewards)  

**Laddered:**  
- Stake 1,000 BUDDY every month for 3 months  
- You’ll get one stake unlocking each month — creating consistent liquidity

---

## Gas & Efficiency

The contract is designed to be **light and efficient** on Base:

| Action | Typical Gas |
|---------|--------------|
| Approve | ~45,000 |
| Stake | ~100,000 |
| Claim Rewards | ~60,000 |
| Unstake | ~80,000 |

Each action usually costs just a few cents in Base gas fees.

---

## Funding & Rewards Pool

The staking contract must hold enough **BUDDY** to pay rewards.  
If the contract balance runs low, rewards pause until it’s refilled.

| Function | Description |
|-----------|--------------|
| **fundContract(amount)** | Add BUDDY for rewards |
| **withdrawExcess(amount)** | Remove unused BUDDY (owner only) |

Before staking large amounts, always make sure the contract has a healthy reward balance.

---

## Use Cases

### For BUDDY Holders
- Earn passive rewards on idle tokens  
- Choose your own lock period  
- Claim rewards flexibly  
- Stack multiple stakes for better timing  

### For Learners & Builders
- Practice staking logic safely  
- Understand reward accrual systems  
- Experiment with Base transactions  

### For Projects
- Simulate staking or loyalty systems  
- Reward testnet contributors  
- Educate users about DeFi mechanics  

---

## Risks & Best Practices

| Type | What to Know |
|------|---------------|
| **Smart Contract Risk** | The staking contract is
