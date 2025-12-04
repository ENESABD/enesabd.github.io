---
title: "Authentication"
date: 2025-12-03T12:00:00-05:00
draft: false
weight: 1
---

# 🔐 Authentication Endpoints

## POST /auth/register

**Description**: Register a new user account

**Authentication**: ❌ Not Required

**Request Body**:

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

**Response** (201 Created):

```json
{
  "success": true,
  "data": {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com"
  }
}
```

**cURL Example**:

```bash
curl -X POST http://localhost:8000/auth/register \
  -H "Content-Type: application/json" \
  -d '{"name":"John Doe","email":"john@example.com","password":"password123"}'
```

---

## POST /auth/login

**Description**: Login and receive JWT token

**Authentication**: ❌ Not Required

**Request Body**:

```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

**Response** (200 OK):

```json
{
  "success": true,
  "data": {
    "token": "eyJ0eXAiOiJKV1QiLCJhbGc...",
    "user": {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com"
    }
  }
}
```

**PowerShell Example**:

```powershell
Invoke-RestMethod -Uri "http://localhost:8000/auth/login" `
  -Method POST -ContentType "application/json" `
  -Body (@{email="john@example.com";password="pass123"}|ConvertTo-Json)
```

---

## GET /auth/me

**Description**: Get current authenticated user information

**Authentication**: ✅ Required

**Headers**:

```
Authorization: Bearer YOUR_JWT_TOKEN
```

**Response** (200 OK):

```json
{
  "success": true,
  "data": {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "created_at": "2025-11-07 10:30:00"
  }
}
```
