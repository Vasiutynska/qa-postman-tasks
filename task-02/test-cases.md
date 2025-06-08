# Test Cases – Task 02

## TC-001: User creation with JSON schema validation
- Validate response against schema
- Check message field = "User successfully created"

## TC-002: Profile update full check
- Validate response matches sent values
- Validate dateBirth dynamically (2006 instead of hardcoded 2005)

## TC-003: Change password
- Assert `userId` is the same before and after password change

## TC-004: Expenses increase
- Send first expense: 100
- Send second expense: 150
- Assert second > first

## TC-005: Validation errors with localization
- Send bad profile data (e.g., string instead of number)
- Expect message in different language ("Invalid data type")

## TC-006: Registration field validation
- Send empty email, short password
- Check `message` field returns proper error
