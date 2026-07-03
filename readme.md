Readme · MD<div align="center">
🪨 Cairn

An online judge / coding platform — submit code for a problem, get it compiled and run remotely, and find out if it's correct.

MERN-based, with Docker sandboxing underneath.

MongoDB · Express · React · Node.js · Docker · Redis

</div>

📌 What it does

You write a solution, submit it, and the platform compiles and runs your code in a secure, sandboxed environment before judging it right or wrong. Every user gets a history of their submissions and a leaderboard to see how they stack up. Multiple submissions at once are handled through a polling + queue system instead of running everything synchronously, so the server doesn't choke under load.


✨ Core features


Remote, secure code compilation and execution for submitted solutions
Docker-based sandboxing so untrusted code can't touch the host system
Submission history per user
Leaderboard tracking
Polling and a queue system to handle multiple simultaneous submissions



🚀 Running it locally

Client

bashcd client
npm install
npm start

Runs on port 3000.

Server

You'll need Docker and Redis (v2.8.18 or higher) installed.


Windows: use WSL for redis-server, and Docker Desktop for Docker.
Database: MongoDB, either local or Atlas.

Using Atlas → add a .env file with DB_URL set to your Atlas connection string.
Using local MongoDB → no DB_URL needed.



Auth: the server uses cookie-based auth with JWT — add JWT_SECRET to the same .env file.


Once that's set up:

bashcd server
npm install
npm start

Runs on port 5000.


<div align="center">


</div>