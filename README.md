# Fullstack Docker App

## 📌 Project Overview

This project is a **full-stack application** setup that will later be containerized using Docker and Docker Compose.

It consists of:

* A **React frontend**
* A **Node.js + Express backend**
* A **PostgreSQL database** with persistence

This is **Stage 1 (Mini Project - I)** where we only set up the file and folder structure.

---

## 📂 Folder Structure

```
fullstack-docker-app/
├── backend/
│   ├── app.js              # Express backend code
│   └── package.json        # Backend dependencies
├── frontend/
│   ├── package.json        # Frontend dependencies
│   └── src/
│       └── App.js          # React frontend code
├── db-data/                # Database volume (empty folder)
├── docker-compose.yml      # (Empty for now, to be used later)
├── .env                    # (Empty, for future environment variables)
└── README.md               # Project documentation
```


# Mini Project 3 - Docker Persistence & Debugging

## Features
- Fullstack app (React + Node.js + Postgres) running in Docker.
- Database persistence using Docker volumes.
- Debugging with `docker logs` and `docker exec`.
- Verified stability after stop/start.

## Steps Performed
1. Added volumes to Postgres service in `docker-compose.yml`.
2. Verified persistence using:
   - `docker-compose down` → `docker-compose up`
   - Logs showed: *Skipping initialization*
3. Debugged using:
   - `docker logs backend-1`
   - `docker exec -it db-1 bash`
4. Tested stop/start:
   - `docker-compose stop`
   - `docker-compose start`
   - App still works in browser 