# TreasureTrack — Personal Finance Tracker (Frontend)

A React.js web application for tracking personal finances — expenses, credits, debits, and monthly income with a calendar view.

---

## Prerequisites (Install These First)

| Software | Version | Download Link |
|----------|---------|---------------|
| **Node.js** | v18 or above | [https://nodejs.org](https://nodejs.org) |
| **Git** | Any | [https://git-scm.com](https://git-scm.com) |

> **Important:** The backend server must be running before using the frontend.  
> 👉 [Backend Setup Instructions](https://github.com/Varunkumar0812/Finance-Tracker-backend)

---

## Getting Started

### Step 1: Clone the Repository

```bash
git clone https://github.com/Varunkumar0812/Finance-Tracker-frontend.git
cd Finance-Tracker-frontend
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Start the Frontend

```bash
npm start
```

The app will open automatically in your browser at **http://localhost:3000**

---

## Running the Full Project (Frontend + Backend)

You need **two terminals running simultaneously**:

### Terminal 1 — Backend

```bash
cd Finance-Tracker-backend
npm install
# Create config.env (see backend README)
npm start
# → Runs on http://localhost:5000
```

### Terminal 2 — Frontend

```bash
cd Finance-Tracker-frontend
npm install
npm start
# → Runs on http://localhost:3000
```

### Summary

| Service | Port | Command |
|---------|------|---------|
| MongoDB | 27017 | `net start MongoDB` (Windows) |
| Backend (Express) | 5000 | `npm start` inside `Finance-Tracker-backend/` |
| Frontend (React) | 3000 | `npm start` inside `Finance-Tracker-frontend/` |

---

## Features

- 🔐 **User Authentication** — Sign up & Sign in with JWT
- 📊 **Dashboard** — Overview of expenses and income
- 💳 **Expense Tracking** — Add, view credit/debit transactions
- 📅 **Calendar View** — See expenses on a monthly calendar
- 📱 **Responsive Design** — Works on desktop and mobile

---

## Tech Stack

- **Framework:** React 18
- **Routing:** React Router v6
- **HTTP Client:** Axios
- **Calendar:** FullCalendar
- **Styling:** Tailwind CSS
- **Icons:** React Icons

---

## Backend Configuration (config.env)

The backend requires a `config.env` file in the `Finance-Tracker-backend/` root:

```env
NODE_ENV=development
PORT=5000

DATABASE=mongodb://localhost:27017/finance-tracker
DATABASE_PASSWORD=

JWT_SECRET=your_secret_key_here
JWT_EXPIRES_IN=90d
JWT_COOKIE_EXPIRES_IN=90
```

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| `option expires is invalid` | Make sure `JWT_COOKIE_EXPIRES_IN=90` is in your `config.env` |
| `ECONNREFUSED localhost:5000` | Start the backend server first (`npm start` in backend folder) |
| `mongod not recognized` | Install MongoDB and make sure the service is running |
| `E11000 duplicate key error` | A user with that email already exists — use a different email or login |

---

## License

MIT License
