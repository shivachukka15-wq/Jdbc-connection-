# Student App: Java MVC backend + Node.js frontend

- `backend/`: Spring Boot (Model, Repository, Controller REST API) + database (H2 default, MySQL optional)
- `frontend/`: Node.js + Express server serving the HTML/JS view and proxying `/api` to the backend

## Run (two terminals)

Backend (Java 17+, Maven), runs on port 8080:

    cd backend
    mvn spring-boot:run

Frontend (Node 18+), runs on port 3000:

    cd frontend
    npm install
    npm start

Open http://localhost:3000

To point the frontend at another backend: `BACKEND_URL=http://host:8080 npm start`

## Use MySQL
1. `CREATE DATABASE studentdb;`
2. In `backend/src/main/resources/application.properties`, comment the H2 block and uncomment the MySQL block.
3. Set `DB_PASSWORD` as an environment variable.

## Upload to GitHub

    git init
    git add .
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/USER/REPO.git
    git push -u origin main
