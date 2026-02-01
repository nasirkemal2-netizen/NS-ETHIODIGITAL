# STEP1: Entities / Core Components

## Schools
- school_id (unique)
- name
- address
- status (active/inactive)

## Users
- user_id
- name
- email/login
- role (Admin, Teacher, Student)
- school_id

## Item Bank
- item_id
- content (question text)
- item_type (MCQ / TF / Matching)
- correct_answer
- created_by

## Exams
- exam_id
- title
- school_id
- teacher_id
- time_limit
- allowed_item_types
- date/time

## Exam Items
- exam_item_id
- exam_id
- item_id
- points

## Responses
- response_id
- exam_id
- student_id
- item_id
- student_answer
- score (auto-graded MCQ/TF)

## Results
- result_id
- exam_id
- student_id
- total_score
- status (pass/fail)
