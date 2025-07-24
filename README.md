# 💧 Water Exchange Platform
A marketplace for farmers to trade water and water credits.

## 🌐 Tech Stack
- **Frontend:** Next.js + TailwindCSS + shadcn/ui
- **Backend:** Node.js + Express + Prisma ORM
- **Database:** PostgreSQL (Railway or Supabase)
- **Auth:** Clerk

---

## 🚀 Getting Started

### 🔧 Prerequisites
- Node.js
- PostgreSQL DB URL
- Clerk account (https://clerk.dev)

### 📦 Install Dependencies
```bash
npm install
```

### ⚙️ Environment Variables (`.env`)
```
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE"
CLERK_SECRET_KEY="your-clerk-secret-key"
CLERK_PUBLISHABLE_KEY="your-clerk-publishable-key"
CLERK_API_URL="https://api.clerk.dev"
PORT=4000
```

### 🔄 Prisma Setup
```bash
npx prisma generate
npx prisma migrate dev --name init
```

### ▶️ Start Backend Server
```bash
npm run dev # or node index.js
```

---

## 📁 Project Structure
```
server/
├── index.js               # Express API
├── middleware/
│   └── requireAuth.js     # Clerk auth guard
├── prisma/
│   └── schema.prisma      # DB schema
.env                       # Environment config
```

---

## 🧪 API Routes

### Listings
- `GET /api/listings` — All listings
- `POST /api/listings` — Create listing *(auth required)*

### Trades
- `GET /api/trades` — All trades
- `POST /api/trades` — Match trade *(auth required)*

---

## 🛰 Deployment

### Backend on Railway
- Push repo to GitHub
- Import to Railway
- Add `.env` vars under Environment tab
- Deploy + run migrations

### Frontend on Vercel
- Import Next.js repo
- Add Clerk + API env vars
- Deploy with default settings

---

## ✨ Future Features
- Water escrow & smart contract escrow
- Transaction status updates
- Regional water right validation
- Forecasting tools with NOAA/USGS data

---

## 🧑‍🌾 Built for farmers, with modern tools 🌱
