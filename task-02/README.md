# Task 02 – Improved User Management API Testing

This task improves the previous Postman collection by adding more advanced validations and test checks.

## Improvements made:
- Added value checks to user registration validation
- Added JSON schema validation for user creation
- Added deep equality check for profile update
- Dynamic date of birth check (no hardcoded dates)
- Ensured `userId` remains the same after password change
- Validated expenses increase on each call
- Added localization-aware error tests
- New validation tests for profile (wrong data types)

## Collection:
- `Homework.postman_collection2.json`

## How to run:
1. Import the collection and environments into Postman
2. Use the `dev` or `prod` environment
3. Run each request manually or with Collection Runner

See details in:
- [`test-cases.md`](./test-cases.md)
- [`bug-reports.md`](./bug-reports.md)
