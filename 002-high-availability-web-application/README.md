# Case Study 004

Designing a High Availability Architecture for a Business-Critical Web Application

## Executive Summary
Contoso Retail Ltd., a rapidly growing e-commerce company with approximately 250 employees, relies heavily on its online shopping platform to generate revenue and serve customers across multiple regions. The application is currently hosted on a single Azure Virtual Machine running Ubuntu Server and Nginx.

While the existing environment satisfies normal operational requirements, it introduces a significant business risk due to the absence of redundancy. Any planned maintenance, hardware failure, operating system issue, or unexpected outage would result in complete application downtime, directly affecting customer experience, company reputation, and revenue.

To address these challenges, a new highly available architecture was designed using Microsoft Azure. The proposed solution distributes application traffic across multiple Linux virtual machines deployed in separate Availability Zones using Azure Load Balancer. Health Probes continuously monitor server availability, allowing traffic to be automatically redirected to healthy instances in the event of a failure.

The redesigned architecture eliminates the single point of failure, improves service availability, enhances operational resilience, and establishes a scalable foundation capable of supporting future business growth.

## Business Services
Contoso Retail provides an online marketplace that allows customers to purchase consumer electronics, office equipment, and accessories. The company's primary revenue source depends on uninterrupted availability of its web platform.

During seasonal campaigns such as Black Friday, Cyber Monday, and holiday sales, website traffic can increase by more than 400%, requiring the underlying infrastructure to remain highly available and capable of handling sudden demand increases.

As the organization continues to expand, management has identified infrastructure resilience as a strategic business priority.

## Business Scenario
Contoso Retail's web application currently operates on a single Azure Virtual Machine.

Although this architecture has successfully supported daily operations, it presents several operational and business risks. The application depends entirely on one server, creating a single point of failure.
If the virtual machine experiences:

- Hardware failure
- Operating system corruption
- Planned maintenance
- Azure host maintenance
- Network issues
- Unexpected software crashes

the entire website becomes unavailable until the issue is resolved.

## Business Challenges
The current infrastructure presents several challenges that limit business continuity and operational efficiency.

# Single Point of Failure
The web application is hosted on a single virtual machine. Any failure immediately results in complete service interruption.

# Limited Scalability
