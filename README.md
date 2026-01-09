# Task Management System (Jira Clone)

Welcome to the central manifest for the **Task Management System**. This project is built using a microservices architecture with **Spring Boot** for the backend and **React (Vite)** for the frontend.

## 📂 Repository Index

Below are the links to the individual repositories for each service.

### 🖥️ Frontend
*   **[TaskFlow Client Application](INSERT_FRONTEND_REPO_LINK_HERE)**  
    *Tech Stack:* React, TypeScript, TailwindCSS, Vite
    *Description:* The main user interface for the task management system.

### 🏗️ Infrastructure Services
*   **[Service Registry (Eureka)](INSERT_REGISTRY_REPO_LINK_HERE)**  
    *Port:* `8761`  
    *Description:* Handles service discovery for all microservices.
*   **[API Gateway](INSERT_GATEWAY_REPO_LINK_HERE)**  
    *Port:* `8080`  
    *Description:* First point of entry, handles routing and centralized authentication.

### 🔌 Core Microservices
*   **[User Management Service (UMS)](INSERT_USER_SERVICE_REPO_LINK_HERE)**  
    *Description:* Handles user registration, authentication (JWT), and profile management.
*   **[Project Service](INSERT_PROJECT_SERVICE_REPO_LINK_HERE)**  
    *Description:* Manages project workspaces, teams, and member assignments.
*   **[Task Service](INSERT_TASK_SERVICE_REPO_LINK_HERE)**  
    *Description:* core logic for creating, updating, and assigning tasks/issues.
*   **[Kanban Service](INSERT_KANBAN_SERVICE_REPO_LINK_HERE)**  
    *Description:* Manages board columns and drag-and-drop state updates.
*   **[Notification Service](INSERT_NOTIFICATION_SERVICE_REPO_LINK_HERE)**  
    *Description:* Handles email and system notifications for task updates.

---

## 🚀 Quick Start Guide

To run the entire system locally:

1.  **Infrastructure First**:
    *   Start **Service Registry** (`taskflow-service-registry`).
    *   Start **API Gateway** (`api-gateway`).
2.  **Backends**:
    *   Start `taskflow-user-service`.
    *   Start `project-service`, `task-service`, `kanban-service`, `notification-service`.
3.  **Frontend**:
    *   Go to `taskflow` directory.
    *   Run `npm install` then `npm run dev`.

## 📐 Architecture

*   **Database**: PostgreSQL / MySQL (per service)
*   **Communication**: Feign Clients (Synchronous), Kafka/RabbitMQ (Asynchronous - if applicable)
*   **Security**: JWT Authentication via API Gateway
