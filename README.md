# E-commerce Microservices

## Overview

Welcome to the E-commerce Microservices repository! This project demonstrates a modern e-commerce platform built using microservices architecture. The system is designed to be scalable, resilient, and maintainable through the implementation of best practices in distributed systems.

![E-commerce Microservice Architecture](https://raw.githubusercontent.com/kenniy/EcommerceMicroservices/refs/heads/main/EcommerceMicroservice.png)

## Features

- Product catalog management
- Shopping cart functionality
- Order processing
- User authentication and authorization
- API Gateway for unified access
- Event-driven communication between services

## Technology Stack

- **Backend**: ASP.NET Core 8 Web API
- **Database**: Microsoft SQL Server
- **ORM**: Entity Framework Core 8
- **Validation**: FluentValidation
- **Messaging**: RabbitMQ with MassTransit
- **Caching**: Redis
- **API Gateway**: Ocelot
- **Containerization**: Docker
- **Design Patterns**:
  - Clean Architecture
  - Domain-Driven Design (DDD)
  - Command Query Responsibility Segregation (CQRS) with MediatR
  - Event-Driven Architecture (EDA)

## Architecture

This project follows a microservices architecture where each service is responsible for a specific business capability. The services are loosely coupled and communicate through APIs and messaging systems, allowing for independent deployment and scaling.
The application consists of several microservices:

- **Product Service**: Manages product catalog and inventory
- **Cart Service**: Handles shopping cart operations
- **Order Service**: Processes and tracks orders
- **Identity Service**: Manages user authentication and authorization
- **API Gateway**: Routes requests to appropriate services
- **Message Broker**: Facilitates asynchronous communication between services

## Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) (optional if using Docker)

## Getting Started

Follow these steps to run the application locally:

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/EcommerceMicroservices.git
   cd EcommerceMicroservices
   ```

2. Using Docker (recommended):

   ```bash
   docker-compose up -d
   git
   ```

   This will start all services, databases, and dependencies.

3. Using Visual Studio:
   - Open the solution file in Visual Studio
   - Set the docker-compose project as the startup project
   - Press F5 or click the Docker Compose button on the toolbar

4. Access the services:
   - API Gateway: [http://localhost:8010](http://localhost:8010)
   - Swagger UI for each service:
     - Product Service: [http://localhost:8001/swagger](http://localhost:8001/swagger)
     - Cart Service: [http://localhost:8002/swagger](http://localhost:8002/swagger)
     - Order Service: [http://localhost:8003/swagger](http://localhost:8003/swagger)

## Development Notes

- Each microservice follows Clean Architecture principles with separate layers for domain, application, infrastructure, and presentation
- Services communicate through asynchronous messaging for eventual consistency
- Data persistence is handled independently by each service

## Troubleshooting

- **Docker Issues**: Ensure Docker Desktop is running and has sufficient resources allocated
- **Database Connection**: Check connection strings in app settings.json or environment variables
- **Port Conflicts**: Make sure the required ports are available on your machine

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details

## Acknowledgements

- [Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/)
- [MassTransit Documentation](https://masstransit-project.com/)
- [Ocelot Documentation](https://ocelot.readthedocs.io/en/latest/)
- [FluentValidation Documentation](https://docs.fluentvalidation.net/en/latest/)
- [Docker Documentation](https://docs.docker.com/)

## Contact

For any questions or feedback, please open an issue on the GitHub repository or contact the project maintainer
