# Task API - NestJS

Simple RESTful API built using NestJS to manage Task resources with full CRUD functionality and input validation.

---

## 📌 Project Overview

This project implements a Task management API using NestJS with a modular architecture (Module, Controller, Service).  
Validation is applied using DTOs and ValidationPipe to ensure data integrity.

Each Task has the following properties:

```ts
interface Task {
  id: number;
  title: string;
  description: string;
  isCompleted: boolean;
}
```

---

## 🚀 Features

- Create Task
- Retrieve All Tasks
- Retrieve Task by ID
- Update Task
- Delete Task
- DTO Validation
- Default value handling (`isCompleted` defaults to false)
- In-memory data storage

---

## 🧱 Tech Stack

- Node.js
- NestJS
- TypeScript
- class-validator
- class-transformer

---

## 📂 Project Structure

```
src/
 ├── tasks/
 │   ├── dto/
 │   │   ├── create-task.dto.ts
 │   │   └── update-task.dto.ts
 │   ├── task.interface.ts
 │   ├── tasks.controller.ts
 │   ├── tasks.service.ts
 │   └── tasks.module.ts
 ├── app.module.ts
 └── main.ts
```

---

## ⚙️ Installation & Running

### 1. Install dependencies
```
npm install
```

### 2. Run development server
```
npm run start:dev
```

Server will run on:
```
http://localhost:3000
```

---

## 📡 API Endpoints

### 🔹 Create Task
**POST** `/tasks`

Request Body:
```json
{
  "title": "Learn NestJS",
  "description": "Build CRUD API"
}
```

---

### 🔹 Get All Tasks
**GET** `/tasks`

---

### 🔹 Get Task by ID
**GET** `/tasks/:id`

---

### 🔹 Update Task
**PUT** `/tasks/:id`

Example:
```json
{
  "isCompleted": true
}
```

---

### 🔹 Delete Task
**DELETE** `/tasks/:id`

---

## ✅ Validation Rules

- `title` → required, must be string
- `description` → optional
- `isCompleted` → optional, defaults to `false`

Validation is handled using:
- CreateTaskDto
- UpdateTaskDto
- Global ValidationPipe

---

## 🧪 Testing

API testing can be done using:
- Thunder Client (VS Code)
- Postman
- cURL

---

## 👤 Author

Andre Muhamad Pajri

---

## 📄 License

MIT License
