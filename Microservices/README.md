# Microservices Containerization

## Setup Instructions
1. Install Docker Desktop and make sure it's running.
2. Clone this repository and navigate to the Microservices folder.
<img width="1025" height="537" alt="image" src="https://github.com/user-attachments/assets/66bddaee-fe61-4ec5-9a92-66bfe2ae5514" />

3. Run: docker-compose up --build
4. Wait for all four services to start (user, product, order, gateway).
<img width="588" height="309" alt="anage microservices-cateway-service" src="https://github.com/user-attachments/assets/569d29ba-5a32-4062-b5ae-66eb18fbf9a0" />


## How to Test Each Service
- User Service: curl http://localhost:3000/health
<img width="508" height="180" alt="localhost3000users" src="https://github.com/user-attachments/assets/d46281c6-7734-4055-a655-6baeec8d62b3" />

- Product Service: curl http://localhost:3001/health
<img width="679" height="146" alt=" → CO localhost3001products" src="https://github.com/user-attachments/assets/b000c794-f6a3-46c0-a982-ccad7384ec57" />

- Order Service: curl http://localhost:3002/health
<img width="338" height="120" alt="Pretty printO" src="https://github.com/user-attachments/assets/d34b0d58-bb30-4374-bd04-fa9f4a3aafc1" />

- Gateway Service: curl http://localhost:3003/health
<img width="361" height="116" alt="image" src="https://github.com/user-attachments/assets/a6c385ba-8fb2-486e-a020-1bc74d2f7d73" />

- Gateway -> Users: curl http://localhost:3003/api/users
<img width="422" height="157" alt="localhost3003apiusers" src="https://github.com/user-attachments/assets/b50afc8b-1ad3-471d-aceb-aa440a5b9d83" />


- Gateway -> Products: curl http://localhost:3003/api/products
<img width="611" height="164" alt="localnost30Usapvproducts" src="https://github.com/user-attachments/assets/818978f2-67fa-4462-8173-adce80ee6db0" />

- Gateway -> Orders: curl http://localhost:3003/api/orders
<img width="611" height="164" alt="localnost30Usapvproducts" src="https://github.com/user-attachments/assets/e38cc85e-bc01-4441-9112-33b3c63e2aa3" />

<img width="603" height="299" alt="image" src="https://github.com/user-attachments/assets/e89a0036-8f99-4b04-8f32-5762d49649c9" />

## Troubleshooting
- If you see "Cannot connect to Docker daemon", make sure Docker Desktop is open and running.
- If a port is already in use, run: docker-compose down, then try again.
- Check logs for a specific service with: docker-compose logs <service-name>
