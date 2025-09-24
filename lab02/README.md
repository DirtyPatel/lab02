## What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology?
- I refactored both the order-service and product-service to remove hard-coded values (such as ports and RabbitMQ connection strings). Instead, these configurations are now stored in environment variables and loaded using a .env file in development. This way, the services can connect to different backing services (like RabbitMQ or databases) without requiring code changes, only configuration changes.

## Why is it important to use environment variables instead of hard-coding configurations in your application?
- Using environment variables ensures that sensitive information (like usernames, passwords, or connection strings) is not exposed in the source code. It also makes the application more portable and flexible — the same codebase can run across multiple environments (development, testing, production) by simply switching environment variables.

## Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?
-Having separate repositories for each microservice keeps them independent. Each service has its own code, dependencies, and deployment pipeline. This makes it easier to:
    - Scale only the services that need it.
    - Update or redeploy one service without breaking others.
    - Keep version control clean and organized.
    - Let different people or teams work on different services without conflicts.

## Link to youtube 

https://youtu.be/gYJ0dnXC4Sk&nbsp;

## Link to the 3 Repositories 

https://github.com/DirtyPatel/store-front

https://github.com/DirtyPatel/product-service

https://github.com/DirtyPatel/order-service