# ClassBuzz - Classroom Management Platform

ClassBuzz is a beautiful, interactive, and modern classroom management platform designed to connect teachers and students in real time. It facilitates streamlined communication, interactive polls, collaborative Q&A (doubts), deadline tracking, resource sharing, feedback loops, and gamified engagement with badges and leaderboards.

---

## 🚀 Key Features

*   📣 **Smart Announcements**: Post targeted class announcements with pins and real-time updates.
*   📊 **Interactive Live Polls**: Create classroom polls and visualize responses with live charts.
*   🙋‍♂️ **Kanban Doubt Board**: Organize student doubts into a Kanban board (Open, In Progress, Resolved) with nested comments and threaded replies.
*   📅 **Deadline Tracking**: View and manage upcoming class deadlines (assignments, tests, events) via lists or a calendar view with live countdown chips.
*   🏆 **Gamification & Badges**: Boost student engagement with achievements, leaderboard rankings, and custom badges.
*   📂 **Resource Library**: Upload, download, and organize files in a folder-based system.
*   💬 **Feedback Portal**: Facilitate structured feedback channels between students and teachers.

---

## 🛠️ Technology Stack

### Frontend
*   **Framework**: [React](https://react.dev/) (v18) with [Vite](https://vitejs.dev/)
*   **Language**: [TypeScript](https://www.typescriptlang.org/)
*   **Styling**: [TailwindCSS](https://tailwindcss.com/) & [Shadcn UI](https://ui.shadcn.com/)
*   **Animations**: [Framer Motion](https://www.framer.com/motion/)
*   **State & Fetching**: [TanStack Query (React Query)](https://tanstack.com/query/latest) & [React Router Dom](https://reactrouter.com/)
*   **Charts**: [Recharts](https://recharts.org/)

### Backend
*   **Runtime/Framework**: [Node.js](https://nodejs.org/) with [Express](https://expressjs.com/)
*   **Language**: [TypeScript](https://www.typescriptlang.org/)
*   **Database**: [MongoDB](https://www.mongodb.com/) via [Mongoose](https://mongoosejs.com/)
*   **Authentication**: [JSON Web Tokens (JWT)](https://jwt.io/) & [Bcrypt](https://github.com/kelektiv/node.bcrypt.js)
*   **File Uploads**: [Multer](https://github.com/expressjs/multer)

---

## 📁 Project Structure

```text
ClassBuzz-Classroom-Management-Platform/
├── backend/                  # Express API Server
│   ├── src/
│   │   ├── config/          # Database connection
│   │   ├── controllers/     # API request handlers
│   │   ├── middleware/      # JWT Authentication & file upload middlewares
│   │   ├── models/          # Mongoose schemas (User, Doubt, Poll, Badge, etc.)
│   │   ├── routes/          # Express API route endpoints
│   │   └── index.ts         # Server entrypoint
│   ├── tsconfig.json
│   └── package.json
│
├── src/                      # React Frontend Application
│   ├── components/          # Reusable UI components (ui/, DoubtCard, PollCard, etc.)
│   ├── contexts/            # Context providers (AuthContext, etc.)
│   ├── data/                # Mock/Static metadata
│   ├── hooks/               # Custom React hooks
│   ├── lib/                 # Utility libraries and API clients (api.ts)
│   ├── pages/               # Page components (Landing, Dashboards, Polls, etc.)
│   ├── types/               # TypeScript interfaces
│   ├── App.tsx              # Router & layout setup
│   └── main.tsx             # Frontend entrypoint
│
├── public/                   # Static assets
├── tailwind.config.ts        # Tailwind styling configurations
├── vite.config.ts            # Vite bundler configurations
└── package.json
```

---

## ⚙️ Getting Started

### Prerequisites
*   [Node.js](https://nodejs.org/) (v18+ recommended)
*   [MongoDB](https://www.mongodb.com/) (Local Community Server or MongoDB Atlas cluster)
*   [npm](https://www.npmjs.com/) or [bun](https://bun.sh/) package manager

---

### 1. Backend Setup

1.  Navigate into the `backend` directory:
    ```bash
    cd backend
    ```
2.  Install dependencies:
    ```bash
    npm install
    # or
    bun install
    ```
3.  Create a `.env` file in the `backend/` directory and add the following:
    ```env
    PORT=5000
    MONGODB_URI=mongodb://localhost:27017/classbuzz
    JWT_SECRET=your_super_secret_jwt_key
    FRONTEND_URL=http://localhost:5173
    ```
4.  Start the backend development server:
    ```bash
    npm run dev
    # or
    bun run dev
    ```
    *The server will run on [http://localhost:5000](http://localhost:5000)*

---

### 2. Frontend Setup

1.  Navigate to the project root directory:
    ```bash
    cd ..
    ```
2.  Install frontend dependencies:
    ```bash
    npm install
    # or
    bun install
    ```
3.  Create a `.env` file in the root directory (optional, as it defaults to backend's local port):
    ```env
    VITE_API_URL=http://localhost:5000/api
    ```
4.  Start the frontend development server:
    ```bash
    npm run dev
    # or
    bun dev
    ```
    *The frontend will run on [http://localhost:5173](http://localhost:5173)*

---

## 🔑 Default Roles & Accounts

You can register new student and teacher accounts directly from the UI register tab. 

*   **Teacher Role**: Permissions to create classrooms, publish announcements, design interactive live polls, award badges, and manage doubts.
*   **Student Role**: Permissions to join classrooms, respond to announcements & polls, raise/reply to doubts, view deadline countdowns, download resource files, and track badges.

---

## 🧪 Running Tests

### Frontend Testing
To run unit and integration tests for the frontend:
```bash
npm run test
# or
bun test
```
To run tests in watch mode:
```bash
npm run test:watch
```
