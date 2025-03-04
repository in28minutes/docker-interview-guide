# Hello World Python 🚀

A simple Python web application using Flask, packaged with Docker

## 📂 Folder Structure

Here’s the folder structure for this project:

```bash
hello-world-python/
├── Dockerfile           # Dockerfile to containerize the application
├── launch.py            # Main Python script running Flask web server
├── requirements.txt     # Python dependencies for the application
└── readme.md            # Documentation for the project
```

## 🛠️ Prerequisites

Before running the project, ensure you have:

- **Python** (≥ 3.x) installed
- **Docker** installed on your machine
- **pip** package manager for Python

## 🚀 Running the Application Locally

If you want to run the Flask app without Docker:

```bash
# Install dependencies
pip install -r requirements.txt

# Run the application
python launch.py
```

The application will be available at:
👉 **http://localhost:5000**

## 🐳 Building and Running the Docker Container

### 1️⃣ Build the Docker Image

The `Dockerfile` is based on `python:alpine3.10`, ensuring a lightweight image

To build the image, use the following **generalized** command:

```bash
docker build -t my-python-app .
```

For **production-ready naming**, use:

```bash
docker build -t myrepo/hello-world-python:v1 .
```

### 2️⃣ Run the Docker Container

Once the image is built, start a container:

```bash
docker run -p 5000:5000 my-python-app
```

Or, using the production-grade naming:

```bash
docker run -d -p 5000:5000 --name hello-python-app myrepo/hello-world-python:v1
```

### 3️⃣ Access the Application in Docker

After running the container, open your browser and go to:

👉 **http://localhost:5000**

You should see:

```json
{"message":"Hello World Python v1"}
```

## 🛑 Stopping and Removing the Container

To stop the running container:

```bash
docker stop hello-python-app
```

To remove the container:

```bash
docker rm hello-python-app
```

## 🏗️ Docker Best Practices

- Use **multi-stage builds** for optimized image sizes
- Pin **Python versions** to ensure consistency
- Use **environment variables** instead of hardcoded values

