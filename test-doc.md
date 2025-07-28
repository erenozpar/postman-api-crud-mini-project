# API Test Documentation

This document contains test scenarios and expected results for the **JSONPlaceholder CRUD API Testing Project** using Postman.

---

## API Base URL

https://jsonplaceholder.typicode.com

---

## Test Scenarios

### Test: Get All Posts

- **Request Type:** GET  
- **Endpoint:** `/posts`  
- **Precondition:** None  
- **Expected Result:**
  - Status Code: `200`
  - Response has 100 posts
  - Each post has keys: `userId`, `id`, `title`, `body`

---

### Test: Get Posts by ID

- **Request Type:** GET  
- **Endpoint:** `/posts/1`  
- **Precondition:** User with ID `1` exists  
- **Expected Result:**
  - Status Code: `200`
  - Response includes correct field like id, title, body
  - User id is 1

---

### Test: Create a New Post

- **Request Type:** POST  
- **Endpoint:** `/posts`  
- **Body:**
  ```json
 {
 "userId": 101,
        "id": 101,
        "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
        "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
 }
Expected Result:

- Status Code: 201
- Response time is less than 200ms
- Response body has correct userId

### Test: Update a Post
Request Type: PUT

Endpoint: /posts/3

Body:

json
Copy
Edit
{
 "userId": 101,
        "id": 101,
        "title": "Uptade Title",
        "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
 }
Expected Result:

- Status Code: 200

5️⃣ Test: Delete Post by userId
Request Type: DELETE

Endpoint: /posts/3

Expected Result:

- Status Code: 200
- Empty response body

## Test Tool
Tool Used: Postman

Environment Variables:

### baseUrl = https://jsonplaceholder.typicode.com

*!!!* Notes
JSONPlaceholder is a fake API; data is not actually created/updated/deleted.

The focus is on validating request/response structure, status codes, and schema fields.

