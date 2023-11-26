1. Server

Purpose:
The server is the foundational component that hosts and runs the entire web infrastructure.

Rationale:
A single server is required to serve as the hosting environment for the entire web application.

2. Load Balancer (HAproxy)

Purpose:
The load balancer distributes incoming network traffic across multiple servers to ensure optimal resource utilization and high availability.

Rationale:
By configuring HAproxy as a cluster with redundancy, we enhance fault tolerance and prevent a single point of failure. This ensures continuous service availability even if one load balancer node goes down.

3. Web Server

Purpose:
The web server handles HTTP requests, serves static content, and manages the initial interaction with clients.

Rationale:
Separating the web server from the application server allows for dedicated handling of static content and improves overall performance. This division of responsibilities enhances scalability and simplifies maintenance.

4. Application Server

Purpose:
The application server executes the application code, processes dynamic content, and communicates with the database.

Rationale:
Isolating the application logic into a dedicated server enables efficient resource utilization. This separation enhances scalability, allows for specialized configurations, and facilitates easier maintenance and updates.

5. Database

Purpose:
The database stores and manages the application's data, handling read and write operations.

Rationale:
Having a dedicated database server separates data storage concerns from application logic. This improves data management, allows for scalability, and simplifies database maintenance.
