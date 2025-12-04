---
title: "Laravel REST API Implementation"
date: 2025-12-03T12:00:00-05:00
draft: false
---

## Project Overview

This project involves the re-implementation of the Gift List API using the **Laravel framework**. The goal was to transition from a raw PHP implementation to a structured MVC architecture provided by Laravel.

### Key Features

-   **MVC Architecture**: Utilized Laravel's Model-View-Controller structure for better code organization.
-   **Eloquent ORM**: Implemented database interactions using Eloquent models (User, Gift, Recipient) instead of raw SQL.
-   **Authentication**: Secured the API using **Laravel Sanctum** for token-based authentication.
-   **API Endpoints**: Re-created all endpoints from Project 1, including CRUD operations for Gifts and Recipients.

### Architecture

![Laravel MVC Architecture](/images/laravel-mvc.webp)

The application follows the standard Laravel directory structure, separating routes, controllers, and models to ensure maintainability and scalability.
