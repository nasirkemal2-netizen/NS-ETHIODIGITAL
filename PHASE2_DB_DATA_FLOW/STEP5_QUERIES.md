# STEP5_QUERIES.md
Sample SQL queries for testing and reporting in NS-ETHIODIGITAL

## 1. List all students in a school
SELECT id, name, email
FROM Users
WHERE role = 'Student' AND school_id = 1;

## 2. Exams created by a teacher
SELECT id, title, time_limit
FROM Exams
WHERE teacher_id = 2;

## 3. Items in an exam
SELECT ei.id AS exam_item_id, ib.question_text, ib.type
FROM Exam_Items ei
JOIN Item_Bank ib ON ei.item_id = ib.id
WHERE ei.exam_id = 3;

## 4. Student responses and scores
SELECT r.student_id, r.exam_id, r.answer, res.total_score, res.status
FROM Responses r
JOIN Results res ON r.student_id = res.student_id AND r.exam_id = res.exam_id
WHERE r.exam_id = 3;

## 5. Top scoring students
SELECT student_id, SUM(total_score) AS total
FROM Results
GROUP BY student_id
ORDER BY total DESC
LIMIT 10;
