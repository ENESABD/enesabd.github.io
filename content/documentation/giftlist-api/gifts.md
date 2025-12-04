---
title: "Gifts"
date: 2025-12-03T12:00:00-05:00
draft: false
weight: 3
---

# 🎁 Gifts Endpoints

## GET /gifts

**Description**: Get all gifts for the authenticated user

**Authentication**: ✅ Required

**Optional Query Parameters**:

- `recipientId` (integer) - Filter gifts by recipient

**Examples**:

- `GET /gifts` - All gifts
- `GET /gifts?recipientId=1` - Gifts for recipient 1

**Response** (200 OK):

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "recipient_id": 1,
      "name": "Garden Tools Set",
      "description": "Premium garden tools",
      "price": 89.99,
      "url": "https://example.com/product",
      "purchased": 0,
      "created_at": "2025-11-07 10:45:00"
    }
  ]
}
```

---

## GET /gifts/:id

**Description**: Get a specific gift by ID

**Authentication**: ✅ Required

**URL Parameters**: `id` (integer)

**Example**: `GET /gifts/1`

**Response** (200 OK): Returns single gift object

---

## GET /recipients/:recipientId/gifts

**Description**: Get all gifts for a specific recipient

**Authentication**: ✅ Required

**URL Parameters**: `recipientId` (integer)

**Example**: `GET /recipients/1/gifts`

**Response** (200 OK): Returns array of gift objects

---

## POST /gifts

**Description**: Create a new gift

**Authentication**: ✅ Required

**Request Body**:

```json
{
  "recipient_id": 1,
  "name": "Wireless Headphones",
  "description": "Noise cancelling",
  "price": 199.99,
  "url": "https://example.com/headphones",
  "purchased": 0
}
```

**Required Fields**: `recipient_id`, `name`
**Optional Fields**: `description`, `price`, `url`, `purchased` (0 or 1)

**Response** (201 Created):

```json
{
  "success": true,
  "data": {
    "id": 2,
    "recipient_id": 1,
    "name": "Wireless Headphones",
    "description": "Noise cancelling",
    "price": 199.99,
    "url": "https://example.com/headphones",
    "purchased": 0,
    "created_at": "2025-11-07 10:50:00"
  }
}
```

---

## PUT /gifts/:id

**Description**: Update an existing gift

**Authentication**: ✅ Required

**URL Parameters**: `id` (integer)

**Request Body** (all fields optional):

```json
{
  "name": "Wireless Headphones Pro",
  "description": "Noise cancelling with case",
  "price": 249.99,
  "purchased": 1
}
```

**Response** (200 OK): Returns updated gift object

---

## DELETE /gifts/:id

**Description**: Delete a gift

**Authentication**: ✅ Required

**URL Parameters**: `id` (integer)

**Example**: `DELETE /gifts/1`

**Response** (200 OK):

```json
{
  "success": true,
  "data": {
    "message": "Gift deleted"
  }
}
```
