# Hello World - Simple learning Projects 🐳

A collection of **three simple applications** (Java, Node.js, and Python) designed to help you **learn Docker, Kubernetes, containerization, and deployment**

## 📖 About This Repository

This repository contains three different **Hello World** applications, each implemented in a different programming language and packaged using Docker. The purpose of this repository is to **demonstrate the basics of Docker** by containerizing and running these applications in an isolated environment

Each project comes with:
- ✅ A simple web application that returns a "Hello World" response
- ✅ A **Dockerfile** to build a containerized version of the application
- ✅ A dedicated **README.md** explaining how to run and test the project

---

## 📂 Folder Structure

```bash
hello-world/
├── hello-world-java/      # Spring Boot application
│   ├── src/               # Java source code
│   ├── Dockerfile         # Dockerfile for containerization
│   ├── pom.xml            # Maven dependencies
│   ├── readme.md          # 🌟 Detailed guide for Java project
│
├── hello-world-nodejs/    # Express.js application
│   ├── index.js           # Main server script
│   ├── package.json       # Node.js dependencies
│   ├── Dockerfile         # Dockerfile for containerization
│   ├── readme.md          # 🌟 Detailed guide for Node.js project
│
├── hello-world-python/    # Flask application
│   ├── launch.py          # Main Python script
│   ├── requirements.txt   # Python dependencies
│   ├── Dockerfile         # Dockerfile for containerization
│   ├── readme.md          # 🌟 Detailed guide for Python project
│
└── readme.md              # 🌟 This metadata file (you're reading it now!)
```

---

## 🚀 How to Use This Repository

1️⃣ Clone the repository:
```bash
git clone https://github.com/your-username/hello-world.git
cd hello-world
```

2️⃣ Explore each project's dedicated folder:
- Java Project: `cd hello-world-java`
- Node.js Project: `cd hello-world-nodejs`
- Python Project: `cd hello-world-python`

3️⃣ Read the **README.md** inside each project folder for setup and Docker instructions
- Java Project:
  - [Checkout detailed instruction HERE](./hello-world-java/readme.md)
- Node.js Project:
  - [Checkout detailed instruction HERE](./hello-world-nodejs/readme.md)
- Python Project:
  - [Checkout detailed instruction HERE](./hello-world-python/readme.md)

---

## 🐳 Learning Docker with This Repository

### **1️⃣ Understanding the Basics**
Each project includes a **Dockerfile**, allowing you to containerize and run the application inside a Docker container

### **2️⃣ Building Docker Images**
For example, to build the **Java application**, navigate to its folder and run:
```bash
docker build -t hello-world-java .
```
Do the same for **Node.js** and **Python**, replacing the project name

### **3️⃣ Running Containers**
After building, run the application inside a container:
```bash
docker run -p 5000:5000 hello-world-java
```
Repeat the same for **Node.js** and **Python** applications

### **4️⃣ Accessing the Application**
Once running, open a browser or use `curl`:
```bash
curl http://localhost:5000
```
You should see the `"Hello World"` response

---

## 🎯 Who is This For?

This repository is perfect for:
- ✅ **Beginners** learning Docker, containerization and kubernetes


---

## 📚 More Information

- To learn more about **Docker**, check out the official documentation:
  👉 [https://docs.docker.com/](https://docs.docker.com/)
- Want to go deeper into **Spring Boot**, **Node.js**, or **Flask**? Check their respective official docs:
  - **Spring Boot**: [https://spring.io/guides](https://spring.io/guides)
  - **Express.js**: [https://expressjs.com/](https://expressjs.com/)
  - **Flask**: [https://flask.palletsprojects.com/](https://flask.palletsprojects.com/)

