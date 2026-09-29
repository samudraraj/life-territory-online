# Life Territory

A single-file browser game based on Conway's Game of Life with territorial strategy and peer-to-peer online multiplayer.

## What it includes
- Local multiplayer / solo play
- Turn-based simulation with territory capture
- Online matching using PeerJS + WebRTC
- Host and join flow with a shareable room link
- No backend server or database required

## Run it locally
1. Open `index.html` in a browser, or
2. Serve the folder with any static host:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

## Online play
1. Click `Host Online Match`
2. Share the generated room link or room ID
3. The other player clicks `Join Match` and enters the room ID
4. The host is assigned as Player 1 and the joiner as Player 2
5. Turns are locked while the other player acts, and game state syncs directly peer-to-peer

## Deploy to GitHub Pages
1. Push this repository to GitHub
2. In the repository settings, open **Pages**
3. Set the source to **Deploy from a branch**
4. Choose the `main` branch and `/ (root)` folder
5. Save

Your site will be published at:

```text
https://<your-username>.github.io/life-territory-online/
```

## Notes
- This uses PeerJS over browser WebRTC, so the room connection is direct between browsers.
- The app is intentionally self-contained in one HTML file for easy hosting.
- Because it uses browser networking, a direct peer connection can require the browser to allow the site to access the necessary WebRTC features.
