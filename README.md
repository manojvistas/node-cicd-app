# Node.js CI/CD Application

This is a sample Node.js application that demonstrates how to implement a CI/CD pipeline using GitHub Actions and Docker. The app includes a simple Express server and is built, tested, and deployed automatically to DockerHub.

---

## 🛠️ Tech Stack

- **Node.js** + **Express**
- **GitHub Actions** (CI/CD)
- **Docker** (Containerization)
- **DockerHub** (Image Registry)

---

## ⚙️ CI/CD Workflow (GitHub Actions)

This repository uses GitHub Actions to automate:

1. **Code Checkout**
2. **Install Dependencies**
3. **Run Tests**
4. **Build Docker Image**
5. **Push to DockerHub**

The workflow file is located at:  
`.github/workflows/main.yml`

> ✅ Docker image is pushed to:  
> `https://hub.docker.com/repository/docker/manoj427/node-cicd-app`

---

## 📦 How to Run the App Locally

```bash
# Clone the repo
git clone https://github.com/manojvistas/node-cicd-app.git
cd node-cicd-app

# Install dependencies
npm install

# Run the application
npm start

# Visit in browser
http://localhost:3000
🐳 Docker Commands
🔹 Build the Image
bash
Copy
Edit
docker build -t manoj427/node-cicd-app .
🔹 Run the Container
bash
Copy
Edit
docker run -p 3000:3000 manoj427/node-cicd-app
🔐 DockerHub Login (If Needed)
bash
Copy
Edit
docker login -u <your-dockerhub-username>
🔄 CI/CD Trigger
Any push or pull request to the main branch will trigger the GitHub Actions workflow.

You can verify this under:

GitHub repo → Actions tab

🧪 Troubleshooting
❌ Docker Daemon Not Running
Error:
open //./pipe/docker_engine: The system cannot find the file specified.

Fix:
Make sure Docker Desktop is running before using Docker commands.

❌ Docker Config Invalid
Error:
invalid character '\x00' looking for beginning of value

Fix:
Delete your broken Docker config file:

bash
Copy
Edit
del C:\Users\<your-username>\.docker\config.json
Then try docker login again.
