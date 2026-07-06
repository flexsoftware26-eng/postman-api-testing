# API Test Summary

## Test Scenarios

### PASS Tests

1. **Get Users - Pass Test**
   - Endpoint: `GET /users/1`
   - Expected: Status 200
   - Assertions:
     - Status code is 200 ✓
     - Response contains id field ✓
     - ID equals 1 ✓

2. **Create Post - Pass Test**
   - Endpoint: `POST /posts`
   - Expected: Status 201
   - Assertions:
     - Status code is 201 ✓
     - Response has required fields ✓
     - Title matches input ✓

3. **Update Post - Pass Test**
   - Endpoint: `PUT /posts/1`
   - Expected: Status 200
   - Assertions:
     - Status code is 200 ✓
     - Response type is JSON ✓

4. **Delete Post - Pass Test**
   - Endpoint: `DELETE /posts/1`
   - Expected: Status 200
   - Assertions:
     - Status code is 200 ✓

### FAIL Tests

1. **Get Invalid User - Fail Test**
   - Endpoint: `GET /users/999999`
   - Expected: Status 404 (but test expects 200)
   - Assertions:
     - Status code is NOT 404 ✗ (Intentional failure)

## Running Tests

```bash
npm test
```

This will execute all tests in the Postman collection and generate a report.
