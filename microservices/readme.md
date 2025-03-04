# Microservices - Currency Exchange & Conversion 🏦💱
This repository contains **two microservices**:
1. **Currency Exchange Service** (`01-currency-exchange-microservice-basic`)
  - A service to provide currency exchange rates
  - If you ask it the value of 1 USD in INR, or 1 Australian Dollar in INR, the Currency Exchange Service answers
    - 1 USD is 60 INR
    - 1 Australian Dollars is 50 INR
2. **Currency Conversion Service** (`02-currency-conversion-microservice-basic`)
  - A service to calculate currency conversion using exchange rates from the first service
  - Currency Conversion Service is used to convert a bucket of currencies
  - If you want to find the value of 10 USD, Currency Conversion Service returns 600
    - **STEP 1** : Currency Conversion Service calls the Currency Exchange Service for the value of 1 USD. It gets a response back saying 60
    - **STEP 2** : The Currency Conversion Service then multiplies 10 by 60, and returns 600 back

These microservices work together to provide real-time currency conversion using REST APIs

## 📂 Project Structure
```bash
microservices/
├── 01-currency-exchange-microservice-basic/   # Currency Exchange Microservice
│   ├── src/                                   # Source code
│   ├── Dockerfile                             # Dockerfile for containerization
│   ├── pom.xml                                # Maven dependencies
│   ├── readme.md                              # 🌟 Detailed guide for this microservice
│
├── 02-currency-conversion-microservice-basic/ # Currency Conversion Microservice
│   ├── src/                                   # Source code
│   ├── Dockerfile                             # Dockerfile for containerization
│   ├── pom.xml                                # Maven dependencies
│   ├── readme.md                              # 🌟 Detailed guide for this microservice
│
├── docker-compose.yml                         # Orchestrates both microservices
└── readme.md                                  # 🌟 You're reading it now!

```


## 🚀 Running Both Microservices with Docker Compose

We use **Docker Compose** to run both microservices together.

### 1️⃣ **Build and Run the Microservices**
```bash
docker-compose up --build
```
This will:
- Build and run **Currency Exchange Service** on `http://localhost:8000`
- Build and run **Currency Conversion Service** on `http://localhost:8100`

### 2️⃣ **Accessing the Microservices**
#### ✅ Currency Exchange API:
- **Get Exchange Rate:** [`http://localhost:8000/currency-exchange/from/USD/to/INR`](http://localhost:8000/currency-exchange/from/USD/to/INR)

#### ✅ Currency Conversion API:
- **Convert Currency:** [`http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10`](http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10)

### 3️⃣ **Stopping and Cleaning Up**
To stop the services, run:
```bash
docker-compose down
```

### 📢 Communication Between Two Services
- The **Currency Conversion Microservice** communicates with the **Currency Exchange Microservice** to fetch exchange rates
- This communication is achieved by setting up environment variable in `docker-compose.yml` file
- Configure an Environment Variable - `CURRENCY_EXCHANGE_SERVICE_HOST`
- --env `CURRENCY_EXCHANGE_SERVICE_HOST=http://currency-exchange`


## 🎯 Who is This For?
This repository is designed for:
- **Learners** exploring microservices architecture

## 📚 More Learning Resources
- **Spring Boot Documentation:** [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)
- **Docker Documentation:** [https://docs.docker.com/](https://docs.docker.com/)
