Flask Application Deployment with AWS CodePipeline, CodeDeploy, and EC2
📌 Overview
This repository contains the source code and configuration files to build a Docker image for a Flask application and deploy it to EC2 instances using AWS CodePipeline and CodeDeploy.

The setup automates the process from code commit to application deployment, ensuring continuous delivery and consistent environment setup.

🚀 Workflow
Source Stage – Code is stored in a Git repository and connected to AWS CodePipeline.

Build Stage – Docker image for the Flask application is built using AWS CodeBuild.

Deploy Stage – The Dockerized application is deployed on EC2 instances through AWS CodeDeploy.

🛠️ Technologies Used
Python (Flask) – Web application framework.

Docker – Containerization of the application.

AWS CodePipeline – CI/CD orchestration.

AWS CodeBuild – Build automation and Docker image creation.

AWS CodeDeploy – Deployment automation to EC2.

AWS EC2 – Hosting environment for the application.

📂 Repository Structure
bash
Copy
Edit
"text
.
├── app/                     # Flask application source code
│   ├── app.py               # Main application file
│   ├── requirements.txt     # Python dependencies
│   └── Dockerfile           # Docker build file
├── scripts/                 # Deployment scripts for CodeDeploy
│   ├── install_dependencies.sh
│   ├── start_server.sh
│   ├── stop_server.sh
│   └── validate_service.sh
├── buildspec.yml            # AWS CodeBuild instructions
├── appspec.yml              # AWS CodeDeploy instructions
└── README.md                # Project documentation

text"
⚙️ Prerequisites
Before using this repository, ensure you have:

AWS Account with CodePipeline, CodeBuild, and CodeDeploy setup.

An EC2 instance with Docker installed and CodeDeploy agent running.

IAM roles with the necessary permissions for deployment.

📦 Deployment Steps
Clone this repository

bash
Copy
Edit
git clone https://github.com/Sushanth-1242/Sushanth_Project_AutoRabit.git
Push changes to trigger CodePipeline

CodePipeline will start the build and deploy process automatically.

