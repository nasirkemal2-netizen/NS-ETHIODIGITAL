# STEP6_SECURITY.md
Data access, roles, and permissions in NS-ETHIODIGITAL

## 1. Role-based Access Control
- Admin: full access to all Schools, Users, Exams, Item Bank, Responses, Results
- Teacher: manage own Exams, view Results for own Exams, select Items from Item Bank
- Student: take Exams, submit Responses, view own Results

## 2. Authentication
- All users must login with email & password
- Passwords stored securely with hashing (e.g., bcrypt)
- Session management or JWT tokens for web & mobile

## 3. Authorization
- API endpoints and actions protected based on roles
- Example: Only Admin can create Schools or assign Teachers

## 4. Data Security
- Sensitive data (passwords, answers) encrypted at rest or in database
- HTTPS / SSL for data in transit
- Regular backups of database

## 5. Optional Enhancements
- Two-factor authentication for Admins
- Audit logs for critical actions (exam creation, result updates)
