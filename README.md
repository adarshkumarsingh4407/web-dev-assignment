# Lab 2 - Student CRUD API

A simple REST API built using **Node.js and Express.js** for performing CRUD operations on student data.

## 📌 Project Overview

This project demonstrates how to create an Express server and implement REST API routes for managing student records.

The API supports:

* **GET** - Retrieve students
* **POST** - Add a new student
* **PUT** - Update student information
* **DELETE** - Delete a student
* Error handling using `try/catch`
* Custom logger middleware
* API testing using Postman

## 🛠️ Technologies Used

* Node.js
* Express.js
* JavaScript
* Postman
* REST API

## 📁 Project Structure

```text
web-dev-assignment/
│
├── middleware/
│   └── logger.js
│
├── routes/
│   └── students.js
│
├── server.js
├── package.json
├── package-lock.json
├── Lab2-Postman-Collection.json
│
├── GET METHOD.png
├── POST METHOD.png
├── PUT METHOD.png
├── DELETE METHOD.png
└── VS code Terminal.png
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/adarshkumarsingh4407/web-dev-assignment.git
```

### 2. Open the project folder

```bash
cd web-dev-assignment
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the server

```bash
npm start
```

The server will run at:

```text
http://localhost:3000
```

## 🔗 API Endpoints

### GET - Get All Students

```http
GET /students
```

Returns the list of students.

**Expected Status:** `200 OK`

---

### POST - Add Student

```http
POST /students
```

Example JSON:

```json
{
  "name": "Aman",
  "age": 20,
  "course": "AI/ML"
}
```

**Expected Status:** `201 Created`

---

### PUT - Update Student

```http
PUT /students/1
```

Example JSON:

```json
{
  "name": "Adarsh Updated",
  "age": 21,
  "course": "AI/ML"
}
```

**Expected Status:** `200 OK`

---

### DELETE - Delete Student

```http
DELETE /students/1
```

Deletes the student with the specified ID.

If the student does not exist:

**Expected Status:** `404 Not Found`

```json
{
  "error": "Student not found"
}
```

## 🧪 Testing with Postman

The APIs can be tested using **Postman**.

A Postman collection is included in the repository:

```text
Lab2-Postman-Collection.json
```

The repository also contains screenshots of the GET, POST, PUT, and DELETE API testing.

## 📝 Logger Middleware

A custom logger middleware is used to display the following information for every request:

* HTTP method
* Request URL
* Timestamp

Example:

```text
GET /students - 2026-09-27T...
```

## 🎯 Learning Objectives

Through this lab, the following concepts are demonstrated:

1. Creating an Express server.
2. Creating REST API routes.
3. Performing CRUD operations.
4. Using HTTP status codes.
5. Handling errors with `try/catch`.
6. Creating custom middleware.
7. Testing APIs using Postman.

## 👨‍💻 Author

**Adarsh Kumar Singh**

B.Tech CSE (AI/ML)

## 📄 License

This project is created for educational and academic purposes.
