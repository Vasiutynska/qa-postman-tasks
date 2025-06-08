# Test Cases – Task 03

## TC-001: Registration validation with parameterized values
- Use looped array of cases (e.g., empty name, invalid email)
- Expected `message` field matches for each

## TC-002: User creation – JSON schema validation
- Save schema from one response
- Validate structure matches for each new user

## TC-003: Profile update
- Validate `name`, `lastName`, `country`
- `dateBirth` format checked using dynamic logic

## TC-004: Change password
- Compare `userId` before and after

## TC-005: Logout and login
- Ensure login returns expected fields (`userId`, `photoFilename`, etc.)

## TC-006: Add car
- Validate brandId, modelId, and mileage in response

## TC-007: Add expenses
- Ensure mileage is greater than in previous request
- Save and compare previous mileage

## TC-008: Delete user
- Expect status 200 and no further access to user data

## TC-009: Run collection in qauto and qauto2
- Same collection runs correctly in both environments
