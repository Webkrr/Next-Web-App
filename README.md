# 🛒 Next.js Commerce Store (Sanity + Stripe)

A modern e-commerce web application built with **Next.js App Router**, **Sanity CMS**, and **Stripe**.  
This project follows a **headless commerce architecture** where content, payments, and frontend are decoupled for scalability and flexibility.

---

## 🚀 Tech Stack

### Frontend / Server
- Next.js 13+ (App Router)
- React
- TypeScript
- Tailwind CSS
- ShadCN UI

### Backend (Headless)
- Sanity CMS (content & products)
- Stripe (payments)


## 🧠 Architecture Overview

Next.js (UI + Server Logic)
|
|-- GROQ Queries
↓
Sanity CMS (Database + Admin UI)
|
|-- Checkout
↓
Stripe (Payments)

## 📁 Project Structure

├── app/ # Next.js app router
│ ├── page.tsx # Home page
│ ├── [category]/ # Category pages
│ ├── product/[slug]/ # Product detail pages
│ └── stripe/ # Checkout success/error
│
├── sanity/ # Sanity Studio (admin backend)
│ ├── schemas/ # Product & category schemas
│ └── sanity.config.ts # Sanity configuration
│
├── components/ # Shared UI components
├── lib/ # Utility functions
└── public/ # Static assets



🛠️ Installation
npm install --legacy-peer-deps

▶️ Running the Project
1. Start Next.js frontend
npm run dev


Runs at:

http://localhost:3000

2. Start Sanity Studio (backend CMS)
cd sanity
npm install
npm run dev


Runs at:

http://localhost:3333

🧪 Creating Data

Open Sanity Studio and create:

Categories

Products

Hero images

The frontend will update automatically.

💳 Stripe Payments

Stripe is used for checkout flow:

Test mode only

No real payments

Use Stripe test cards

If you don’t need payments, you can run the app without Stripe keys (just don’t click checkout).