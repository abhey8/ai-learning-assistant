# Use Case Diagram — AI-Powered Learning Assistant

## Overview

This document describes the use case diagram for the **AI-Powered Learning Assistant** platform.  
The diagram illustrates how users interact with the system to upload study documents, use AI-powered learning tools, and track their academic progress.

The platform focuses on transforming static PDF-based study material into an interactive learning experience using artificial intelligence.

---

## Actors

- **User (Student)**  
  Primary actor who uploads documents, interacts with AI features, and tracks learning progress.

- **AI System (Google Gemini)**  
  Processes document content and generates intelligent outputs such as answers, summaries, flashcards, and quizzes.

- **Backend System**  
  Handles authentication, document storage, analytics, and coordination between frontend and AI services.

---

## Use Case Diagram

![alt text](<Screenshot 2026-02-18 at 7.42.24 PM.png>)


---

## Use Case Descriptions

| #    | Use Case                     | Actors              | Description |
|-----|------------------------------|---------------------|-------------|
| UC1 | Register / Login              | User, Backend       | User registers or logs in using secure JWT-based authentication. |
| UC2 | Manage Profile               | User                | User updates personal information and account settings. |
| UC3 | Upload PDF                   | User, Backend       | User uploads PDF study documents to the system for processing and storage. |
| UC4 | View PDF                     | User                | User reads documents using the embedded PDF viewer within the application. |
| UC5 | Chat with Document           | User, AI System     | User asks questions related to document content and receives AI-generated answers. |
| UC6 | Generate Document Summary    | User, AI System     | AI generates a concise summary of the selected document. |
| UC7 | Explain Concept              | User, AI System     | AI provides detailed explanations for specific topics from the document. |
| UC8 | Generate Flashcards          | User, AI System     | AI automatically creates flashcards based on document content. |
| UC9 | Mark Favorite Flashcards     | User                | User marks important flashcards for quick review. |
| UC10| Generate Quiz                | User, AI System     | AI generates multiple-choice quizzes from document content. |
| UC11| View Quiz Results            | User                | User views quiz scores, correct answers, and explanations. |
| UC12| Track Learning Progress      | User, Backend       | User views dashboard showing documents, quizzes, flashcards, and recent activity. |

---

## Notes

- All AI-generated outputs are derived strictly from the uploaded document content.
- Each user can access only their own documents and generated learning data.
- The system is designed to support scalability and future feature expansion.

