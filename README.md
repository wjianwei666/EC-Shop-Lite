# EC Shop Lite - Full-Stack E-Commerce Platform

A budget-friendly, production-ready e-commerce platform built with **Python FastAPI** + **Vue 3**, supporting both **physical and digital products** with **Stripe, PayPal, and Cash on Delivery**.

> **Version:** Lite ($39) | **License:** Self-hosted, personal use only

---

## 📸 Screenshots

### Storefront — Mobile
![Mobile storefront](screenshots/shop-mobile.png)

### Storefront — Product List (Mobile)
![Mobile products](screenshots/shop-mobile-products.png)

### Admin Dashboard
![Admin dashboard](screenshots/admin-dashboard.png)

### Admin — Orders with Filters
![Admin orders](screenshots/admin-orders.png)

### Admin — Product Management with Filters
![Admin products](screenshots/admin-products.png)

### Buyer — Order History
![Buyer orders](screenshots/shop-orders.png)

### Digital Product Auto-Delivery
![Digital delivery](screenshots/order-digital-delivery.png)

---

## 🎬 Live Demo

> **Seller note:** replace the placeholder URLs below with your own deployment
> before publishing the listing — a clickable demo dramatically improves conversion.

| | URL | Login |
|---|---|---|
| **Storefront** | `https://your-demo-domain.com` | Register freely |
| **Admin Panel** | `https://your-demo-domain.com/admin` | `admin` / `change-me` |

**Demo tip:** keep the seed products and add 1–2 paid digital orders so buyers
can see the auto-delivery flow end-to-end.

---

## ✨ Features

### 🛍️ Customer Frontend
- Browse products with filtering (category, type, keyword, sort)
- Product detail pages for physical & digital goods
- Shopping cart with quantity management
- Checkout with Stripe, PayPal, or COD
- Order history & details
- User registration & login (JWT + bcrypt)

### ⚙️ Admin Dashboard
- Dashboard with sales & order statistics
- Product CRUD (physical + digital with file delivery)
- Order management with status workflows
- User management with role controls
- Category management
- Payment gateway toggling (Stripe/PayPal/COD)
- Site settings

### 💳 Payment Gateways (2 channels + COD)
| Gateway | Status | Use Case |
|---------|--------|----------|
| **Stripe** | ✅ Built-in | Credit/Debit cards |
| **PayPal** | ✅ Built-in | Global online payments |
| **Cash on Delivery** | ✅ Built-in | Pay upon receipt |

> Empty API keys = simulation mode for testing.

### 🏗️ Tech Stack
| Layer | Technology |
|-------|-----------|
| Backend | Python 3.11+ / FastAPI |
| Database | MySQL 5.7+ / 8.0 |
| ORM | SQLAlchemy 2.0 |
| Auth | JWT + bcrypt |
| Frontend | Vue 3 + Vite |
| UI Framework | Element Plus |
| State | Pinia |

---

## 📦 Project Structure

```
ec-shop-lite/
├── backend/
│   ├── app/
│   │   ├── models/          # Database models
│   │   ├── schemas/         # Pydantic schemas
│   │   ├── routers/         # API route handlers
│   │   ├── services/        # Business logic (2 gateways)
│   │   ├── config.py        # Settings from .env
│   │   ├── database.py      # MySQL connection
│   │   ├── auth.py          # JWT + bcrypt
│   │   └── main.py          # FastAPI app entry
│   ├── .env.example         # Env config template (simpler)
│   ├── requirements.txt     # Python dependencies
│   └── run.py               # Start script
├── frontend/
│   ├── src/
│   │   ├── api/             # Axios API client
│   │   ├── assets/          # CSS styles
│   │   ├── router/          # Vue Router
│   │   ├── stores/          # Pinia state
│   │   └── views/           # Shop + Admin views
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
├── sql/
│   └── init.sql             # DB schema (Stripe+PayPal+COD only)
└── README.md
```

---

## 🚀 Quick Start

### Prerequisites
- Python 3.11+
- Node.js 18+
- MySQL 5.7+ / 8.0

### 1. Database Setup

```bash
mysql -u root -p < sql/init.sql
```

### 2. Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your MySQL + Stripe/PayPal keys
python run.py
```

### 3. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

### 4. Access

| Page | URL |
|------|-----|
| Shop Frontend | http://localhost:5173 |
| Admin Dashboard | http://localhost:5173/admin |
| API Documentation | http://localhost:8000/docs |

**Default Admin:** `admin` / `admin123`

---

## 🔧 Payment Configuration (`.env`)

```env
# Stripe
STRIPE_SECRET_KEY=sk_live_xxx
STRIPE_PUBLISHABLE_KEY=pk_live_xxx
STRIPE_WEBHOOK_SECRET=whsec_xxx

# PayPal
PAYPAL_CLIENT_ID=xxx
PAYPAL_CLIENT_SECRET=xxx
PAYPAL_MODE=sandbox
```

---

## 🔒 Security

- Passwords hashed with **bcrypt**
- JWT token authentication
- Admin-only API endpoints
- SQL injection protection (SQLAlchemy ORM)

---

## 📱 Responsive Design

Fully responsive — mobile, tablet, and desktop layouts with adaptive grids and touch-friendly UI.

---

## 🏷️ Product Types

| Type | Features |
|------|----------|
| Physical | Stock tracking, weight, shipping address |
| Digital | Download URL, file name/size, download limits |

---

## ⚠️ License & Limitations

- **Framework:** FastAPI + Vue 3
- **Database:** MySQL
- **Password Encryption:** bcrypt
- **License:** Personal / self-hosted use only
- **NOT included:** Paddle, Lemon Squeezy, Polar gateways
- **NOT allowed:** Redistribution, resale, commercial use

---

## 📄 Upgrade Options

Need more payment gateways or commercial rights?

| | **Lite ($39)** | Standard ($69) | Commercial ($199) |
|---|:---:|:---:|:---:|
| Stripe + PayPal + COD | ✅ | ✅ | ✅ |
| Paddle + Lemon Squeezy + Polar | ❌ | ✅ | ✅ |
| Redistribution Rights | ❌ | ❌ | ✅ |
| 30-Day Support | ❌ | ❌ | ✅ |
| Deploy Scripts | ❌ | ❌ | ✅ |