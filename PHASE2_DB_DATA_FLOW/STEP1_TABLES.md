# STEP1_TABLES.md
Database tables definitions, fields, types, and constraints

This file contains all core database tables for NS-ETHIODIGITAL, including:

## 1. Schools
- id (PK, int, auto-increment)
- name (varchar)
- address (varchar)
- created_at (timestamp)
- updated_at (timestamp)

## 2. Users
- id (PK, int, auto-increment)
- school_id (FK → Schools.id)
- role (enum: Admin, Teacher, Student)
- name (varchar)
- email (varchar)
- password_hash (varchar)
- created_at, updated_at

## 3. Exams
- id (PK)
- teacher_id (FK → Users.id)
- title (varchar)
- description (text)
- time_limit (int, minutes)
- created_at, updated_at

## 4. Item Bank
- id (PK)
- question_text (text)
- type (enum: MCQ, TF, Matching)
- options (JSON, nullable)
- answer_key (text)
- created_at, updated_at

## 5. Exam Items
- id (PK)
- exam_id (FK → Exams.id)
- item_id (FK → Item Bank.id)
- sequence_order (int)
- created_at, updated_at

## 6. Responses
- id (PK)
- student_id (FK → Users.id)
- exam_id (FK → Exams.id)
- item_id (FK → Exam Items.id)
- answer (text)
- created_at, updated_at

## 7. Results
- id (PK)
- exam_id (FK → Exams.id)
- student_id (FK → Users.id)
- total_score (int)
- status (enum: pass, fail)
- created_at, updated_at
