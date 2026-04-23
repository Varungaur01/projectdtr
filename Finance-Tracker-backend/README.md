# TreasureTrack — Personal Finance Tracker (Backend)

A Node.js + Express.js REST API for managing user authentication and expense tracking, with MongoDB as the database.

---

## Prerequisites (Install These First)

| Software | Version | Download Link |
|----------|---------|---------------|
| **Node.js** | v18 or above | [https://nodejs.org](https://nodejs.org) |
| **MongoDB** | v6 or above | [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community) |
| **Git** | Any | [https://git-scm.com](https://git-scm.com) |

### Quick Install (Windows - using winget)

```bash
winget install OpenJS.NodeJS
winget install MongoDB.Server
winget install Git.Git
```

---

## Getting Started

### Step 1: Clone the Repository

```bash
git clone https://github.com/Varunkumar0812/Finance-Tracker-backend.git
cd Finance-Tracker-backend
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Create the Environment File

Create a file named `config.env` in the root of the project and add the following:

```env
NODE_ENV=development
PORT=5000

DATABASE=mongodb://localhost:27017/finance-tracker
DATABASE_PASSWORD=

JWT_SECRET=your_secret_key_here
JWT_EXPIRES_IN=90d
JWT_COOKIE_EXPIRES_IN=90
```

> **Note:** Replace `your_secret_key_here` with any random long string (e.g., `myapp_secret_2024_xyz`).  
> If using MongoDB Atlas (cloud) instead of local MongoDB, replace the `DATABASE` value with your Atlas connection string.

### Step 4: Start MongoDB Service

Make sure MongoDB is running before starting the server:

**Windows:**
```bash
net start MongoDB
```

**macOS/Linux:**
```bash
sudo systemctl start mongod
```

### Step 5: Start the Backend Server

```bash
npm start
```

You should see:
```
Server is running...
DB connected successfully !!
```

The backend will run on **http://localhost:5000**

---

## API Endpoints

### User Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/users/signup` | Register a new user |
| POST | `/api/users/signin` | Login and get JWT token |

### Expense Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/expenses/` | Get all expenses for a user |
| POST | `/api/expenses` | Create a new expense |
| GET | `/api/expenses/:id` | Get a specific expense |
| PATCH | `/api/expenses/:id` | Update a specific expense |
| DELETE | `/api/expenses/:id` | Delete a specific expense |

---

## Tech Stack

- **Runtime:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB + Mongoose
- **Auth:** JWT (JSON Web Tokens)
- **Password Hashing:** bcrypt
- **Validation:** validator.js

---

## Frontend Repository

👉 [Finance-Tracker-frontend](https://github.com/Varunkumar0812/Finance-Tracker-frontend)

---

## License

MIT License
