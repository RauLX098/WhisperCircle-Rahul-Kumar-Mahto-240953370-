# WhisperCircle

**Anonymous Talking Club and Discussion Platform**

WhisperCircle is a full-stack web application for topic-based group conversations and private one-to-one chats using pseudonymous guest identities. Users can choose or generate a nickname, explore discussion rooms, chat in real time, share anonymous confessions, and use safety tools such as reporting and blocking.

## Features

- Pseudonymous guest identity with a chosen or generated nickname.
- Six topic-based clubs: College Life, Confessions, Friends & Feelings, Gaming Zone, Music Lounge, and Anything Goes.
- Real-time group chat with recent room history.
- Live online member list.
- Private one-to-one conversations.
- Anonymous confessions.
- Message reporting and user blocking.
- A basic moderation queue for reviewing or dismissing reports.
- Responsive desktop and mobile interface.

## Technology stack

| Part | Technologies |
|---|---|
| Frontend | React 18, Vite, CSS, lucide-react |
| Backend | Node.js, Express |
| Real-time communication | Socket.IO |
| Database | MongoDB, Mongoose |
| Security and validation | Helmet, CORS, express-rate-limit, Zod, input sanitisation |
| Testing | Node.js test runner, Playwright |
| Version control | Git and GitHub |

## Project structure

```text
WhisperCircle/
├── client/                 # React + Vite frontend
├── server/                 # Express + Socket.IO backend
├── PROJECT_REPORT_TEMPLATE.md
├── .gitignore
└── README.md
```

## Requirements

- Node.js 20 or newer recommended
- npm
- MongoDB (optional for local demonstration; an in-memory fallback is available)

## Run locally

The frontend and backend run separately.

### 1. Backend

```bash
cd server
npm install
```

Copy `.env.example` to `.env` and configure `MONGODB_URI` if using MongoDB. Then run:

```bash
npm run dev
```

The backend normally runs at `http://localhost:4000`.

### 2. Frontend

Open a second terminal from the project root:

```bash
cd client
npm install
npm run dev
```

Open the local URL printed by Vite, normally `http://localhost:5173`.

### 3. MongoDB (optional)

Add your MongoDB connection string to `server/.env`:

```env
MONGODB_URI=your_mongodb_connection_string
```

Do not publish `.env` files, passwords, API keys, or database credentials. Without MongoDB configuration, the application uses temporary in-memory storage, which is cleared when the server restarts.

## Tests

From the `server` directory, run:

```bash
npm test
```

The project report records 12 passing backend tests and 34 passing end-to-end checks for the tested version.

## Try the application

1. Open the application in two separate browser profiles or one normal and one private window.
2. Enter different guest nicknames.
3. Join the same room from both sessions.
4. Exchange group messages.
5. Select an online member to start a private chat.
6. Try the report and block options.
7. Explore the confessions area and demo moderation queue.

## Privacy and safety

WhisperCircle provides **pseudonymous public identities, not guaranteed anonymity**. The server handles technical connection information. The moderation queue is a classroom demonstration, not a production moderation system.

Before public deployment, add appropriate moderator authentication, privacy notices, data-retention controls, stronger abuse prevention, and production-grade configuration. Do not collect sensitive personal information through this educational project.

## Team members

| Name | Registration number | Roll number |
|---|---:|---:|
| **Rahul Kumar Mahto** | **240953370** | 56 |
| **Akshith K** | **240953290** | 58 |

Both team members contributed to the project across frontend development, backend services, real-time communication, data storage, integration, testing, and documentation.

## Project report

The accompanying project report documents the problem statement, objectives, system design, technology stack, feature descriptions, database design, screenshots, testing summary, team details, limitations, and conclusion.

## GitHub repository

[WhisperCircle](https://github.com/RaulX098/WhisperCircle)

---

**WhisperCircle – Anonymous Talking Club and Discussion Platform**
