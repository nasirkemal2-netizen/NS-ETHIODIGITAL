# STEP2: Relationships Between Entities

## 1. School → Users
- One school has many teachers and students
- Users table contains `school_id` to link users to their school

## 2. Teacher → Exams
- One teacher can create many exams
- Each exam has `teacher_id` linking it to the creator

## 3. Exam → Exam Items
- One exam can contain many questions
- Exam Items table links `exam_id` with `item_id`

## 4. Student → Responses
- One student can submit many responses for different exams
- Responses table links `student_id` to `exam_id` and `item_id`

## 5. Responses → Results
- Auto-graded responses (MCQ/TF) generate total scores
- Results table contains `exam_id`, `student_id`, `total_score`, and status (pass/fail)

## 6. Item Bank → Exam Items
- Central item bank is used by multiple exams
- Exam Items table references `item_id` from Item Bank

## Textual ERD (Simple View)
School ───< Users
Users (Teacher) ───< Exams ───< Exam Items >─── Item Bank
Users (Student) ───< Responses >── Results
