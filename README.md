# Node.js Demo App - CI/CD Pipeline with GitHub Actions

## 📌 Project Overview

This project demonstrates a complete **CI/CD pipeline** using **GitHub Actions** for a sample Node.js application. It includes building, testing, and (optionally) deploying a Dockerized Node.js app to DockerHub.

## ✅ Objectives

- Automate code deployment using GitHub Actions.
- Set up a `.github/workflows/main.yml` CI/CD workflow.
- Build and optionally push Docker image.
- Learn the fundamentals of DevOps automation.

---

## 🔧 Tools & Technologies Used

- **GitHub & GitHub Actions**
- **Node.js**
- **Docker (optional)**
- **YAML**

---

## 🛠 Pipeline Steps

### Trigger
- The workflow is triggered on `push` events to the `main` branch.

### Jobs
1. **Setup**
   - Use Ubuntu runner.
   - Checkout the code.

2. **Install**
   - Install Node.js version 18.x.
   - Install dependencies using `npm ci`.

3. **Test**
   - Run `npm test` to ensure the code passes all tests.

4. **Build (Optional)**
   - Build Docker image (if Dockerfile is available).
   - Tag the image appropriately.

5. **Push (Optional)**
   - Login to DockerHub using secrets.
   - Push the built image to DockerHub.

---

## 📂 Project Structure

github/
│ └── workflows/
│ └── main.yml # GitHub Actions workflow
├── app.js # Sample app code
├── package.json # Node.js project file
├── Dockerfile # Docker instructions (optional)
└── README.md # Project documentation
## How TO Run Locally 
git clone https://github.com/yourusername/nodejs-demo-app.git
cd nodejs-demo-app
npm install
npm test

