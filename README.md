# 🏏 IPL Auction Simulator: The Ultimate Franchise Experience

Welcome to the **IPL Auction Simulator** — a premium, real-time multiplayer platform designed to replicate the high-stakes thrill of a real Indian Premier League player auction. 

Whether you are hosting a watch party, competing with friends, or just testing your squad-building skills, this platform offers a complete, end-to-end franchise management experience. From the suspense of the waiting room to the final gavel drop, every detail is engineered for maximum excitement.

---

## 🌟 The Journey: How It Works

### 1. The Waiting Room (The Pre-Auction Hype)
Your journey begins in the **Waiting Room**. 
- **Franchise Selection:** Connect using a unique room code and select your favorite franchise. Duplicate selections are blocked, ensuring every team is unique.
- **Immersive Theming:** The moment you pick your team, your UI dynamically adapts. The lobby glows with your franchise's colors, setting the tone for the battles to come.
- **Ignition:** Once all owners are ready, the Host clicks the **"Ignite Auction"** button. Everyone is synchronously transported from the lobby straight into the live bidding dashboard.

### 2. The Live Bidding Dashboard (The Main Event)
This is where fortunes are made and lost. The dashboard features a **futuristic, holographic design** with glowing gold accents.
- **Authentic Player Sets:** Players are presented one by one, moving through structured sets (Marquee, Batsmen, Spinners, etc.) just like the real broadcast. While the sets are structured, the order of players *within* each set is uniquely randomized for every room to keep you guessing.
- **Real-Time Combat:** When a player appears, the countdown timer begins. Click **Bid** to raise your paddle. The system handles the math, automatically calculating the next legal increment (₹5L, ₹10L, ₹20L, or ₹25L depending on the current price).
- **Feel the Pressure:** If the timer hits zero, the player is sold to the highest bidder. Miss out? They're gone. Every bid triggers snappy animations, and winning a player triggers a celebration effect.
- **Purse Management:** Keep an eye on your budget! You start with ₹120 Crore. The system actively tracks your remaining purse, your maximum possible bid, and your overseas player limits.

### 3. The Trade Desk (Post-Auction Negotiations)
The auction might be over, but the strategy isn't. 
- Head to the **Trade** page to propose player-for-player swaps with rival franchises.
- See a high-fidelity visual representation of the trade. The receiving team can accept or reject your offer in real-time.

### 4. Playing XI & Final Standings
Now that your squad is finalized, it's time to build your best team.
- **Submit Your XI:** Pick your best 11 players from your squad.
- **Team Ratings:** The system calculates a total team rating based on your selections (using our comprehensive `espnlist.json` dataset). The Host controls whether player Overall (OVR) ratings are visible during the auction, but the final results reveal all!
- **The Results:** View the final leaderboard. See every team's complete squad, how much they spent, and how their final Playing XI stacks up against the competition.

---

## ✨ Platform Highlights

* 🎨 **Premium Visuals:** Glassmorphism cards, Framer Motion animations, and deep franchise-color integration make the platform look and feel like a high-end esports broadcast.
* ⚡ **Zero Latency:** Powered by Socket.IO WebSockets, every bid, timer tick, and trade offer is synchronized across all players' screens in milliseconds.
* 📱 **Fully Responsive:** Whether you are bidding furiously on a desktop monitor or trading players from your mobile phone, the interface is optimized for every screen size.
* 🏏 **Rich Player Data:** Featuring a massive database of international and domestic talent, complete with base prices, roles, and historical stats.

---

## 🛠️ For Developers

Are you a developer looking to run this locally or contribute? Here is a quick overview of what powers the platform under the hood.

### Tech Stack
- **Frontend:** Next.js 16, React 19, Tailwind CSS v4, Framer Motion, Lucide React
- **Backend:** Custom Node.js server wrapping Next.js, Socket.IO
- **Database:** PostgreSQL via Prisma ORM 6
- **Architecture Highlights:** Debounced database syncing for high-frequency bidding, optimistic UI updates, and a custom seeded PRNG for room-specific player shuffling.

### Local Setup
```bash
# Clone the repo & install dependencies
git clone https://github.com/PremSahith/IA.git
cd IA
npm install

# Setup your environment variables (.env)
# DATABASE_URL=postgresql://user:password@host:5432/ipl_auction

# Run migrations & start the server
npx prisma migrate deploy
npm run dev
```

---
*Private project — all rights reserved.*
