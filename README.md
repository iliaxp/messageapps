# MessageApp

A Full-Stack Real-Time Messaging Application

MessageApp is a full-stack messaging platform built with Kotlin, Java, Spring Boot, and React. It combines a native Android application, a backend API, and a web-based administration panel into one integrated system.

The project focuses on modern application architecture, real-time communication, database management, and reliable deployment.

## Features & Components

- Android Application: Native Android client developed with Kotlin.
- Backend API: Java and Spring Boot backend.
- REST API: Structured API endpoints for client-server communication.
- Real-Time Communication: WebSocket-based communication infrastructure.
- Admin Panel: Web-based administration interface.
- Database: PostgreSQL for persistent data storage.
- Deployment: Docker Compose and Nginx infrastructure.

## Technology Stack

| Technology     | Purpose                     |
| -------------- | --------------------------- |
| Kotlin         | Android Development         |
| Java           | Backend Development         |
| Spring Boot    | Backend Framework           |
| PostgreSQL     | Database                    |
| REST API       | Client-Server Communication |
| WebSocket      | Real-Time Communication     |
| React          | Admin Panel                 |
| Docker         | Containerization            |
| Docker Compose | Service Orchestration       |
| Nginx          | Reverse Proxy               |
| Git            | Version Control             |

## System Architecture

The application follows a multi-component architecture in which the Android client and administration panel communicate with the central backend.

```
                    ┌──────────────────┐
                    │   Android App    │
                    │      Kotlin      │
                    └────────┬─────────┘
                             │
                    ┌────────▼─────────┐
                    │  Nginx Reverse   │
                    │      Proxy       │
                    └────────┬─────────┘
                             │
                    ┌────────▼─────────┐
                    │   Spring Boot    │
                    │    Backend      │
                    └───────┬──────────┘
                            │
                 ┌──────────┴──────────┐
                 │                     │
        ┌────────▼────────┐   ┌────────▼────────┐
        │   PostgreSQL    │   │  WebSocket API  │
        │    Database    │   │ Real-Time Layer │
        └─────────────────┘   └─────────────────┘

                    ┌──────────────────┐
                    │   Admin Panel    │
                    │      React       │
                    └──────────────────┘
```

## Project Structure

```
messageapps/
├── SpringBoot/          # Spring Boot backend
├── app/                 # Android application
├── admin-panel/         # Web administration panel
├── nginx/               # Nginx configuration
├── gradle/              # Gradle wrapper
├── docker-compose.yml   # Docker orchestration
├── .env.example         # Environment variables template
├── DEPLOYMENT.md        # Deployment documentation
└── README.md
```

## Getting Started

### Prerequisites

- Java JDK
- Android Studio
- Docker Engine
- Docker Compose
- Git

### 1. Clone the Repository

```
git clone https://github.com/iliaxp/messageapps.git

cd messageapps
```

### 2. Configure Environment

Create your environment file:

```
cp .env.example .env
```

Configure the required environment variables before starting the services.

### 3. Start the Backend Infrastructure

```
docker compose up -d --build
```

Check running containers:

```
docker compose ps
```

View application logs:

```
docker compose logs -f
```

### 4. Run the Android Application

1. Open the project in Android Studio.
2. Configure the backend API and WebSocket URLs.
3. Sync the Gradle project.
4. Build and run the application.

## Communication

The system uses two communication approaches:

REST API

Used for standard HTTP-based client-server operations and backend integration.

WebSocket

Provides persistent connections for real-time communication between connected clients and the backend.

## Deployment

The project includes Docker-based deployment infrastructure with the following components:

- Spring Boot backend
- PostgreSQL database
- React administration panel
- Nginx reverse proxy

For detailed deployment instructions, configuration, and server setup, see DEPLOYMENT.md.

## Engineering Highlights

This project demonstrates practical experience in:

- Full-stack application architecture
- Java and Spring Boot development
- RESTful API design and integration
- Real-time communication
- PostgreSQL database management
- Native Android development with Kotlin
- Docker-based deployment
- Backend and infrastructure integration

## Author

Ilia XP

GitHub: [@iliaxp](https://github.com/iliaxp?utm_source=chatgpt.com)
