# Fullstack Delivery App

A full-stack delivery tracking application with DevOps pipeline.

## Tech Stack

| Component | Technology |
|-----------|------------|
| Frontend | React, Nginx |
| Backend | Spring Boot, Java 8 |
| Database | MySQL 8 |
| Containerization | Docker |
| Orchestration | Kubernetes |
| CI/CD | GitHub Actions |

## Architecture
```
User → Frontend (React/Nginx) → Backend (Spring Boot) → Database (MySQL)
```

## Local Development
```bash
docker-compose up --build
```

Access: http://localhost:3000

## CI/CD Pipeline

Push to `main` branch triggers:
1. Build frontend image
2. Build backend image
3. Push to Docker Hub

## Kubernetes Deployment
```bash
kubectl apply -f k8s/
```

### Services
- Frontend: 2 replicas
- Backend: 2 replicas
- Database: 1 replica

## Project Structure
```
├── DeliveryApp-REACTJS/     # Frontend
│   ├── Dockerfile
│   └── nginx.conf
├── DeliveryApp-SPRING-BOOT/ # Backend
│   └── Dockerfile
├── k8s/                     # Kubernetes manifests
│   ├── frontend-deployment.yaml
│   ├── backend-deployment.yaml
│   └── db-deployment.yaml
├── docker-compose.yml
└── .github/workflows/ci.yml
```

## Author

Youssef Laamarti
