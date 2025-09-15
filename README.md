# Xeno CRM Platform

A Mini CRM Platform that enables customer segmentation, personalized campaign delivery, and intelligent insights using modern tools and approaches.

## Features

### 1. Data Ingestion APIs
- Secure, well-documented REST APIs to ingest customers and orders data
- Pub-sub architecture using a message broker where API layer handles validation and data persistence happens asynchronously

### 2. Campaign Creation UI
- Define audience segments using flexible rule logic
- Combine conditions using AND/OR with a dynamic rule builder
- Preview audience size before saving the segment
- Campaign history page showing past campaigns and delivery stats

### 3. Campaign Delivery & Logging
- Store campaign details in a communication_log table
- Send personalized messages to customers via a dummy vendor API
- Update delivery status in the communication log

### 4. Authentication
- Google OAuth 2.0-based authentication
- Secure access to campaign creation and viewing

### 5. AI Integration
- Natural Language to Segment Rules
- AI-Driven Message Suggestions
- Campaign Performance Summarization
- Smart Scheduling Suggestions
- Audience Lookalike Generator
- Auto-tagging Campaigns

## Tech Stack

### Frontend
- Next.js
- React
- Tailwind CSS

### Backend
- Java Spring Boot
- Spring Security
- Spring Data JPA

### Database
- MySQL

### Message Broker
- Kafka

### AI Integration
- Google Gemini API

## Getting Started

### Prerequisites
- Node.js and npm
- Java 17+
- Maven
- MySQL
- Kafka

### Installation

#### Frontend Setup

1. Navigate to the frontend directory:
   ```
   cd frontend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Create a `.env.local` file with the following variables:
   ```
   BACKEND_URL=http://localhost:8080
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=your-secret-key
   GOOGLE_CLIENT_ID=your-google-client-id
   GOOGLE_CLIENT_SECRET=your-google-client-secret
   GEMINI_API_KEY=your-gemini-api-key
   ```

4. Start the development server:
   ```
   npm run dev
   ```

#### Backend Setup

1. Navigate to the backend directory:
   ```
   cd backend
   ```

2. Configure the `application.properties` file with your database and Kafka settings.

3. Build the application:
   ```
   ./mvnw clean package
   ```

4. Run the application:
   ```
   ./mvnw spring-boot:run
   ```

## API Documentation

API documentation is available via Swagger UI at `/swagger-ui.html` when the backend is running.

## Project Structure

```
Xeno_CRM/
├── frontend/                # Next.js frontend application
│   ├── src/
│   │   ├── app/             # Next.js app router pages
│   │   ├── components/       # Reusable React components
│   │   └── providers/        # Context providers
│   ├── public/               # Static assets
│   └── package.json          # Frontend dependencies
│
├── backend/                  # Spring Boot backend application
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/        # Java source code
│   │   │   └── resources/   # Application properties and resources
│   │   └── test/            # Test files
│   └── pom.xml              # Backend dependencies
│
└── README.md                # Project documentation
```