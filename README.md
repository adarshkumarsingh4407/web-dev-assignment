# Lab 2 - Student CRUD API

## Requirements covered
1. Create Express routes for `/students`.
2. Implement GET, POST, PUT and DELETE.
3. Return correct HTTP status codes.
4. Use try/catch and JSON error responses.
5. Add custom logger middleware using `app.use()`.
6. Test the APIs using Postman.

## Run the project

Open a terminal inside this folder:

```bash
npm install
npm start
```

Server:
`http://localhost:3000`

## Postman tests

### 1. GET
Method: GET
URL: `http://localhost:3000/students`
Expected: `200` and a JSON array.

### 2. POST
Method: POST
URL: `http://localhost:3000/students`

Body -> raw -> JSON:
```json
{
  "name": "Aman",
  "age": 20,
  "course": "AI/ML"
}
```

Expected: `201` and the created student.

### 3. PUT
Method: PUT
URL: `http://localhost:3000/students/1`

Body -> raw -> JSON:
```json
{
  "name": "Adarsh Updated",
  "age": 21,
  "course": "AI/ML"
}
```

Expected: `200` and the updated student.

### 4. DELETE unknown ID
Method: DELETE
URL: `http://localhost:3000/students/99`

Expected: `404` and:
```json
{
  "error": "Student not found"
}
```

## Logger
Every request prints method, URL and timestamp in the terminal.
