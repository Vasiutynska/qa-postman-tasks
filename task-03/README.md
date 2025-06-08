# Task 03 – Collection optimization with parameterization and environment switch

## Goal

- Optimize validation tests to avoid duplication.
- Use one request to cover multiple validation cases by parameterizing the input.
- Run the same collection in two environments (`qauto` and `qauto2`) automatically.

---

## ✅ What was done

1. Created one test request `Validation2` using `Pre-request Script` to loop through an array of invalid registration cases (e.g., empty name, invalid email, short password, etc.).
2. Stored test data in an array and injected values using `pm.variables.set(...)`.
3. Removed multiple separate validation requests and replaced them with this loop.
4. Made sure the collection can be executed in both `qauto` and `qauto2` environments using `Runner`.
5. Avoided duplicate test logic in scripts.
6. Added test scripts for:
   - Registration schema validation
   - Profile editing (date format, country, etc.)
   - Password change validation
   - Logout and login
   - Adding a car and verifying response
   - Adding expenses with mileage check
   - User deletion

---

## 🧪 How to test it

1. Import the collection:  
   `Homework.postman_collection3.json`

2. Import both environments:  
   - `qauto.postman_environment.json`  
   - `qauto2.postman_environment.json`

3. Open **Runner** in Postman.

4. Choose the collection `Homework`.

5. Set **Iteration count** to at least the number of test cases (if using looping script, usually 11).

6. Set **Data** if needed (not required if using internal script array).

7. First run using environment `qauto`, then `qauto2` (or set up two runs manually).

8. Check results — errors and messages should match expectations.

---

## 📁 Folder content

| File                               | Description                            |
|------------------------------------|----------------------------------------|
| `Homework.postman_collection3.json` | Optimized Postman collection           |
| `qauto.postman_environment.json`    | First environment (qauto)              |
| `qauto2.postman_environment.json`   | Second environment (qauto2)            |
| `Homework.postman_test_run1.json`   | Test run result in first environment   |
| `Homework.postman_test_run2.json`   | Test run result in second environment  |
