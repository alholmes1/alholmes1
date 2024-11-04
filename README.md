**Inventory Management System (IMS) - Software Requirements Specification**  
**Version 2**

**Team Number:** 18  
**Project Manager:** Arthur Holmes  
**Team Members:** Natiza Dahal, Jack Stahl, Artemio Cortez, Trent Little, Zayd Silwan

---

### Revisions

| Version | Primary Author(s) | Description of Version  | Date Completed |
|---------|--------------------|-------------------------|----------------|
| 1.0     | Arthur Holmes      | Initial Document       | [10/29/24]        |
| 2.0     | Arthur Holmes      | Revised Document       | [11/3/24]    |

---

### Review History

| Reviewer      | Version Reviewed | Date       |
|---------------|------------------|------------|
| [Team 18] | 1.0              | [10/24]     |
| [Team 18] | 2.0              | [11/24] |

---

### Table of Contents (Version 2)

1. **Introduction**
   1.1 Project Objectives  
   1.2 Project Scope  
   1.3 Project Overview  
2. **Project Description**
   2.1 Project Features / Functions  
   2.2 User Stories  
   2.3 Use Cases  
   2.4 Project Assumptions and Dependencies  
3. **Project Collaboration and Documentation**  
4. **Project Management**  
5. **Requirements Specification**
   5.1 Business Requirements  
   5.2 User Requirements  
   5.3 Functional Requirements  
   5.4 Non-Functional Requirements  
   5.5 Implementation (Performance) Requirements (Optional)  
6. **High-level Design**
   6.1 Security (Required)  
   6.2 Hardware (Required)  
   6.3 User Experience (Required)  
   6.4 Architecture (Required)  
   6.5 Database (Required)  
   6.6 Top-level Classes (Required)  
   6.7 Data Flow and States (Required)  
   6.8 Reports (Required)  
   6.9 Internal Interfaces (Optional)  
   6.10 External Interfaces (Optional)  
   6.11 Other Outputs (Optional)  
   6.12 Configuration Data (Optional)  
   6.13 Training (Optional)  
7. **Appendixes (Optional)**  

---

### 1. Introduction

#### 1.1 Project Objectives
Define a comprehensive, user-friendly IMS that streamlines inventory tracking, improves stock accuracy, and enables real-time visibility across multiple warehouses. The system aims to support timely restocking, automated alerts, and efficient demand order management.

#### 1.2 Project Scope
- **Included:** Real-time stock tracking, restock alerts, multi-warehouse inventory coordination, demand order management, and reporting tools.
- **Excluded:** Logistics and delivery management, customer relationship management.

#### 1.3 Project Overview
This project will develop an IMS for Acme Inc., designed to meet warehouse needs and provide inventory insights across multiple locations. Key phases include development (backend with Flask, frontend with Vue.js and Bootstrap), testing (using pytest), and deployment (on AWS EC2 and S3). Expected outcomes include a robust, scalable system with features like multi-warehouse coordination and automated restocking alerts.

---

### 2. Project Description

#### 2.1 Project Features / Functions
1. Real-time Stock Tracking
2. Automated Restock Alerts
3. Demand Order and Inventory Correction Logging

#### 2.2 User Stories
- As a warehouse manager, I want to sort products by brand/type so I can quickly locate items.
- As a warehouse supervisor, I want automated restock alerts to prevent stockouts.
- As a sales manager, I want access to a dashboard for demand order management.

#### 2.3 Use Cases
- **Use Case 1:** Warehouse Manager sorting products by type
- **Use Case 2:** Warehouse Supervisor receiving restock alerts
- **Use Case 3:** Sales Manager viewing demand order metrics

#### 2.4 Project Assumptions and Dependencies
- **Assumptions:** Users have internet access, AWS infrastructure for hosting, team members familiar with Flask, MySQL.
- **Dependencies:** AWS EC2 and S3 for hosting, MySQL for data management, Flask and Vue.js for development.

---

### 3. Project Collaboration and Documentation

Your group will use GitHub for version control and documentation storage, Slack for team communication, and Trello for project tracking and task management.

---

### 4. Project Management

The team will follow Agile methodologies, using Trello for sprint planning and tracking, with weekly progress reviews.

---

### 5. Requirements Specification

#### 5.1 Business Requirements

| Requirement ID | Requirement Description                                         | MOSCOW |
|----------------|-----------------------------------------------------------------|--------|
| BR1            | The system must support real-time inventory tracking.           | M      |
| BR2            | The system should enable automated restock alerts.              | S      |
| BR3            | The system must provide a dashboard for demand order insights.  | M      |

#### 5.2 User Requirements

