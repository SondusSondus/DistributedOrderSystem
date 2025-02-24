

### **📌 Distributed Order Processing System**
🚀 **A scalable, event-driven microservices architecture built using .NET 9 and deployed on Azure Kubernetes Service (AKS).**  

---

## **📖 Overview**
The **Distributed Order Processing System** is a cloud-native microservices-based solution designed for **high availability, scalability, and resilience**. It enables seamless **order management, inventory tracking, payment processing, and notifications** using an **event-driven architecture**.

This system is built using **.NET 9, Entity Framework Core, RabbitMQ/Kafka, and Azure Kubernetes Service (AKS)** to ensure **real-time communication** between services.

---

## **🔗 System Architecture**
The system follows the **microservices architecture** pattern, enabling **independent service scaling** and **fault tolerance**.

### **🏗 Microservices Overview**
| Microservice | Responsibility |
|-------------|--------------|
| **Order Service** | Manages order creation, tracking, and status updates. |
| **Inventory Service** | Checks stock availability and updates inventory. |
| **Payment Service** | Handles payments via an external payment gateway. |
| **Notification Service** | Sends order confirmation via email/SMS. |
| **API Gateway (Ocelot)** | Routes external requests to microservices. |
| **Message Broker (RabbitMQ/Kafka)** | Handles asynchronous communication between services. |

---

## **📡 Tech Stack**
| Component | Technology |
|-----------|------------|
| **Backend** | .NET 9 Web API, C# |
| **Database** | SQL Server, Redis Cache |
| **Event Bus** | RabbitMQ / Kafka |
| **API Gateway** | Ocelot |
| **Authentication** | IdentityServer, OAuth 2.0 |
| **Logging & Monitoring** | Serilog, ELK Stack, Prometheus, Grafana |
| **Deployment** | Docker, Kubernetes (AKS) |
| **CI/CD** | GitHub Actions, Azure DevOps |

---

## **📌 Key Features**
✅ **Scalable Microservices Architecture**  
✅ **Event-Driven Communication using RabbitMQ/Kafka**  
✅ **API Gateway for Routing and Security**  
✅ **OAuth 2.0 Authentication & Role-Based Access Control (RBAC)**  
✅ **Resilient System with Circuit Breakers & Retry Mechanisms**  
✅ **Kubernetes-based Cloud Deployment (AKS)**  
✅ **Automated CI/CD Pipeline with GitHub Actions**  

---

## **🛠 Getting Started**
### **1️⃣ Prerequisites**
Ensure you have the following installed:
- **.NET 9 SDK** → [Download](https://dotnet.microsoft.com/download/dotnet/9.0)
- **Docker & Docker Compose** → [Download](https://www.docker.com/products/docker-desktop)
- **RabbitMQ / Kafka** → Installed via Docker
- **SQL Server** → [Download](https://www.microsoft.com/en-us/sql-server)

### **2️⃣ Clone the Repository**
```sh
git clone https://github.com/your-username/DistributedOrderSystem.git
cd DistributedOrderSystem
```

### **3️⃣ Run the Microservices Locally**
```sh
dotnet build
dotnet run --project src/OrderService/OrderService.API
dotnet run --project src/InventoryService/InventoryService.API
dotnet run --project src/PaymentService/PaymentService.API
dotnet run --project src/NotificationService/NotificationService.API
```

### **4️⃣ Run with Docker Compose**
```sh
docker-compose up -d
```

---

## **🖥️ Deployment to Azure Kubernetes Service (AKS)**
1. **Build & Push Docker Images**
```sh
docker build -t your-dockerhub/order-service ./src/OrderService/OrderService.API
docker push your-dockerhub/order-service
```
2. **Apply Kubernetes Manifests**
```sh
kubectl apply -f k8s-manifests/
```
3. **Monitor Logs**
```sh
kubectl get pods -n order-system
kubectl logs -f <pod-name>
```

---

## **📌 Project Structure**
```
DistributedOrderSystem/
│-- src/
│   ├── OrderService/
│   │   ├── OrderService.API/ (Controllers & API Logic)
│   │   ├── OrderService.Domain/ (Entities & Business Logic)
│   │   ├── OrderService.Infrastructure/ (Database & Repositories)
│   ├── InventoryService/
│   ├── PaymentService/
│   ├── NotificationService/
│-- infrastructure/
│   ├── api-gateway/ (Ocelot API Gateway)
│   ├── message-broker/ (RabbitMQ/Kafka setup)
│-- deployment/
│   ├── docker-compose.yml
│   ├── k8s-manifests/
│-- tests/
│-- docs/
```

---

## **🚀 Roadmap**
- [x] Set up .NET 9 microservices structure
- [x] Implement Entity Framework Core & SQL Server
- [x] Set up RabbitMQ/Kafka for Event-Driven Architecture
- [ ] Implement API Gateway & Authentication
- [ ] Deploy to Azure Kubernetes Service (AKS)
- [ ] Integrate Monitoring & Logging

---

## **🤝 Contributing**
1. **Fork the repo**
2. **Create a new branch** (`feature/your-feature`)
3. **Commit changes** (`git commit -m "Added feature X"`)
4. **Push the branch** (`git push origin feature/your-feature`)
5. **Open a Pull Request**

---

