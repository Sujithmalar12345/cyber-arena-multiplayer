# cyber-arena-multiplayer
# Cyber Arena

A real-time 2-player multiplayer browser game using React, Node.js, Express and Socket.IO.

## Local development

### Server
cd server
npm install
npm start

### Client
cd client
npm install
npm run dev

Set `VITE_SERVER_URL` in the client production environment to the deployed server URL.

## Render deployment

Deploy the `server` directory as a Node Web Service:
- Build command: `npm install`
- Start command: `npm start`
- Environment variable: `CLIENT_URL=https://YOUR-FRONTEND-URL`

Deploy the `client` directory as a Static Site:
- Build command: `npm install && npm run build`
- Publish directory: `dist`
- Environment variable: `VITE_SERVER_URL=https://YOUR-SERVER-URL`

After both services are deployed, open the frontend URL on two devices and test Create Arena + Join Arena.
