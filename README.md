# 🍽️ Restaurant Reservation System — MERN Stack

A full-stack restaurant reservation web app built with **MongoDB**, **Express.js**, **React** (Vite), and **Node.js**.

> Built by **mayankgupta8448**

---

## 📋 Prerequisites

- **Node.js** v18+ — [Download](https://nodejs.org/)
- **MongoDB** — Local install ([Download](https://www.mongodb.com/try/download/community)) or [MongoDB Atlas](https://www.mongodb.com/atlas) (cloud)
- **Git** — [Download](https://git-scm.com/)

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/mayankgupta8448/MERN_STACK_RESTAURANT_RESERVATION.git
cd MERN_STACK_RESTAURANT_RESERVATION
```

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` directory:

```env
PORT=7700
FRONTEND_URL=http://localhost:3000
MONGO_URI=mongodb://localhost:27017/RESERVATIONS
```

> 💡 If using MongoDB Atlas, replace `MONGO_URI` with your Atlas connection string.

Start the backend server:

```bash
npm run dev
```

The backend will start on **http://localhost:7700**.

### 3. Frontend Setup

Open a **new terminal** window:

```bash
cd frontend
npm install
```

Create a `.env` file in the `frontend/` directory:

```env
VITE_BACKEND_URL=http://localhost:7700
```

Start the frontend dev server:

```bash
npm run dev
```

The frontend will start on **http://localhost:3000**.

### 4. Open the App

Visit **http://localhost:3000** in your browser.

---

## 📁 Project Structure

```
MERN_STACK_RESTAURANT_RESERVATION/
├── backend/
│   ├── controller/        # Route handlers (reservation logic)
│   ├── database/          # MongoDB connection setup
│   ├── middlewares/        # Error handling middleware
│   ├── models/            # Mongoose schemas
│   ├── routes/            # Express route definitions
│   ├── app.js             # Express app configuration
│   ├── server.js          # Server entry point
│   ├── .env               # Backend environment variables
│   └── package.json
├── frontend/
│   ├── public/            # Static assets (images, SVGs)
│   ├── src/
│   │   ├── components/    # React components (Navbar, Footer, etc.)
│   │   ├── Pages/         # Page components (Home, Success, NotFound)
│   │   ├── App.jsx        # Root component with routing
│   │   ├── App.css        # Global styles
│   │   ├── main.jsx       # React entry point
│   │   └── restApi.json   # Static data for menu, team, etc.
│   ├── index.html         # HTML entry point
│   ├── vite.config.js     # Vite configuration
│   ├── .env               # Frontend environment variables
│   └── package.json
├── .gitignore
└── README.md
```

---

## 🔧 API Endpoints

| Method | Endpoint                    | Description              |
| ------ | --------------------------- | ------------------------ |
| GET    | `/`                         | Health check             |
| POST   | `/api/v1/reservation/send`  | Create a new reservation |

### Request Body (POST `/api/v1/reservation/send`)

```json
{
  "firstName": "Mayank",
  "lastName": "Gupta",
  "email": "mayank@example.com",
  "phone": "9876543210",
  "date": "2026-05-10",
  "time": "19:00"
}
```

---

## 🛠️ Tech Stack

| Layer    | Technology         |
| -------- | ------------------ |
| Frontend | React 18 + Vite    |
| Backend  | Express.js + Node  |
| Database | MongoDB + Mongoose |
| Styling  | Vanilla CSS        |

---

## 📝 Environment Variables

### Backend (`backend/.env`)

| Variable       | Description                        | Default                                    |
| -------------- | ---------------------------------- | ------------------------------------------ |
| `PORT`         | Backend server port                | `7700`                                     |
| `FRONTEND_URL` | Allowed CORS origin                | `http://localhost:3000`                     |
| `MONGO_URI`    | MongoDB connection string          | `mongodb://localhost:27017/RESERVATIONS`    |

### Frontend (`frontend/.env`)

| Variable           | Description         | Default                    |
| ------------------ | ------------------- | -------------------------- |
| `VITE_BACKEND_URL` | Backend API base URL | `http://localhost:7700`    |

---

## 📄 License

This project is open source and available under the [ISC License](https://opensource.org/licenses/ISC).

---

Made with ❤️ by **mayankgupta8448**
