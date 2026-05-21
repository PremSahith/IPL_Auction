<div align="center">

<br/>

<img src="https://img.shields.io/badge/🏏-IPL%20AUCTION%20SIMULATOR-gold?style=for-the-badge&labelColor=1a1a2e&color=c8a951" alt="IPL Auction Simulator"/>

<br/><br/>

**A premium, real-time multiplayer platform for high-stakes franchise auctions.**

*The waiting room. The countdown. The final gavel. All of it.*

<br/>

[![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=flat-square&logo=socket.io&logoColor=white)](https://socket.io/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://postgresql.org/)
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)](https://prisma.io/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)

<br/>

[![View Demo](https://img.shields.io/badge/View%20Demo-%E2%86%92-c8a951?style=for-the-badge&labelColor=1a1a2e)](https://ipl-auction-lw63.onrender.com/)

</div>

---

## The Experience

### 1 · Waiting Room
Join via a unique room code and claim your franchise. Duplicate picks are blocked — every team belongs to exactly one owner. The moment you choose, your entire UI adapts to your franchise's colors. When everyone is ready, the Host hits **Ignite Auction** and all clients transition to the live dashboard simultaneously.

### 2 · Live Bidding Dashboard
Players appear one by one in structured sets — Marquee, Batsmen, Spinners, and more — mirroring the real broadcast format. The order within each set is uniquely seeded per room so no two auctions play out the same.

Hit **Bid** before the countdown hits zero. The system auto-calculates the next legal increment (₹5L / ₹10L / ₹20L / ₹25L based on current price). Every bid triggers snappy animations; winning a player triggers a full celebration effect. Miss the timer and they're gone.

Your **₹120 Crore purse**, maximum possible bid, and overseas slot count are tracked live.

### 3 · Trade Desk
Once the gavel drops, head to the Trade page to negotiate player-for-player swaps with rival franchises. Proposals render as a high-fidelity visual comparison; the receiving team accepts or rejects in real-time.

### 4 · Playing XI & Final Standings
Pick your best 11 from your squad. The system scores each team against the full `espnlist.json` dataset (OVR ratings optionally hidden during the auction, revealed at the end). The final leaderboard shows every franchise's complete squad, spend, and XI rating side by side.

---

## Highlights

| | |
|---|---|
| ⚡ **Zero latency** | Socket.IO WebSockets sync every bid, timer tick, and trade offer in milliseconds |
| 🎨 **Premium visuals** | Glassmorphism cards, Framer Motion animations, deep franchise-color integration |
| 📱 **Fully responsive** | Optimized from a desktop auction setup down to mobile trading |
| 🏏 **Rich player data** | Full international and domestic database with base prices, roles, and historical stats |
| 🔀 **Seeded randomness** | Custom PRNG ensures room-specific player ordering — reproducible but unique |
| 🛡️ **Resilient writes** | Debounced DB syncing handles high-frequency bidding without hammering Postgres |

---

## Tech Stack

**Frontend**

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer%20Motion-0055FF?style=flat-square&logo=framer&logoColor=white)
![Lucide](https://img.shields.io/badge/Lucide%20React-F56565?style=flat-square)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=flat-square&logo=socket.io&logoColor=white)

**Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)

---

## Architecture Notes

**Debounced DB syncing** — bid events fire at high frequency during contested auctions; writes are debounced to prevent Postgres contention while keeping in-memory state authoritative.

**Optimistic UI** — bid confirmations render client-side immediately, reconciled against server state on the next socket event for a snappy, lag-free feel.

**Seeded PRNG** — each room gets a deterministic shuffle of players within sets, derived from the room code. Reproducible for debugging; unique per game.

**Franchise theming** — color tokens are injected at the session level via CSS variables, scoping the entire UI to the selected franchise without re-renders.

---

<div align="center">
<sub>Private project — all rights reserved.</sub>
</div>
