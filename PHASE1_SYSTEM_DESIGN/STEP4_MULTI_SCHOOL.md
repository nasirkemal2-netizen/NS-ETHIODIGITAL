# STEP4: Multi-Tenant Approach

## Goal
Ensure multiple schools can use the platform while keeping their data isolated and secure.

## Approach Options

### 1. Separate Database per School
- Pros: Total isolation, strong data security
- Cons: Harder maintenance, updates must be repeated per database

### 2. Single Database with school_id Field (Recommended)
- Pros: Easier maintenance, single backend, scalable
- Cons: Must always filter data by `school_id` in queries
- Implementation:
  - Every table containing school-related data includes a `school_id` field
  - Queries always filter by `school_id` to ensure isolation
  - Central item bank can be shared or restricted per school as needed

## Recommendation
- Use **single database with `school_id` field** for MVP
- Allows easier maintenance and future expansion while maintaining logical isolation