| Requirement ID | Requirement Description                                                 | MOSCOW |
|----------------|-------------------------------------------------------------------------|--------|
| UR1            | Users must be able to view real-time stock levels across warehouses.    | M      |
| UR2            | Users should receive alerts for low stock levels.                       | S      |
| UR3            | Users must be able to log inventory corrections.                        | M      |

#### 5.3 Functional Requirements

| Requirement ID | Requirement Description                                                    | MOSCOW |
|----------------|---------------------------------------------------------------------------|--------|
| FR1            | The application shall provide real-time stock data updates.               | M      |
| FR2            | The system shall enable setting thresholds for automated restock alerts. | S      |
| FR3            | The application shall log demand orders and corrections.                  | M      |

#### 5.4 Non-Functional Requirements

| Requirement ID | Requirement Description                                                  | MOSCOW |
|----------------|-------------------------------------------------------------------------|--------|
| NFR1           | The system shall have a responsive interface for mobile/desktop use.    | M      |
| NFR2           | The application shall handle up to 10,000 items per warehouse.          | M      |
| NFR3           | The system should have less than 1-second response time for queries.    | S      |

#### 5.5 Implementation Requirements (Optional)

| Requirement ID | Requirement Description                                                | MOSCOW |
|----------------|-----------------------------------------------------------------------|--------|
| IR1            | Development shall use Flask (Python) as the primary backend framework. | M      |

---

### 6. High-level Design

#### 6.1 Security (Required)
- **Specification 1:** User Authentication - Secure login with encrypted credentials.
- **Specification 2:** Access Control - Limit data access by user roles.

#### 6.2 Hardware (Required)
- **Specification 1:** AWS EC2 instances to host backend services.
- **Specification 2:** S3 for storing backup data.
- **Specification 3:** Cloud-based database server.

#### 6.3 User Experience (Required)
- **Specification 1:** Simple, responsive dashboard for inventory tracking.
- **Specification 2:** Alerts/notifications for low stock.

#### 6.4 Architecture (Required)
- **Specification 1:** Client-server model using Flask and Vue.js.
- **Specification 2:** REST API for backend communication.

#### 6.5 Database (Required)
- **Specification 1:** MySQL for main data storage.
- **Specification 2:** Data replication for backup.

### 7 Key Stakeholders 

| Role                       | Stakeholder Name                                     | Responsibility / Interest                                                  |
|----------------------------|-----------------------------------------------------|---------------------------------------------------------------------------|
| Project Sponsor             | [Name/Position]                                    | Provides project funding and high-level project guidance.                 |
| Project Manager             | Arthur Holmes                                       | Oversees project timeline, budget, and team coordination.                |
| Warehouse Managers          | [Name/Position]                                    | Responsible for daily warehouse operations, inventory accuracy, and overseeing stock levels. Need real-time insights into inventory, automated restock alerts, and reporting tools. |
| Sales and Operations Managers| [Name/Position]                                   | Oversee sales and order fulfillment; rely on inventory data to ensure stock availability. Need access to a dashboard showing demand order statuses and inventory levels for efficient prioritization. |
| Supply Chain Managers       | [Name/Position]                                    | Ensure product availability across warehouses and manage distribution and restocking logistics. Require functionality for multi-warehouse coordination and insights into inventory levels. |
| IT and Development Teams    | Natiza Dahal, Jack Stahl, Artemio Cortez, Trent Little, Zayd Silwan | Handle technical implementation, maintenance, and updates to the system. Need clear documentation, a robust development environment, and reliable deployment on AWS. |
| Finance and Accounting Teams | [Name/Position]                                    | Track inventory value, losses, and stock movements, impacting financial reporting and cost controls. Need detailed reporting on inventory metrics and real-time data integration for financial accuracy. |
| Executive Leadership (e.g., CIO, CFO, CEO) | [Name/Position]          | Interested in the high-level value the IMS brings, such as operational efficiency, cost savings, and scalability. Require reports and KPIs that show the system’s impact on inventory accuracy, cost reduction, and stock management efficiency. |
| End Users (Warehouse Staff) | [Position/Role]                                    | Use the system for daily tasks like tracking stock levels, sorting inventory, and logging inventory corrections. Require a user-friendly interface and training to operate the IMS efficiently. |
| System Administrator        | [Name/Position]                                    | Manages system configuration, maintenance, and updates.                   |

### Additional Requirements
- **Database Capacity**: The IMS should support a database capacity of up to 10,000 unique SKUs and handle 100+ simultaneous users without significant lag.

These stakeholders will have different requirements, which will need to be balanced to ensure the IMS meets organizational goals and operational efficiency. Feel free to fill in the placeholders with actual names and positions as needed.

