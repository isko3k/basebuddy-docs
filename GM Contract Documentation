# GM Contract

Send a GM message that lives **onchain forever**.  
Every time you say GM, the contract tracks your streak and awards energy points — think of it as **proof you showed up today**.  
Your GM count and last message are stored on the blockchain, and your energy points grow with every greeting.

---

## Contract Address

| Contract | Address |
|-----------|----------|
| **GM Contract** | `0xa42bbE6477CF20dAa5c9b04b68dBA385e42eb971` |

---

## What It Does

The GM Contract is your onchain greeting system on **Base**.  
Every time you say GM, the blockchain records it forever, tracks your dedication through streaks, and rewards you with **energy points**.  
Your greetings aren’t just messages — they’re timestamped proof of your participation in the Base community.

---

## How It Works

### Sending a GM
When you call the `Greeter()` function:

1. The contract checks that you’ve waited at least **1 hour** since your last GM  
2. It updates your **streak** (consecutive days saying GM)  
3. It tracks how many GMs you’ve sent **today**  
4. It awards **energy points** based on your daily activity  
5. Your stats are permanently recorded **onchain**

---

### Energy Rewards

| GM Count Today | Energy Earned | Action Type |
|----------------|----------------|--------------|
| 1st GM | 100 points | `gm_first` |
| 2nd–4th GM | 200 points each | `gm_streak` |
| 5th GM | 500 points (bonus) | `gm_5_bonus` |
| 6th+ GM | 200 points each | `gm_streak` |

**The 5-GM Bonus**  
Once per day, hitting your 5th GM triggers a **500-point bonus**.  
After that, additional GMs earn the standard 200 points.

---

### Streaks

Your streak increases every consecutive day you say GM.  
If you skip a day, your streak resets — but your all-time best streak is saved forever.

| Example | Result |
|----------|--------|
| Day 1: GM | Streak: 1 |
| Day 2: GM | Streak: 2 |
| Day 3: GM | Streak: 3 |
| Day 5: GM (missed day 4) | Streak: 1 (reset) |

---

### Cooldown

- **1 hour cooldown** between GMs  
- Multiple GMs per day are allowed (if spaced 1 hour apart)  
- The daily GM counter resets at **midnight UTC**

You can send up to 24 GMs per day, but most users send 1–5 to maximize efficiency.

---

## Your Stats

The contract stores stats for every user:

| Stat | Description |
|------|--------------|
| **Total GMs** | Lifetime count of all GMs sent |
| **Current Streak** | Consecutive days with at least one GM |
| **Longest Streak** | Your all-time best streak |
| **GMs Today** | Count resets daily at midnight UTC |
| **Last GM Time** | Timestamp of your most recent GM |
| **Next Energy Reward** | Points your next GM will earn |

Example output from `getMyStats()`:

```javascript
{
  totalGms: 127,
  currentStreak: 15,
  bestStreak: 23,
  gmsToday: 3,
  lastTime: 1698765432,
  cooldown: 3245,
  nextEnergyReward: 200
}
