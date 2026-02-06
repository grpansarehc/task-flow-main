# Task Management System (Jira Clone)

Welcome to the central manifest for the **Task Management System**. This project is built using a microservices architecture with **Spring Boot** for the backend and **React (Vite)** for the frontend.

## 📂 Repository Index

Below are the links to the individual repositories for each service.

### 🖥️ Frontend
*   **[TaskFlow Client Application](https://github.com/grpansarehc/taskflow-frontend)**  
    *Tech Stack:* React, TypeScript, TailwindCSS, Vite
    *Description:* The main user interface for the task management system.

### 🏗️ Infrastructure Services
*   **[Service Registry (Eureka)](https://github.com/ManishShettyHumanCloud/taskflow-service-registry)**  
    *Port:* `8761`  
    *Description:* Handles service discovery for all microservices.
*   **[API Gateway](https://github.com/grpansarehc/taskflow-api-gateway)**  
    *Port:* `8080`  
    *Description:* First point of entry, handles routing and centralized authentication.
*   **[TaskFlow Infrastructure](https://github.com/ManishShettyHumanCloud/taskflow-infra.git)**
    *Description:* Central repository for GitOps configurations (ArgoCD), Kubernetes manifests, and infrastructure setup.

### 🔌 Core Microservices
*   **[User Management Service (UMS)](https://github.com/ManishShettyHumanCloud/taskflow-user-service)**  
    *Description:* Handles user registration, authentication (JWT), and profile management.
*   **[Project Service](https://github.com/grpansarehc/taskflow-project-service)**  
    *Description:* Manages project workspaces, teams, and member assignments.
*   **[Task Service](https://github.com/ManishShettyHumanCloud/taskflow-task-service)**  
    *Description:* core logic for creating, updating, and assigning tasks/issues.
*   **[Kanban Service](https://github.com/grpansarehc/taskflow-kanban-service)**  
    *Description:* Manages board columns and drag-and-drop state updates.
*   **[Notification Service](https://github.com/grpansarehc/taskflow-notification-service)**  
    *Description:* Handles email and system notifications for task updates.

### 🚧 Missing & Planned Features

While the core functional modules are established, the following features are currently in development or planned for the roadmap:

*   **Comment Service (`cms`)**: Dedicated microservice for task comments, threading, and reactions (Currently in development).
*   **Advanced Search**: Full-text search capability (e.g., via Elasticsearch) for tasks and projects.
*   **Analytics & Reporting**: comprehensive dashboards for burndown charts, velocity tracking, and user performance.
*   **File Attachments**: Support for file uploads and management via S3 or MinIO.
*   **Real-time Updates**: WebSocket integration for instant Kanban board and notification updates.

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


