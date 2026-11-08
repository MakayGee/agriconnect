# AgriConnect 🌿

> Community Agricultural Technology Platform for Lesotho

A full-stack application connecting farmers, buyers, and agricultural advisors — featuring blockchain records, AI predictions, and role-based security.

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL 13+
- Python 3.10+ (for AI dashboard)

### 1. Setup PostgreSQL Database

```sql
CREATE DATABASE agriconnect;
```

### 2. Backend

```bash
cd server
# Edit .env with your PostgreSQL credentials (DB_USER, DB_PASSWORD, DB_HOST, DB_PORT)
npm install
npm run dev               # Starts on http://localhost:5000
```

On first run it auto-creates tables and seeds demo data:
- **Admin:** admin@agriconnect.ls / Admin@1234
- **Farmer:** thabo@agriconnect.ls / Farmer@1234
- **Advisor:** mphato@agriconnect.ls / Advisor@1234

### 3. Frontend

```bash
# Root of project
npm start                 # Starts on http://localhost:3000
```

---

## 📁 Project Structure

```
agriconnect/
├── src/              # React frontend
├── server/           # Node.js + Express backend
├── blockchain/       # Solidity smart contracts (Part B)
├── ai/               # Python AI + Streamlit dashboard (Part D)
└── docs/             # Data classification & GDPR spreadsheets
```

---

## 🔑 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18 + Bootstrap 5 |
| Backend | Node.js + Express |
| Database | PostgreSQL 13+ + Sequelize ORM |
| Auth | JWT + bcrypt |
| Blockchain | Solidity + Hardhat (Part B) |
| AI/ML | Python + scikit-learn + Streamlit (Part D) |

---

## 🌐 Pages

| Route | Description | Access |
|-------|-------------|--------|
| `/` | Landing page | Public |
| `/marketplace` | Browse crop listings | Public |
| `/listings/:id` | Listing detail + contact | Public |
| `/prices` | Market price charts | Public |
| `/weather` | Weather & alerts | Public |
| `/tips` | Farming advice | Public |
| `/listings/new` | Post a listing | Auth |
| `/messages` | Buyer-seller chat | Auth |
| `/dashboard` | User dashboard | Auth |
| `/admin` | Admin panel + security | Admin |

---

## 🔐 RBAC Roles

| Role | Capabilities |
|------|-------------|
| `farmer` | List/browse crops, message, buy |
| `buyer` | Browse crops, message, list |
| `advisor` | All above + post farming tips |
| `admin` | Full access + user management + security config |
