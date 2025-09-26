# Node.js CI/CD Demo App

This repository demonstrates a simple **Node.js app** with a **CI/CD pipeline** using GitHub Actions and Docker.

---

## Project Structure

- `index.js` – Node.js Express app
- `package.json` – Node.js dependencies
- `Dockerfile` – Docker image build instructions
- `.github/workflows/main.yml` – GitHub Actions workflow

---

## Run Locally

1. Clone the repository:
bash
git clone <repo-url>
cd nodejs-demo-app
Install dependencies:

bash

npm install
Build the Docker image:

bash

docker build -t nodejs-demo-app:latest .
Run the Docker container:

bash

docker run -p 3000:3000 nodejs-demo-app:latest
Open a browser and visit:

arduino

http://localhost:3000
CI/CD Pipeline
Triggered on push to main branch

Workflow steps:

Checkout code

Setup Node.js

Install dependencies

Run tests

Build Docker image

Login to DockerHub using secret token

Push Docker image

Notes
Dockerfile must be named exactly Dockerfile (no .txt)

Use GitHub Secrets for storing tokens; do not put them in code


