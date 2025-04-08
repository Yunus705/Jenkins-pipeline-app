# Jenkins CI/CD Pipeline Node.js App

This project demonstrates a simple Node.js application deployed using Docker and automated through a Jenkins CI/CD pipeline.

---

## 📌 What is this Project?

A basic Express.js app built and run inside a Docker container. The CI/CD process is managed using Jenkins, which automates:
- Building the Docker image
- (Optional) Testing
- Running the Docker container

---

## ⚙️ How CI/CD is Configured?

Jenkins uses a declarative pipeline (`Jenkinsfile`) with the following stages:

### ✅ Pipeline Stages:
- **Build**: Docker image is built using the Dockerfile.
- **Test**: (Optional placeholder step).
- **Deploy**: Docker container is launched on a specified port.

### 🕒 Build Trigger:
- CI/CD is triggered using **Poll SCM**
- Jenkins checks GitHub repo every 5 minutes for any changes using this cron expression:
   H/5 * * * *

> If any changes are found (commits/pushes), Jenkins triggers a new pipeline build automatically.

---

## 🧰 Technologies Used

- **Node.js** (Express)
- **Docker**
- **Jenkins**
- **GitHub**

---

## 🖥️ How to Run Locally

1. **Clone the Repository**

git clone https://github.com/your-username/jenkins-pipeline-app.git
cd jenkins-pipeline-app

Build the Docker Image:
docker build -t jenkins-app .

Run the Container:
docker run -d -p 9000:3000 jenkins-app

Open in Browser:
Visit: http://localhost:9000
You will see:
Hello from Yunus Sharif