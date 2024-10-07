# Expense Tracker App

## Overview
The **Expense Tracker App** helps users manage their personal finances by allowing them to log expenses, track categorized spending, and generate reports. It also offers future scope for automatic expense tracking via SMS parsing and notification features through WhatsApp and SMS.

## Functional Requirements
- **User Authentication**: Users can log in and sign up to the application.
- **Manual Expense Management**: Users can add or remove expenses manually.
- **Expense Overview**: Users can view categorized expenses.
- **Reports and Statistics**: Users can generate weekly, monthly, and yearly reports showing statistics about their spending.

## Non-Functional Requirements
- **Fault Tolerant and Scalable**: The system is designed to be fault-tolerant and scalable, ensuring a latency of less than 100ms.
- **Config-Driven**: The system should support a configuration-driven approach to minimize code changes in the future.

## Future Scope
- **Financial Behavior Tracking**: Users can track their financial behavior and receive tips for improvement.
- **Automated Expense Tracking**: The app will be able to automatically add expenses by reading and parsing SMS messages if the user grants the necessary permissions.
- **Notifications**: The app will send notifications via WhatsApp and SMS regarding overspending, financial risks, and other indicators.

## System Architecture
The system is built on microservices architecture with the following components:

- **Client**: The user interface through which users interact with the app.
- **API Gateway**: Manages all client requests and handles tokenization for security.
- **Auth Service**: Responsible for user authentication and authorization.
- **Notification Service**: Sends notifications to users via various channels.
- **Templatisation Service**: Manages notification templates for sending customized messages.
- **User Service**: Handles all user-related information and operations.
- **Billing Service**: Manages user billing and payments.
- **Ledger Service**: Records and maintains all transaction data for users.
- **Reporting Service**: Generates reports based on user data, providing insights into spending behavior.

### System Diagram
![System Architecture](link_to_diagram_image)

## Tools and Technologies Used

- **Redis**: In-memory data structure store, used for caching.
- **RabbitMQ**: Message broker for asynchronous communication between microservices.
- **Docker**: Containerization for easy deployment across environments.
- **Kafka**: Distributed streaming platform for handling real-time data pipelines.
- **Kubernetes**: Orchestrates and manages containerized applications, enabling scaling.
- **Kong**: An API gateway for managing and monitoring API traffic.

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/expense-tracker-app.git
   cd expense-tracker-app
