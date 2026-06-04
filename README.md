# 💳 PaymentFlow – Payment Processing System

A production-inspired payment processing platform built using **Flask**, **SQLAlchemy**, and **MySQL**.

The system allows merchants to create payments, track transaction lifecycles, process refunds, retry failed transactions, and monitor activity through a modern web dashboard.

---

## 🚀 Features

### Payment Management

* Create card, bank, and wallet payments
* Unique payment tracking
* Idempotency support
* Customer and merchant management

### Transaction Processing

* Automatic transaction creation
* Success and failure tracking
* Transaction history monitoring
* Payment status updates

### Failure Handling

* Simulate gateway failures
* Retry failed transactions
* Test payment recovery workflows

### Refund System

* Full refunds
* Partial refunds
* Refund tracking
* Refund history

### Dashboard

* Interactive payment console
* Filter payments by status
* Retry failed transactions
* Process refunds from UI
* Real-time ledger visibility

### REST API

* Payment APIs
* Transaction APIs
* Refund APIs
* Health monitoring endpoint

---

## 🛠 Tech Stack

### Backend

* Python
* Flask
* SQLAlchemy
* REST API

### Database

* MySQL
* SQLite (Development)

### DevOps

* Docker
* Docker Compose

### Testing

* PyTest

---

## 📂 Project Structure

```text
project/
│
├── app/
├── tests/
├── .env.example
├── docker-compose.yml
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ⚡ Installation

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/paymentflow.git
cd paymentflow
```

### 2. Create Virtual Environment

```bash
python -m venv .venv
```

Activate environment:

Windows:

```bash
.venv\Scripts\activate
```

Linux/Mac:

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment

```bash
cp .env.example .env
```

Example:

```env
FLASK_ENV=development
DATABASE_URL=sqlite:///dev.db
PAYMENT_GATEWAY_FAILURE_RATE=0
```

---

## 🐳 Run With Docker

Start MySQL:

```bash
docker compose up -d mysql
```

Run application:

```bash
flask --app app:create_app run --debug
```

---

## ▶ Run Locally

```bash
flask --app app:create_app run --debug
```

Application:

```text
http://127.0.0.1:5000
```

---

## API Endpoints

### Health Check

```http
GET /health
```

### Create Payment

```http
POST /api/payments
```

### List Payments

```http
GET /api/payments
```

### Get Payment

```http
GET /api/payments/{payment_id}
```

### Retry Payment

```http
POST /api/payments/{payment_id}/retry
```

### Create Refund

```http
POST /api/payments/{payment_id}/refunds
```

### List Refunds

```http
GET /api/refunds
```

### List Transactions

```http
GET /api/transactions
```

---

## Payment Lifecycle

```text
Pending
   ↓
Processing
   ↓
Succeeded / Failed
   ↓
Refunded / Partially Refunded
```

---

## Testing

Run tests:

```bash
pytest
```

---

## Future Improvements

* JWT Authentication
* Role-Based Access Control
* Payment Analytics Dashboard
* Webhook Integration
* Multi-Currency Support
* Kafka/RabbitMQ Event Processing
* Kubernetes Deployment

---

## Why This Project?

This project demonstrates real-world backend engineering concepts including:

* Payment lifecycle management
* Transaction consistency
* Refund processing
* Failure recovery
* RESTful API design
* Database modeling
* Dockerized deployment
* Test-driven development

Perfect for showcasing backend development and fintech engineering skills.

---

## License

MIT License

Feel free to fork, improve, and use this project for learning and portfolio purposes.

