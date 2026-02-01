# STEP5: Role-Based Access (Admin / Teacher / Student)

## Roles Overview
- **Admin:** Full control over the system, manages schools, users, exams, and item bank
- **Teacher:** Creates exams, selects items from item bank, views results for their students
- **Student:** Takes exams assigned to them, views personal results

## Permissions Table

| Feature / Role       | Admin | Teacher | Student |
|---------------------|-------|---------|---------|
| Manage Schools       | ✅    | ❌      | ❌      |
| Manage Users         | ✅    | ❌      | ❌      |
| Create Exams         | ✅    | ✅      | ❌      |
| Select Items         | ✅    | ✅      | ❌      |
| Take Exams           | ❌    | ❌      | ✅      |
| View Results         | ✅    | ✅ (own students) | ✅ (self only) |
| Export Results       | ✅    | ✅ (own students) | ❌      |

## Notes
- Role-based filtering must be enforced at **backend queries** and **UI level**  
- Future roles (e.g., Proctor, Auditor) can be added as needed
