# Currency Exchange Microservice 💱

A Spring Boot microservice that provides **exchange rates** for different currencies
  - If you ask it the value of 1 USD in INR, or 1 Australian Dollar in INR, the Currency Exchange Service answers
    - 1 USD is 60 INR
    - 1 Australian Dollars is 50 INR

## 🛠️ Prerequisites
- **Java 8+**
- **Maven**
- **Docker** (optional, for containerized deployment)

## 📌 API Endpoints

| Method | Endpoint | Description |
|--------|---------|-------------|
| `GET` | `/` | Health check `{healthy:true}` |
| `GET` | `/currency-exchange/from/{from}/to/{to}` | Fetch exchange rate from one currency to another |

### 📍 Example API Call:
GET http://localhost:8000/currency-exchange/from/EUR/to/INR

#### ✅ Sample Response:
```json
{
  "id": 10002,
  "from": "EUR",
  "to": "INR",
  "conversionMultiple": 75.00,
  "exchangeEnvironmentInfo": "37f1ad927c6e v1 27c6e"
}
```


## 🚀 Running Locally

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/your-username/microservices.git
cd microservices/01-currency-exchange-microservice-basic
```

### 2️⃣ **Run Using Maven**
```bash
mvn spring-boot:run
```

The service will be available at `http://localhost:8000`


## 🐳 Running with Docker

### 1️⃣ **Build the Docker Image**
```bash
docker build -t currency-exchange-service .
```

### 2️⃣ **Run the Container**
```bash
docker run -p 8000:8000 currency-exchange-service
```

### 3️⃣ **Access the Application**
- **API Endpoint:** [`http://localhost:8000/currency-exchange/from/USD/to/INR`](http://localhost:8000/currency-exchange/from/USD/to/INR)


## 🛑 Stopping and Cleaning Up
To stop the container:
```bash
docker stop currency-exchange-service
```
To remove the container:
```bash
docker rm currency-exchange-service
```











