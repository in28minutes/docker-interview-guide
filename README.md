
---

# Docker Interview Guide: Projects Repository
- Welcome to the **Docker Interview Guide** projects repository! This repo contains hands-on examples that help you practice **Docker**, **containerization**, and **microservices** development.
- Each project folder has its own detailed `README.md` with build instructions, so you can jump right in.

---

## 📂 Repository Structure

```bash
.
├── hello-world
│   ├── hello-world-java
│   ├── hello-world-nodejs
│   ├── hello-world-python
│   └── readme.md
├── microservices
│   ├── 01-currency-exchange-microservice-basic
│   ├── 02-currency-conversion-microservice-basic
│   ├── docker-compose.yml
│   └── readme.md
└── readme.md
```

### 1. **Hello World**
A collection of simple **"Hello World"** applications in different programming languages:
- **[Java](./hello-world/hello-world-java/readme.md)**
- **[Node.js](./hello-world/hello-world-nodejs/readme.md)**
- **[Python](./hello-world/hello-world-python/readme.md)**

Each folder contains:
- A minimal application (Spring Boot, Express.js, Flask)
- A `Dockerfile` to build and run the project in a container
- Step-by-step instructions in its `readme.md`

> **Explore** the [`hello-world/`](./hello-world/readme.md) folder for an overview of all three projects.

---

### 2. **Microservices**
Two microservices demonstrating **currency exchange** and **conversion**:
- **[01-currency-exchange-microservice-basic](./microservices/01-currency-exchange-microservice-basic/readme.md)**
- **[02-currency-conversion-microservice-basic](./microservices/02-currency-conversion-microservice-basic/readme.md)**

Use [`docker-compose.yml`](./microservices/docker-compose.yml) to run both services together:
- **Currency Exchange Service** (provides exchange rates)
- **Currency Conversion Service** (calculates conversions based on exchange rates)

> **Explore** the [`microservices/`](./microservices/readme.md) folder for setup instructions and architecture details.

---

## 🚀 Getting Started

1. **Clone the repository**:
   ```bash
   git clone https://github.com/in28minutes/docker-interview-guide.git
   cd docker-interview-guide
   ```
2. **Choose a project**: Navigate into the project folder of your choice.
3. **Follow the instructions**: Each project has a `readme.md` explaining how to build and run its Docker container.

---

## 💡 What’s Next?

- **More Projects**: We plan to add additional examples covering advanced Docker topics, Kubernetes deployments, and more.
- **Stay Updated**: Watch or star this repo to get notified when new projects or updates are released.

---

## 📚 Additional Resources

- **Docker Documentation**: [https://docs.docker.com/](https://docs.docker.com/)
- **Kubernetes Documentation**: [https://kubernetes.io/docs/](https://kubernetes.io/docs/)
- **Spring Boot**: [https://spring.io/guides](https://spring.io/guides)
- **Node.js**: [https://nodejs.org/en/docs/](https://nodejs.org/en/docs/)
- **Python & Flask**: [https://flask.palletsprojects.com/](https://flask.palletsprojects.com/)
