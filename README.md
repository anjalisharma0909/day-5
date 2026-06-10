# 📝 Notes API (Express.js)

A simple RESTful API built using Express.js to create, read, update, and delete notes. This project is great for beginners learning backend development with Node.js and Express.

---

## 🚀 Features

* Create a note
* Get all notes
* Update a note by index
* Delete a note by index
* Uses in-memory storage (array)

---

## 📁 Project Structure

```
.
├── src/
│   └── app.js        # Express app with routes
├── server.js         # Entry point
├── package.json
└── README.md
```

---

## 📦 Installation

1. Clone the repository:

```bash
git clone <your-repo-url>
cd day-5
```

2. Install dependencies:

```bash
npm install
```

---

## ▶️ Running the Server

### Development mode (with nodemon):

```bash
npm run dev
```

### Normal mode:

```bash
node server.js
```

Server will run on:

```
http://localhost:3000
```

---

## 📌 API Endpoints

### ➕ Create a Note

**POST /notes**

```json
{
  "title": "My Note",
  "content": "This is a note"
}
```

Response:

```json
{
  "message": "Note created successfully"
}
```

---

### 📖 Get All Notes

**GET /notes**

Response:

```json
{
  "notes": [ ... ]
}
```

---

### ✏️ Update a Note

**PATCH /notes/:index**

Example:

```
PATCH /notes/0
```

```json
{
  "title": "Updated Note",
  "content": "Updated content"
}
```

Response:

```json
{
  "message": "Note updated successfully"
}
```

---

### ❌ Delete a Note

**DELETE /notes/:index**

Example:

```
DELETE /notes/0
```

Response:

```json
{
  "message": "Note deleted successfully"
}
```

---

## ⚠️ Notes

* Data is stored in memory (array), so it will reset when the server restarts.
* No validation or error handling is implemented (can be improved).
* Using `delete` leaves empty slots in the array — consider using `splice()` instead.

---

## 🛠️ Dependencies

* express

---

  
