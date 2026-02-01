# STEP3_DATA_FLOW.md
Data flow between modules for NS-ETHIODIGITAL

## Overview
This file describes how data moves through the system from Users → Exams → Item Bank → Responses → Results.

## Flow Steps

1. **User Registration / Login**
   - Students, Teachers, Admins register
   - Authentication validates credentials

2. **Exam Creation (Teacher)**
   - Teacher selects Items from Item Bank
   - Exam record is created with metadata (title, description, time limit)

3. **Student Exam Taking**
   - Students retrieve available Exams
   - Responses submitted to Responses table

4. **Automatic Grading**
   - MCQ, True/False, Matching types graded automatically
   - Results table updated (total_score, status)

5. **Reporting**
   - Admins / Teachers view results dashboards
   - Export results for analysis

6. **Feedback / Notifications**
   - Optional notifications sent to students for results
