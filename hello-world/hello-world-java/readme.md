# Hello World Java 🚀

A simple **Spring Boot REST API**, packaged with **Docker**

## 📂 Folder Structure

Here’s the folder structure for this project:

```bash
hello-world-java/
├── src/
│   ├── main/
│   │   ├── java/com/in28minutes/rest/webservices/restfulwebservices/
│   │   │   ├── HelloWorldController.java       # Controller handling HTTP requests
│   │   │   ├── RestfulWebServicesApplication.java  # Main Spring Boot application entry
│   │   ├── resources/
│   │   │   ├── application.properties         # Configuration file (sets port 5000)
│   ├── test/java/com/in28minutes/rest/webservices/restfulwebservices/
│   │   ├── RestfulWebServicesApplicationTests.java # Unit test file
├── Dockerfile            # Dockerfile to containerize the application
├── pom.xml               # Maven dependencies and project metadata
```

## 🛠️ Prerequisites

Before running the project, ensure you have:

- **Java 8** or higher installed
- **Maven** installed
- **Docker** installed on your machine

## 🚀 Running the Application Locally

If you want to run the Java application without Docker:

```bash
# Build the JAR file
mvn clean package

# Run the application
java -jar target/hello-world-java.jar
```

The application will be available at:
👉 **http://localhost:5000**

## 🐳 Building and Running the Docker Container

### 1️⃣ Build the Docker Image

The `Dockerfile` follows a **multi-stage build** pattern using Maven and OpenJDK

To build the image, use the following **generalized** command:

```bash
docker build -t my-java-app .
```

For **production-ready naming**, use:

```bash
docker build -t myrepo/hello-world-java:v1 .
```

### 2️⃣ Run the Docker Container

Once the image is built, start a container:

```bash
docker run -p 5000:5000 my-java-app
```

Or, using the production-grade naming:

```bash
docker run -d -p 5000:5000 --name hello-java-app myrepo/hello-world-java:v1
```

### 3️⃣ Access the Application in Docker

After running the container, open your browser and go to:

👉 **http://localhost:5000**

You should see:

```json
{"message":"Hello World Java v1"}
```

## 🛑 Stopping and Removing the Container

To stop the running container:

```bash
docker stop hello-java-app
```

To remove the container:

```bash
docker rm hello-java-app
```

## 🏗️ Docker Best Practices

- Use **multi-stage builds** to minimize final image size
- Pin **Java versions** to ensure consistency
- Use **environment variables** instead of hardcoded values
