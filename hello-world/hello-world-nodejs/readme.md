# Hello World Node.js 🚀

A simple **Node.js** web application using **Express.js**, packaged with **Docker**

## 📂 Folder Structure

Here’s the folder structure for this project:

```bash
hello-world-nodejs/
├── Dockerfile         # Dockerfile to containerize the application
├── index.js           # Main Node.js script running Express server
└── package.json       # Project metadata and dependencies
```

## 🛠️ Prerequisites

Before running the project, ensure you have:

- **Node.js** (≥ 8.16.1) installed
- **Docker** installed on your machine
- **npm** (Node Package Manager) installed

## 🚀 Running the Application Locally

If you want to run the Node.js app without Docker:

```bash
# Install dependencies
npm install

# Run the application
node index.js
```

The application will be available at:
👉 **http://localhost:5000**

## 🐳 Building and Running the Docker Container

### 1️⃣ Build the Docker Image

The `Dockerfile` is based on `node:8.16.1-alpine`, ensuring a lightweight image

To build the image, use the following **generalized** command:

```bash
docker build -t my-nodejs-app .
```

For **production-ready naming**, use:

```bash
docker build -t myrepo/hello-world-nodejs:v1 .
```

### 2️⃣ Run the Docker Container

Once the image is built, start a container:

```bash
docker run -p 5000:5000 my-nodejs-app
```

Or, using the production-grade naming:

```bash
docker run -d -p 5000:5000 --name hello-nodejs-app myrepo/hello-world-nodejs:v1
```

### 3️⃣ Access the Application in Docker

After running the container, open your browser and go to:

👉 **http://localhost:5000**

You should see:

```json
{"message":"Hello World JavaScript v1"}
```

## 🛑 Stopping and Removing the Container

To stop the running container:

```bash
docker stop hello-nodejs-app
```

To remove the container:

```bash
docker rm hello-nodejs-app
```

## 🏗️ Docker Best Practices

- Use **multi-stage builds** for optimized image sizes
- Pin **Node.js versions** to ensure consistency
- Use **environment variables** instead of hardcoded values