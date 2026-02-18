# ER Diagram — AI-Powered Learning Assistant

## Overview

This ER (Entity–Relationship) diagram represents the database design of the **AI-Powered Learning Assistant** system.  
It focuses on how data is structured, stored, and related within the application.

The diagram models users, documents, AI-generated learning resources, and progress tracking using standard ER concepts.

---

## Entities and Attributes

### User
- userId (PK)
- name
- email
- passwordHash
- createdAt

---

### Document
- documentId (PK)
- title
- filePath
- fileSize
- uploadedAt
- userId (FK)

---

### Flashcard
- flashcardId (PK)
- question
- answer
- isFavorite
- documentId (FK)

---

### Quiz
- quizId (PK)
- title
- totalQuestions
- documentId (FK)

---

### Question
- questionId (PK)
- questionText
- options
- correctAnswer
- quizId (FK)

---

### QuizResult
- resultId (PK)
- score
- submittedAt
- userId (FK)
- quizId (FK)

---

### Progress
- progressId (PK)
- totalDocuments
- totalFlashcards
- totalQuizzes
- lastActivity
- userId (FK)

---

## Relationships

- One **User** can upload many **Documents** (1:N)
- One **Document** can generate many **Flashcards** (1:N)
- One **Document** can generate many **Quizzes** (1:N)
- One **Quiz** contains many **Questions** (1:N)
- One **User** can have multiple **QuizResults** (1:N)
- Each **User** has exactly one **Progress** record (1:1)

---

## ER Diagram

![alt text](<Screenshot 2026-02-18 at 8.06.02 PM.png>)

---

## Notes

- Primary Keys (PK) uniquely identify each entity.
- Foreign Keys (FK) establish relationships between entities.
- The ER diagram strictly represents database structure and does not include application logic.
- The design supports scalability and efficient querying for AI-driven learning features.

