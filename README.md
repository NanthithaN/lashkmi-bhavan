# Lakshmi Bhavan — Ready Orders

Simple real-time app to mark orders ready from a bill counter and display them on a TV screen.

Features
- Admin page for bill counter: `admin.html` — enter order number and optional note
- TV display: `display.html` — shows latest ready orders with large typography
- Real-time transport via Socket.IO

Quick start (Windows / PowerShell)

1. Install dependencies:

```powershell
cd "c:\Users\SNOWFINA\Downloads\lak"
npm install
```

2. Run locally:

```powershell
npm start
# open http://localhost:3000/admin.html for the counter
# open http://localhost:3000/display.html on the TV (use a browser in full-screen)
```

Deployment
- This is a small Node app; deploy to Heroku, Render, Fly, or any VPS. Ensure `PORT` environment variable is exposed.

Customizing
- Replace `public/assets/logo.svg` with the hotel's actual logo.
- Replace `public/sounds/chime.mp3` with a short chime audio file.
- Adjust colors in `public/css/style.css`.

Notes
- The app currently keeps no server-side state; reconnecting displays only new events while the client is online. If persistent history is required, a small database can be added.
