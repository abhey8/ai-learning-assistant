# AI-Powered Learning Assistant — Document-Centric Study Platform

## Overview

**AI-Powered Learning Assistant** is a full-stack web application that transforms static study materials (PDFs) into interactive, personalized learning experiences using artificial intelligence.

Students often rely on PDFs for notes, textbooks, and reference material, but traditional study workflows are fragmented — reading in one app, note-taking in another, quizzes elsewhere, and progress tracking nowhere. This platform centralizes the entire learning process by combining **document management**, **AI-driven understanding**, **active recall tools**, and **progress analytics** into a single system.

By leveraging **Google Gemini AI**, the application enables users to chat with their documents, generate summaries, flashcards, quizzes, and track learning progress — all directly derived from their uploaded PDFs.

---

## Problem Statement

- **Passive learning from PDFs** — Reading PDFs alone leads to low retention and poor engagement.
- **Fragmented study tools** — Students switch between multiple apps for notes, quizzes, flashcards, and summaries.
- **Manual content creation** — Creating flashcards and quizzes manually is time-consuming.
- **Lack of personalization** — Traditional learning platforms do not adapt content to the learner’s documents.
- **No measurable progress tracking** — Students lack visibility into their learning activity and improvement.

---

## Scope

### In Scope
- Secure user authentication and authorization
- PDF upload, storage, and document management
- Embedded PDF reading experience
- AI-powered document interaction (chat, summaries, explanations)
- Automated generation of flashcards and quizzes
- Quiz evaluation and analytics
- Progress tracking dashboard with activity insights
- Responsive, modern UI for desktop and mobile

### Out of Scope (for Milestone 1)
- Collaborative learning (multi-user document sharing)
- Offline access to documents
- Mobile native applications
- Paid subscription or billing system
- Voice-based AI interaction

---

## Key Features

### 1. User Authentication
- Secure signup and login using JWT-based authentication
- Protected routes and user-specific data isolation

### 2. PDF Upload & Management
- Upload PDF study materials
- File size tracking and metadata storage
- Organized document library per user

### 3. Embedded PDF Viewer
- In-app PDF viewer for uninterrupted reading
- No need to download or open external applications

### 4. AI-Powered Document Chat
- Context-aware AI chat using Google Gemini
- Ask questions directly related to uploaded documents
- AI responses grounded in document content

### 5. AI Document Summary
- One-click generation of concise document summaries
- Useful for quick revision and overview

### 6. AI Concept Explainer
- Detailed explanations of selected topics or concepts
- Helps clarify complex sections from documents

### 7. Auto-Generated Flashcards
- AI-generated flashcards derived from document content
- Interactive flip-card UI
- Favorite important flashcards for quick revision

### 8. AI Quiz Generator
- Automatic multiple-choice quiz generation
- Configurable number of questions
- Questions aligned with document content

### 9. Quiz Results & Analytics
- Score calculation and performance breakdown
- Correct answers with explanations
- Review incorrect responses

### 10. Progress Tracking Dashboard
- Track number of uploaded documents
- Flashcards and quizzes generated
- Recent activity feed for learning consistency

### 11. Responsive UI
- Mobile-friendly, modern interface
- Built using Tailwind CSS

---

## Tech Stack

| Layer        | Technology |
|-------------|------------|
| Frontend    | React.js, Tailwind CSS |
| Backend     | Node.js, Express.js |
| Database    | MongoDB (Mongoose ODM) |
| AI          | Google Gemini API |
| Auth        | JWT (JSON Web Tokens) |
| File Storage| Local / Cloud Storage (configurable) |
| API         | RESTful APIs |

---

## Architecture Overview

- Client–Server architecture
- Frontend handles UI, PDF viewing, and user interactions
- Backend manages authentication, document processing, AI requests, and analytics
- AI layer processes document content and generates responses, summaries, quizzes, and flashcards
- Database layer stores users, documents, flashcards, quizzes, and progress data

---

## Design Principles

- Separation of concerns between UI, business logic, and data access
- Scalable REST API design
- Reusable frontend components
- Secure authentication and authorization
- AI-first feature design driven by document context

---

## Target Users

- College and university students
- Competitive exam aspirants
- Self-learners using PDFs as primary study material
- Educators preparing structured learning resources
