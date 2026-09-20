# Microservices Containerization

## Setup Instructions
1. Install Docker Desktop and make sure it's running.
2. Clone this repository and navigate to the Microservices folder.
3. Run: docker-compose up --build
4. Wait for all four services to start (user, product, order, gateway).
<img width="588" height="309" alt="anage microservices-cateway-service" src="https://github.com/user-attachments/assets/569d29ba-5a32-4062-b5ae-66eb18fbf9a0" />


## How to Test Each Service
- User Service: curl http://localhost:3000/health

- Product Service: curl http://localhost:3001/health
- Order Service: curl http://localhost:3002/health
- Gateway Service: curl http://localhost:3003/health
- Gateway -> Users: curl http://localhost:3003/api/users
- Gateway -> Products: curl http://localhost:3003/api/products
- Gateway -> Orders: curl http://localhost:3003/api/orders

## Troubleshooting
- If you see "Cannot connect to Docker daemon", make sure Docker Desktop is open and running.
- If a port is already in use, run: docker-compose down, then try again.
- Check logs for a specific service with: docker-compose logs <service-name>
