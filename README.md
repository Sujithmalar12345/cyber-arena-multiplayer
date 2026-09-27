# ⚡ Cyber Arena — Real-Time Multiplayer Game

Cyber Arena is a real-time 2-player multiplayer browser game built with React, Node.js, Express, and Socket.IO. Players can create or join a private arena using a room code and battle each other from separate devices in real time.

## 🛠️ Technology Stack

* **Frontend:** React + Vite
* **Backend:** Node.js + Express
* **Real-Time Communication:** Socket.IO
* **Language:** JavaScript
* **Styling:** CSS
* **Version Control:** Git + GitHub
* **Deployment:** Render

---

# 🚀 Local Setup

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/cyber-arena-multiplayer.git
cd cyber-arena-multiplayer
```

Replace `YOUR-USERNAME` with your GitHub username.

## 2. Setup the Backend

Open a terminal:

```bash
cd server
npm install
npm start
```

The server will start on:

```text
http://localhost:3000
```

You can verify the server using:

```text
http://localhost:3000/health
```

A successful response should look similar to:

```json
{
  "ok": true,
  "game": "Cyber Arena"
}
```

## 3. Setup the Frontend

Open a **new terminal** while keeping the backend running:

```bash
cd client
npm install
npm run dev
```

Vite will provide a local URL similar to:

```text
http://localhost:5173
```

Open that URL in your browser.

---

# 🎮 Local Multiplayer Testing

Open the game in two separate browsers.

### Player 1

1. Open the game.
2. Enter a nickname.
3. Click **Create Arena**.
4. Copy the generated room code.

### Player 2

1. Open the game in another browser.
2. Enter a nickname.
3. Click **Join Arena**.
4. Enter the room code.

Both players should now be connected to the same game.

Test:

* Attack
* Power Attack
* Defend
* Charge
* Turn switching
* HP updates
* Energy updates
* Victory/defeat
* Play Again
* Disconnect handling

---

# 🌐 Production Deployment

Cyber Arena can be deployed using **Render**.

The project contains two services:

```text
GitHub Repository
       │
       ├── client → Render Static Site
       │
       └── server → Render Web Service
```

## 1. Deploy the Backend

Create a new **Web Service** on Render and connect the GitHub repository.

Set the root directory to:

```text
server
```

Build Command:

```bash
npm install
```

Start Command:

```bash
npm start
```

Add the environment variable:

```text
CLIENT_URL=https://YOUR-FRONTEND-URL
```

After deployment, Render will provide a backend URL similar to:

```text
https://cyber-arena-server.onrender.com
```

Test:

```text
https://cyber-arena-server.onrender.com/health
```

---

# 2. Deploy the Frontend

Create a **Static Site** on Render using the same GitHub repository.

Set the root directory to:

```text
client
```

Build Command:

```bash
npm install && npm run build
```

Publish Directory:

```text
dist
```

Add this environment variable:

```text
VITE_SERVER_URL=https://YOUR-BACKEND-URL
```

Example:

```text
VITE_SERVER_URL=https://cyber-arena-server.onrender.com
```

Deploy the frontend.

Render will provide a public URL similar to:

```text
https://cyber-arena.onrender.com
```

---

# 🔗 Production Multiplayer Test

After deployment, open the frontend URL on two separate devices.

### Device 1

```text
Open the public URL
        ↓
Create Arena
        ↓
Copy Room Code
```

### Device 2

```text
Open the same public URL
        ↓
Join Arena
        ↓
Enter Room Code
```

Both players should be able to play the game in real time.

---

# 🔄 Updating the Deployed Game

After making changes:

```bash
git add .
git commit -m "Update Cyber Arena"
git push origin main
```

Render can automatically deploy the latest changes from GitHub when automatic deployment is enabled.

---

# ⚠️ Important Deployment Notes

* Never commit `.env` files containing secrets.
* Keep `node_modules` out of GitHub.
* Make sure `VITE_SERVER_URL` points to the production backend.
* Make sure `CLIENT_URL` points to the production frontend.
* The backend must support WebSocket/Socket.IO connections.
* Test the production game from two different devices after deployment.

---

# 📌 Project Structure

```text
cyber-arena-multiplayer/
│
├── client/
│   ├── src/
│   ├── index.html
│   ├── package.json
│   └── ...
│
├── server/
│   ├── server.js
│   ├── package.json
│   └── ...
│
├── .gitignore
└── README.md
```

## 🎯 Project Goal

Cyber Arena demonstrates full-stack web development, real-time multiplayer communication, server-side game validation, responsive UI design, Git/GitHub workflow, and cloud deployment.
