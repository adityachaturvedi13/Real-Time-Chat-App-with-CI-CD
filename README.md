# Real-Time-Chat-App-with-CI-CD
This is a simple, real-time chat application built with Node.js, Express, and Socket.IO. The project also features a complete CI/CD pipeline using GitHub Actions and Docker to automatically build and containerize the application for deployment.

✨ Features
Real-Time Messaging: Instantly send and receive messages without needing to refresh the page.

User List: See a live list of all users currently in the chat room.

Join & Leave Notifications: Get notified when a user joins or leaves the chat.

Simple UI: A clean and intuitive interface for a seamless user experience.

Automated Pipeline: Fully automated build and containerization process with CI/CD.

🛠️ Technologies Used
This project is built with a modern tech stack:

Backend: Node.js, Express

Real-Time Communication: Socket.IO

Frontend: HTML, CSS, Vanilla JavaScript

Containerization: Docker

CI/CD Automation: GitHub Actions

🚀 Getting Started
You can get a copy of this project running on your local machine for development and testing purposes.

Prerequisites
Make sure you have the following installed on your machine:

Node.js (which includes npm)

Git

Installation & Running Locally
Clone the repository:

Bash

git clone https://github.com/your-username/nodejs-chat-app-ci-cd.git
cd nodejs-chat-app-ci-cd
Install dependencies:

Bash

npm install
Start the server:

Bash

npm start
Open the application:
Open your web browser and navigate to http://localhost:3000. Open multiple tabs or browsers to simulate a multi-user chat!

🤖 The CI/CD Pipeline
This project includes an automated Continuous Integration/Continuous Deployment (CI/CD) pipeline using GitHub Actions.

How It Works
Trigger: The pipeline automatically runs on every push to the main branch.

Build: It builds the Node.js application into a portable Docker image.

Push: The newly created Docker image is pushed to a container registry (like Docker Hub).

Deploy (Optional): The final step (which can be added) would be to deploy this image to a cloud server or container service.

Setting Up the Pipeline
To get the CI/CD pipeline working in your own forked repository, follow these steps:

Create a Docker Hub Account:
If you don't have one, sign up for a free account at Docker Hub.

Add GitHub Secrets:
In your GitHub repository, go to Settings > Secrets and variables > Actions and add the following secrets. This ensures your credentials are kept secure.

DOCKERHUB_USERNAME: Your Docker Hub username.

DOCKERHUB_TOKEN: A Docker Hub Personal Access Token. You can create one in your Docker Hub account settings under "Security".

Once the secrets are in place, any push to your main branch will automatically trigger the pipeline, building and publishing your application to Docker Hub.
