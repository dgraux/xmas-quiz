# Xmas Trivia Quiz

Static web app (no server). Players connect peer-to-peer (WebRTC via PeerJS public broker); the host browser is the game server.

## Deploy (GitHub Pages)
1. Create a repo, add `index.html` and `questions.js` at the root.
2. Settings > Pages > Deploy from branch `main` / root.
3. Host opens `https://<user>.github.io/<repo>/?host` (or clicks the small "Host a game" link on the landing page), sets options, clicks **Create room**.
4. Share the displayed link (`...?room=ABCD`) on Google Meet. Up to 30 players (`MAXP` in `index.html`).

## Notes
- Keep the host tab open and in the foreground for the whole game.
- 200 questions: 72 tech/AI, 65 fun/festive, 63 ecology. Edit `questions.js` (correct answer is always first; choices are shuffled at runtime).
- Scoring: 500-1000 points per correct answer depending on speed. Top 5 shown after every question.
- Corporate networks that block WebRTC may stop some players from connecting.
