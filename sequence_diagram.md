
# Sequence Diagram — AI-Powered Learning Assistant

## Overview

This document describes the sequence diagram for the **AI-Powered Learning Assistant** platform.  
The sequence diagram illustrates the step-by-step interaction between the user, frontend, backend, database, and AI service during document upload and AI-powered learning operations.

The diagram focuses on the primary learning flow, from authentication to AI-based document interaction.

---

## Participants

- **User (Student)**  
  Initiates actions such as login, document upload, and AI interactions.

- **Frontend (React Web Application)**  
  Handles user interface, PDF viewing, and communication with backend services.

- **Backend Server (Node.js / Express)**  
  Manages authentication, business logic, document processing, and AI coordination.

- **Database (MongoDB)**  
  Stores user data, documents, flashcards, quizzes, and progress information.

- **AI Service (Google Gemini API)**  
  Processes document context and generates intelligent responses, summaries, flashcards, and quizzes.

---

## Sequence Diagram

![alt text](<Screenshot 2026-02-18 at 7.53.50 PM.png>)

---

## Interaction Flow Description

### 1. User Authentication
1. The user submits login credentials through the frontend.
2. The frontend sends authentication data to the backend server.
3. The backend validates credentials using the database.
4. Upon successful validation, the backend generates a JWT token.
5. The frontend receives the token and grants access to protected features.

### 2. PDF Upload and Storage
6. The user uploads a PDF document via the frontend.
7. The frontend sends the document and metadata to the backend.
8. The backend stores the PDF and related metadata in the database.
9. The backend confirms successful upload to the frontend.

### 3. AI-Powered Document Interaction
10. The user opens the document and submits a query through the AI chat interface.
11. The frontend sends the query along with document reference to the backend.
12. The backend extracts relevant document content.
13. The backend sends the query and extracted context to the Google Gemini AI service.
14. The AI service processes the request and returns a response.
15. The backend forwards the AI-generated response to the frontend.
16. The frontend displays the response to the user.

---

## Notes

- All AI responses are generated strictly based on the uploaded document content.
- User data and documents are isolated per account to ensure security and privacy.
- The sequence diagram represents the primary system flow; additional AI features such as summaries, flashcards, and quizzes follow a similar interaction pattern.

