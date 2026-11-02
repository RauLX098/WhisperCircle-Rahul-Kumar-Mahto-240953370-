# WhisperCircle

**Anonymous Talking Club and Discussion Platform**

WhisperCircle is a full-stack web application that lets people join topic-based group conversations and private one-to-one chats using pseudonymous guest identities. Users can choose or generate a nickname, explore discussion rooms, chat in real time, share anonymous confessions, and use basic safety tools such as reporting and blocking.

## Features

1. **Pseudonymous guest identity** – Join without creating an account and choose or generate a nickname.
2. **Topic-based discussion rooms** – Browse six clubs: College Life, Confessions, Friends & Feelings, Gaming Zone, Music Lounge, and Anything Goes.
3. **Real-time group chat** – Send messages instantly and view recent room history.
4. **Online member list** – See who is currently present in a discussion room.
5. **Private one-to-one chat** – Start a private conversation with another online member.
6. **Anonymous confessions** – Share thoughts in a dedicated space without displaying the author's nickname.
7. **Report and block** – Report messages with a reason and block private messages from a user.
8. **Moderation queue** – Review or dismiss submitted reports.
9. **Responsive interface** – Use the application on desktop and mobile screens.

## Technology stack

| Part | Technologies |
|---|---|
| Frontend | React 18, Vite, CSS, lucide-react |
| Backend | Node.js, Express |
| Real-time communication | Socket.IO |
| Database | MongoDB, Mongoose |
| Security and validation | Helmet, CORS, express-rate-limit, Zod, input sanitisation |
| Testing | Node.js test runner, Playwright end-to-end tests |
| Version control | Git and GitHub |

## Project structure

```text
WhisperCircle/
├── client/                 # React + Vite frontend
│   ├── src/
│   ├── index.html
│   └── package.json
├── server/                 # Express + Socket.IO backend
│   ├── src/
│   ├── tests/
│   ├── .env.example
│   └── package.json
├── PROJECT_REPORT_TEMPLATE.md
├── .gitignore
└── README.md
```

## Requirements

- Node.js 20 or newer recommended
- npm
- MongoDB (optional for local demonstration; the server has an in-memory fallback)

## Run the project locally

The frontend and backend run in separate terminals.

### 1. Start the backend

```bash
cd server
npm install
```

Copy `.env.example` to `.env`, then start the backend:

```bash
npm run dev
```

The backend normally runs at `http://localhost:4000`.

### 2. Start the frontend

Open a second terminal from the project root:

```bash
cd client
npm install
npm run dev
```

Open the local URL printed by Vite, normally `http://localhost:5173`.

### 3. Optional MongoDB setup

To use persistent storage, add your MongoDB connection string to `server/.env`:

```env
MONGODB_URI=your_mongodb_connection_string
```

Keep real credentials private. Do not commit `.env` or publish database passwords. If MongoDB is not configured, the application uses temporary in-memory storage; that data is cleared when the server restarts.

## Run backend tests

From the `server` directory:

```bash
npm test
```

The project report records 12 passing backend tests and 34 passing end-to-end checks for the tested project version. Run the tests yourself before making claims about the current state of your copy.

## Try the application

1. Open the application in two separate browser profiles or one normal and one incognito window.
2. Enter different guest nicknames.
3. Join the same room from both browser sessions.
4. Send group messages and confirm that they appear in both sessions.
5. Select another online member to start a private chat.
6. Try the report and block options.
7. Open the confessions area and the demo moderation queue.

## Privacy and safety notes

WhisperCircle provides **pseudonymous public identities, not guaranteed anonymity**. The server handles technical connection information. The moderation queue is a classroom demonstration, not a production moderation system. Before public deployment, add appropriate authentication and moderator permissions, privacy notices, data-retention controls, stronger abuse prevention, and production-grade configuration.

Do not use this educational project to collect sensitive personal information. Never publish passwords, API keys, or database credentials.

## Team members

| Name | Registration number | Roll number |
|---|---:|---:|
| **Rahul Kumar Mahto** | **240953370** | 56 |
| **Akshith K** | **240953290** | 58 |

**Registration numbers are shown prominently as the primary student identifiers.** Both team members contribute to integration, testing, documentation, screenshots, and the final presentation. Update the division of work below to reflect the tasks each member actually completed.

### Division of work

- **Rahul Kumar Mahto** – Frontend implementation and user-interface work (confirm this allocation).
- **Akshith K** – Backend, real-time communication, data storage, and server-side features (confirm this allocation).
- **Both members** – Integration, testing, documentation, screenshots, and presentation.

> Please verify the individual task allocation with both team members before submitting the report.

## Project report

The accompanying project report contains the problem statement, objectives, system design, technology stack, feature descriptions, database design, screenshots, testing summary, division of work, limitations, and conclusion.

## GitHub repository

Repository: [WhisperCircle](https://github.com/RaulX098/WhisperCircle)

---
**WhisperCircle – Anonymous Talking Club and Discussion Platform**
