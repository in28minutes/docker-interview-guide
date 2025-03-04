# Currency Conversion Microservice 💹

A Spring Boot microservice that performs **currency conversion** using exchange rates from the **Currency Exchange Microservice**
  - Currency Conversion Service is used to convert a bucket of currencies
  - If you want to find the value of 10 USD, Currency Conversion Service returns 600
    - **STEP 1** : Currency Conversion Service calls the Currency Exchange Service for the value of 1 USD. It gets a response back saying 60
    - **STEP 2** : The Currency Conversion Service then multiplies 10 by 60, and returns 600 back

## 🛠️ Prerequisites
- **Java 8+**
- **Maven**
- **Docker** (optional, for containerized deployment)

## 📌 API Endpoints

| Method | Endpoint | Description |
|--------|---------|-------------|
| `GET` | `/` | Health check `{healthy:true}` |
| `GET` | `/currency-conversion/from/{from}/to/{to}/quantity/{quantity}` | Converts currency amount |

### 📍 Example API Call:
```
GET http://localhost:8100/currency-conversion/from/EUR/to/INR/quantity/10
```
#### ✅ Sample Response:
```json
{
  "id": 10002,
  "from": "EUR",
  "to": "INR",
  "conversionMultiple": 75.00,
  "quantity": 10,
  "totalCalculatedAmount": 750.00,
  "exchangeEnvironmentInfo": "37f1ad927c6e v1 27c6e",
  "conversionEnvironmentInfo": "fb6316b5713d v1 5713d"
}
```


## 🚀 Running Locally

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/your-username/microservices.git
cd microservices/02-currency-conversion-microservice-basic
```

### 2️⃣ **Run Using Maven**
```bash
mvn spring-boot:run
```

The service will be available at `http://localhost:8100`


## 🐳 Running with Docker

### 1️⃣ **Build the Docker Image**
```bash
docker build -t currency-conversion-service .
```

### 2️⃣ **Run the Container**
```bash
docker run -p 8100:8100 currency-conversion-service
```

### 3️⃣ **Access the Application**
- **API Endpoint:** [`http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10`](http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10)



## 🛑 Stopping and Cleaning Up
To stop the container:
```bash
docker stop currency-conversion-service
```
To remove the container:
```bash
docker rm currency-conversion-service
```