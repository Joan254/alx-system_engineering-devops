Additional Elements and Their Purpose:

Firewalls: Provide security by controlling and monitoring incoming and outgoing network traffic. A Web Application Firewall (WAF) protects against web-based attacks.
SSL Certificate: Enables HTTPS to secure data in transit between the user and the server.
Monitoring Clients: Collect data for monitoring purposes, providing insights into the performance, health, and security of the infrastructure.

Why Firewalls:

Firewalls are added to enhance security by controlling and monitoring traffic. A WAF specifically protects against web-based attacks.

Why HTTPS:

HTTPS encrypts the data exchanged between the user and the server, ensuring secure communication and preventing data interception or tampering.

Why Monitoring:

Monitoring is used to track and analyze the performance, availability, and security of the infrastructure. It helps in identifying issues proactively and optimizing resource utilization.

How Monitoring Tool Collects Data:

Monitoring clients act as data collectors for tools like Sumo Logic. They gather metrics, logs, and events from various components, providing a comprehensive view of the system.

Monitoring Web Server QPS:

To monitor the Web Server's Query Per Second (QPS), configure the monitoring tool to collect and analyze relevant metrics, such as incoming request rates.

Issues:

Terminating SSL at the Load Balancer Level:

Issue: While terminating SSL at the load balancer improves performance, it also means that traffic between the load balancer and the servers is unencrypted. If this internal traffic is compromised, it poses a security risk.
Solution: Encrypt internal traffic by using end-to-end SSL encryption or other secure communication methods between components.
Single MySQL Server for Writes:

Issue: Having only one MySQL server capable of accepting writes is a single point of failure. If this server fails, write operations cannot be performed.
Solution: Implement database replication or clustering to provide redundancy and fault tolerance for write operations.
Identical Components on Servers:

Issue: Having servers with identical components may lead to uniform vulnerabilities. If a vulnerability affects one server, it could potentially impact all servers.
Solution: Introduce diversity in server configurations, update schedules, or use different technologies to reduce the impact of a single vulnerability.
