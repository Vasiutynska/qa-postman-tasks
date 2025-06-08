# Test Cases – Task 01

## TC-001: Create user with valid data
- Method: POST `/user/register`
- Body: valid email, name, password
- Expected: 201 Created + token

## TC-002: Create user with missing email
- Expected: 400 Bad Request, validation error

## TC-003: Update user profile
- Method: PUT `/user/profile`
- Update all fields
- Expected: 200 OK + updated data

## TC-004: Change password
- Method: PUT `/user/change-password`
- Body includes correct oldPassword and newPassword
- Expected: 200 OK

## TC-005: Logout and login
- POST `/auth/logout`, then `/auth/login`
- Use same credentials
- Expected: 200 OK + token

## TC-006: Add a car
- POST `/cars`
- Send brand, model, year, etc.
- Expected: 201 Created + carId

## TC-007: Add expenses to car
- POST `/expenses`
- Use carId from previous step
- Expected: 201 Created

## TC-008: Delete user
- DELETE `/user/me`
- Expected: 200 OK or 204 No Content
