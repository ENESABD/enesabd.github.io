---
title: "Recipients"
date: 2025-12-03T12:00:00-05:00
draft: false
weight: 2
---

# 🎯 Recipients Endpoints

## GET /recipients

**Description**: Get all recipients for the authenticated user

**Authentication**: ✅ Required

**Response** (200 OK):

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "user_id": 1,
      "name": "Mom",
      "relationship": "Mother",
      "notes": "Birthday in June",
      "created_at": "2025-11-07 10:35:00"
    }
  ]
}
```

---

## GET /recipients/:id

**Description**: Get a specific recipient by ID

**Authentication**: ✅ Required

**URL Parameters**:

- `id` (integer) - Recipient ID

**Example**: `GET /recipients/1`

**Response** (200 OK):

```json
{
  "success": true,
  "data": {
    "id": 1,
    "user_id": 1,
    "name": "Mom",
    "relationship": "Mother",
    "notes": "Birthday in June",
    "created_at": "2025-11-07 10:35:00"
  }
}
```

---

## POST /recipients

**Description**: Create a new recipient

**Authentication**: ✅ Required

**Request Body**:

```json
{
  "name": "Dad",
  "relationship": "Father",
  "notes": "Loves technology"
}
```

**Required Fields**: `name`
**Optional Fields**: `relationship`, `notes`

**Response** (201 Created):

```json
{
  "success": true,
  "data": {
    "id": 2,
    "user_id": 1,
    "name": "Dad",
    "relationship": "Father",
    "notes": "Loves technology",
    "created_at": "2025-11-07 10:40:00"
  }
}
```

**PowerShell Example**:

```powershell
Invoke-RestMethod -Uri "http://localhost:8000/recipients" `
  -Method POST -Headers @{Authorization="Bearer $token"} `
  -ContentType "application/json" `
  -Body (@{name="Dad";relationship="Father"}|ConvertTo-Json)
```

---

## PUT /recipients/:id

**Description**: Update an existing recipient

**Authentication**: ✅ Required

**URL Parameters**: `id` (integer)

**Request Body** (all fields optional):

```json
{
  "name": "Mom",
  "relationship": "Mother",
  "notes": "Birthday in June - loves gardening"
}
```

**Response** (200 OK): Returns updated recipient object

---

## DELETE /recipients/:id

**Description**: Delete a recipient and all associated gifts

**Authentication**: ✅ Required

**URL Parameters**: `id` (integer)

**Example**: `DELETE /recipients/1`

**Response** (200 OK):

```json
{
  "success": true,
  "data": {
    "message": "Recipient deleted"
  }
}
```
