# Class Diagram — AI-Powered Learning Assistant

## Overview

This class diagram represents the static structure of the **AI-Powered Learning Assistant** system.  
It shows the core classes, their responsibilities, and relationships used to support AI-based document learning.

---

## Main Classes

### User
- id, name, email, passwordHash
- login(), logout()

### Document
- id, title, filePath, fileSize
- generateSummary(), generateFlashcards(), generateQuiz()

### Flashcard
- id, question, answer, isFavorite

### Quiz
- id, title, totalQuestions
- startQuiz(), submitQuiz()

### Question
- id, questionText, options, correctAnswer

### QuizResult
- id, score, submittedAt
- calculateScore()

### Progress
- totalDocuments, totalFlashcards, totalQuizzes, lastActivity
- updateProgress()

---

## Service Classes

- **AuthService** — login(), register(), validateToken()
- **DocumentService** — uploadPDF(), fetchDocuments()
- **AIService** — generateResponse(), generateSummary(), generateFlashcards(), generateQuiz()
- **QuizService** — createQuiz(), evaluateQuiz()
- **FlashcardService** — createFlashcards(), markFavorite()

---

## Class Diagram

![alt text](<Screenshot 2026-02-18 at 7.58.10 PM.png>)

---

## Relationships

- User → Document (one-to-many)
- Document → Flashcard (one-to-many)
- Document → Quiz (one-to-many)
- Quiz → Question (one-to-many)
- User → Progress (one-to-one)
- Services depend on domain classes

