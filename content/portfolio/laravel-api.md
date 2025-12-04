---
title: "Laravel REST API Implementation"
date: 2025-12-03T12:00:00-05:00
draft: false
featured_image: "/images/laravel-shell-script.png"
description: "A complete re-implementation of the GiftList API using Laravel, featuring MVC architecture, Eloquent ORM, and Sanctum authentication."
---

## Project Overview

This project involves the re-implementation of the Gift List API using the **Laravel framework**. The goal was to transition from a raw PHP implementation to a structured MVC architecture provided by Laravel.

### Automated Deployment

I created a shell script `run.sh` to automate the deployment process. This script handles:

1.  Database setup (creating the database if it doesn't exist).
2.  Installing Composer dependencies.
3.  Configuring the environment (`.env`).
4.  Running database migrations and seeders.
5.  Starting the Laravel development server.

![Deployment Script Execution](/images/laravel-shell-script.png)

### Server & API Testing

Once deployed, the server runs on port 8000. The application logs incoming requests, confirming that the API endpoints are accessible and functioning correctly.

![Server Logs](/images/laravel-server-logs.png)

### Key Features

- **MVC Architecture**: Utilized Laravel's Model-View-Controller structure.
- **Eloquent ORM**: Implemented database interactions using Eloquent models.
- **Authentication**: Secured the API using **Laravel Sanctum**.
