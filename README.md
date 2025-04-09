# Jenkins CI/CD Pipeline Project

## 🚀 Project Title:
**Automate Code Build and Deployment Using Jenkins Pipeline**

## 🎯 Objective:
Set up a basic Jenkins pipeline to automatically build and deploy an application whenever code is pushed to a GitHub repository.

## 🛠️ Tools & Technologies:
- Jenkins
- Docker
- GitHub
- Ngrok (for local Jenkins-GitHub webhook testing)

## 📂 Project Structure:
jenkins-ci-cd/ Jenkinsfile app/ # Your application code (example: index.js, app.py) README.md


## 🔄 Pipeline Stages:
The pipeline includes the following stages:

1. **Build** – Compile or set up the application.
2. **Test** – (Optional) Run tests to ensure stability.
3. **Deploy** – Deploy the application (e.g., to a container or server).

Done with
Install Jenkins (or use a cloud instance).
 Create a Jenkinsfile in your project repo with steps to build and deploy the app.
 Configure Jenkins to trigger the pipeline on each code commit. 
 Add stages like build, test, and deploy. 
 Test the pipeline by pushing changes and checking the Jenkins dashboard

## 🔧 Jenkins Setup:

### 1. Install Jenkins using Docker:
```bash
docker run -d --name jenkins \
  -p 8080:8080 -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  jenkins/jenkins:lts
2. Install Plugins:
Ensure the following plugins are installed:

Git Plugin

GitHub Plugin

GitHub Integration Plugin

Pipeline: GitHub

3. Configure GitHub Webhook:
Run ngrok http 8080 to expose Jenkins to GitHub.

Use https://<your-ngrok>.ngrok-free.app/github-webhook/ as the webhook URL.

Add this URL under GitHub → Repo → Settings → Webhooks.

🧪 Testing the Pipeline:
Push a code change to your GitHub repository.

Jenkins will automatically start a new build.

View the build status and logs in the Jenkins dashboard.

✅ Output:
Successful pipeline execution triggered by code commit.

Stages displayed with console output in Jenkins UI.

✍️ Author:
Dasaradhi T

 Notes:
This project is beginner-friendly and follows DevOps best practices.

Can be extended with test reports, notifications, or multi-branch pipelines.
