# Multi-Tier Architecture: Nextcloud & MariaDB

## Overview
A multi-tier architecture separates an application into distinct, modular layers or tiers that run on separate infrastructure or containers. For this laboratory mission, we implemented a **Two-Tier Architecture** consisting of a Web/Application Tier and a Database Tier.

## The Web/Application Tier
* **Role**: The web and application tier serves as the user-facing interface and processing center.
* **Responsibilities**: It handles incoming HTTP requests from users on port `8080`, processes business logic, renders the Nextcloud user interface, and interacts with the database tier to fetch or store data. In our stack, this is powered by the **Nextcloud** container.

## The Database Tier
* **Role**: The database tier is dedicated to data persistence, management, and retrieval[cite: 1, 2].
* **Responsibilities**: It securely stores user credentials, configuration settings, and file metadata behind the scenes. By isolating the database, we ensure data integrity and security[cite: 1, 2]. In our stack, this is powered by the **MariaDB** container (`mariadb:10.6`)[cite: 1, 2].

## Why Separate Them?
Separating the web server and the database into two distinct containers instead of packing them into a single monolithic container is an industry best practice[cite: 1, 2]. It enhances security by isolating the database from direct public web exposure, improves scalability (allowing you to scale the web tier independently of the database), and simplifies maintenance and debugging when updating either component[cite: 1, 2].