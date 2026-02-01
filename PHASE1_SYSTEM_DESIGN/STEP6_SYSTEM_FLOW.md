# STEP6: Web + App Flow Description

## Overview
This section describes the flow of the system for both **web portal** (for Admins and Teachers) and **mobile app** (for Students and Teachers if needed).

## Web Portal (Admin / Teacher)
1. **Login / Authentication**
   - Admin or Teacher logs in with email/username + password
   - Role-based access determines dashboard view
2. **Dashboard**
   - Admin: manage schools, users, exams, item bank
   - Teacher: create exams, select items, view results
3. **Exam Management**
   - Create/Edit/Delete exams
   - Assign items from central item bank
   - Set time limits and exam schedules
4. **Results & Reports**
   - View results per exam
   - Export results in Excel / PDF
5. **Settings**
   - Update profile, change password
   - Configure school-specific settings (for Admin)

## Mobile App (Student)
1. **Login / Authentication**
   - Student logs in with school-provided credentials
2. **Dashboard**
   - View available exams
   - Show countdown / time-limited exams
3. **Exam Taking**
   - Select answers for MCQ / TF / Matching items
   - Submit exam
4. **Results Viewing**
   - View scores after auto-grading
   - Download / export if allowed

## Notes
- All requests are filtered by `school_id` for multi-tenant isolation
- Role-based permissions enforce access at UI and backend
- Future enhancements may include push notifications, proctoring, and AI-assisted grading
