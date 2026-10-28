# Quickfire Quiz

Real-time room-code quiz for 2–8 players. The included Windows launcher uses the Node.js runtime bundled with Codex; no npm install is needed.

## Start and verify on Windows

1. Download and extract QuickfireQuiz-Windows.zip.
2. Open the extracted quickfire-quiz folder.
3. Double-click Start Quickfire Quiz.bat. A black console window opens.
4. Wait until it prints: Quickfire Quiz ready at http://localhost:3000/
5. In Chrome or Edge on this same computer, open http://localhost:3000/api/health. A small response containing "ok":true confirms the server is responding.
6. Open http://localhost:3000 to play. Keep the console window open for the whole game.

If the console says the address is already in use, close any other Quickfire server window and double-click the launcher again. If the console says it cannot find Node.js, keep the window open and share the message so we can adjust the launcher.

Players on the same Wi-Fi can join using the host computer’s local network address and port 3000. For players outside that network, deploy this folder to a Node.js host and share its HTTPS address. Rooms are held in memory and disappear when the server stops.

Three rounds of five mixed-topic questions. Each question has four choices and a shared 20-second timer. The first answer locks. Correct answers earn 1,000 points plus a speed bonus of floor(500 × remaining time ÷ 20), calculated using server receipt time. Incorrect or unanswered questions earn zero. Scores update after each question; tied final scores share place.
