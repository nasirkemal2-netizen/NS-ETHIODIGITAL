# STEP2_RELATIONS.md
Table relationships and foreign keys for NS-ETHIODIGITAL database

## 1. Schools → Users
- One School has many Users (Teachers & Students)
- Users.school_id → Schools.id (FK)

## 2. Users (Teacher) → Exams
- One Teacher can create many Exams
- Exams.teacher_id → Users.id (FK)

## 3. Exams → Exam Items
- One Exam can have many Exam Items
- Exam_Items.exam_id → Exams.id (FK)
- Exam_Items.item_id → Item_Bank.id (FK)

## 4. Users (Student) → Responses
- One Student can submit many Responses
- Responses.student_id → Users.id (FK)
- Responses.exam_id → Exams.id (FK)
- Responses.item_id → Exam_Items.id (FK)

## 5. Responses → Results
- Auto-graded Responses generate Results
- Results.exam_id → Exams.id (FK)
- Results.student_id → Users.id (FK)
