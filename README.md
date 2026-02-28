# AI Contribution Detection Tool

A tool that analyzes GitHub commits and code to detect AI-generated contributions and improve transparency in software development.

---

## 1. Problem Statement

### Problem Title

Detecting AI-Generated Contributions in GitHub Repositories

### Problem Description

Developers increasingly use AI tools like ChatGPT and Copilot to generate commit messages, code snippets, documentation, and pull requests. However, Git platforms currently have no system to detect or track AI-generated contributions, leading to issues in transparency, accountability, and code quality.

### Target Users

* Software development teams
* Open-source maintainers
* Academic institutions
* Companies enforcing AI usage policies

### Existing Gaps

* No automated detection of AI-generated commits
* No analytics on AI usage in repositories
* No transparency on AI-assisted contributions
* Difficulty enforcing policies on AI usage

---

## 2. Problem Understanding & Approach

### Root Cause Analysis

AI tools generate high-quality text and code that is difficult to distinguish from human work. Developers may submit AI-generated code without full understanding, creating risks in security and maintainability.

### Solution Strategy

Create a tool that analyzes commit messages and code patterns using rule-based heuristics or ML models to assign an **AI Likelihood Score** and provide analytics.

---

## 3. Proposed Solution

### Solution Overview

A web tool that checks commit messages and code snippets to estimate whether they were AI-generated.

### Core Idea

Use pattern detection (language style, repetition, formatting) to identify AI-like behavior.

### Key Features

* Detect AI-style commit messages
* Detect AI-generated code patterns
* Assign AI Likelihood Score
* Contributor-level analytics
* Repository-level AI usage trends

---

## 4. System Architecture

        User
         ↓
Frontend (React Web App)
         ↓
Backend API (Node.js / Python)
        ↓
AI Detection Logic
        ↓
Database (Store commits & scores)
        ↓
Response back to User


### High-Level Flow

User → Frontend → Backend → Detection Logic → Database → Response

### Architecture Description

Users submit commit messages or code snippets through the frontend. The backend processes input using rule-based or ML detection logic and stores results in a database. The system returns AI Likelihood Score and analytics.

### Architecture Diagram

(To be added)

---

## 5. Database Design

### ER Diagram

(To be added)

### ER Diagram Description

Database will store:

* User details
* Repository details
* Commit data
* AI Likelihood scores
* Analytics reports

---

## 6. Dataset Selected

### Dataset Name

Sample GitHub Commit Dataset (Public repositories)

### Source

GitHub public repositories / manually collected commits

### Data Type

Text data (commit messages) + code snippets

### Selection Reason

Needed real commit messages and code samples to identify AI-like patterns.

### Preprocessing Steps

* Remove duplicates
* Clean formatting
* Tokenize text
* Normalize code structure

---

## 7. Model Selected

### Model Name

Rule-based Heuristic Detection (Initial Version)

### Selection Reasoning

Hackathon time limit requires a simple but working prototype.

### Alternatives Considered

* GPT-based classifier
* BERT text classifier
* Code similarity models

### Evaluation Metrics

* Accuracy
* Precision
* Recall
* False Positive Rate

---

## 8. Technology Stack

### Frontend

HTML, CSS, JavaScript / React

### Backend

Node.js / Python Flask

### ML/AI

Rule-based detection (future: ML model)

### Database

MongoDB / SQLite

### Deployment

Vercel / Render / Localhost

---

## 9. API Documentation & Testing

### API Endpoints List

* `/analyzeCommit` – Analyze commit message
* `/analyzeCode` – Analyze code snippet
* `/getAnalytics` – Show AI usage stats

### API Testing Screenshots

(To be added)

---

## 10. Module-wise Development & Deliverables

### Checkpoint 1: Research & Planning

* Finalize idea
* Create README
* Define architecture

### Checkpoint 2: Backend Development

* Create detection logic
* Build API endpoints

### Checkpoint 3: Frontend Development

* Create UI for input/output
* Display AI scores

### Checkpoint 4: Model Training

* Improve rule-based detection
* Test dataset

### Checkpoint 5: Model Integration

* Connect frontend with backend

### Checkpoint 6: Deployment

* Deploy app
* Final demo

---

## 11. End-to-End Workflow

1. User submits commit message/code
2. Frontend sends request
3. Backend analyzes text/code
4. Detection logic calculates score
5. Database stores result
6. Analytics generated
7. User receives report

---

## 12. Demo & Video

* Live Demo Link: To be added
* Demo Video Link: To be added
* GitHub Repository: To be added

---

## 13. Hackathon Deliverables Summary

* AI Contribution Detection Tool prototype
* Rule-based detection system
* Analytics dashboard
* GitHub repository with documentation

---

## 14. Team Roles & Responsibilities

| Member Name | Role                    | Responsibilities                         |
| ----------- | ----------------------- | ---------------------------------------- |
| Yash Borkar | ----------------------- | ---------------------------------------- |
| Sachit Kumar| ----------------------- | ---------------------------------------- |
|Azmol Wasim Hussain | ----------------------- | ---------------------------------------- |

---

## 15. Future Scope & Scalability

### Short-Term

* Improve detection accuracy
* GitHub API integration

### Long-Term

* ML-based detection model
* Browser extension
* Enterprise compliance dashboard

---

## 16. Known Limitations

* Rule-based detection not 100% accurate
* Limited dataset
* Cannot fully prove AI usage

---

## 17. Impact

* Improves transparency in software teams
* Helps detect risky AI-generated code
* Supports academic and enterprise integrity policies
