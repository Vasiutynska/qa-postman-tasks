# Test Cases – Task 01

## TC-001: Registration validation – empty or invalid values  
- Method: POST `/auth/signup`  
- Body: invalid combinations (e.g., empty name, invalid email, name with digits)  
- Expected: 400 Bad Request + specific error `message` in response  

## TC-002: Create user with valid data  
- Method: POST `/auth/signup`  
- Body: valid name, lastName, email, password, repeatPassword  
- Expected: 201 Created + token + user ID  

## TC-003: Update user profile  
- Method: PUT `/users/profile`  
- Body: name, lastName, photo, dateBirth, country  
- Expected: 200 OK + response matches all updated fields  
- `dateBirth` should be validated without hardcoding  

## TC-004: Change password  
- Method: PUT `/users/password`  
- Body: oldPassword from environment, new password  
- Expected: 200 OK + response contains same `userId` as before  

## TC-005: Logout and login  
- Method: GET `/auth/logout`, then POST `/auth/signin`  
- Body: email, password  
- Expected: 200 OK + token + fields like `userId`, `photoFilename`, `currency`  

## TC-006: Add a car  
- Method: POST `/cars`  
- Body: carBrandId, carModelId, mileage  
- Expected: 201 Created + response contains all sent values  

## TC-007: Add expenses to car  
- Method: POST `/expenses`  
- Body: carId, reportedAt, mileage, liters, totalCost  
- Expected: 201 Created + mileage is greater than previous (checked via variable)  

## TC-008: Delete user  
- Method: DELETE `/users`  
- Expected: 200 OK or 204 No Content  
