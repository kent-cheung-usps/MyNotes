## Microservices
Microservices are an architectural style for software development. They structure an application as a collection of small, autonomous services modeled around a business requirement.
## Key characteristics of a microservices architecture
Single Responsibility: Each microservice focuses on one specific task or function.
- **Independence:** Microservices can work, update, and grow on their own. They use APIs to talk to other services.
- **Decentralization:** Each service manages its own data to stay separate from others.
- **Fault Isolation:** If one service fails, it doesn’t affect the rest of the system.
- **Flexibility:** Microservices can use different programming languages or tools that fit their needs.
- **Containerization:** Tools like Docker and Kubernetes help manage, scale, and deploy microservices easily.
## Design Patterns in Microservices Architecture
**API Gateway Pattern**
- Provides a single entry point for clients, handling tasks like routing requests, authentication, and response aggregation.
**Circuit Breaker Pattern**
- Prevents cascading failures by detecting service failures and providing fallback responses.
**Database per Service Pattern**
- Ensures each service has its own database, maintaining independence and minimizing coupling.
**Saga Pattern**
- Manages distributed transactions across multiple services using a series of local transactions.
**Event-Driven Pattern**
- A service sends out a message (event) when it does something important, and other services react to it.
## Design Focus
- A good microservice design focuses on addressing the specific challenges and requirements of the system.
- In short, pick the right patterns for business use case and scale the design thoughtfully
