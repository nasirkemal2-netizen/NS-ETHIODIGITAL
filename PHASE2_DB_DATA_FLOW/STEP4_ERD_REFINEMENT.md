# STEP4_ERD_REFINEMENT.md
Refined ERD (Entity-Relationship Diagram) details for NS-ETHIODIGITAL

## Overview
This file contains notes and refinements for the database ERD, building upon the initial ERD.png created in Phase 1.

## Refinements
1. **Primary & Foreign Keys**
   - Ensure all FK relationships are clearly defined
   - Add cascade rules where necessary (e.g., deleting a School deletes associated Users)

2. **Indexes**
   - Add indexes on frequently queried fields (e.g., exam_id in Responses)

3. **Constraints**
   - Ensure enum types are used for roles, question types, and result status
   - Enforce NOT NULL where appropriate

4. **Optional Enhancements**
   - Add timestamp fields for auditing
   - Consider soft-delete flags for Users / Exams
