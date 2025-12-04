---
title: "Docker & GitHub Actions Automation"
date: 2025-12-03T12:00:00-05:00
draft: false
---

## Project Overview

This project focuses on modern DevOps practices, specifically **containerization** and **CI/CD automation**.

### Docker Containerization

I containerized the Laravel application using **Docker** and **Docker Compose**. This ensures that the application runs consistently across different environments.

-   **Nginx**: Serves as the web server.
-   **PHP-FPM**: Handles PHP processing.
-   **MySQL**: Provides the database service.

![Docker Setup](/images/docker-setup.png)

### GitHub Actions

I implemented **GitHub Actions** to automate the deployment process.

-   **Continuous Integration**: Automatically builds the project on every push.
-   **Continuous Deployment**: Deploys the documentation site to GitHub Pages.

![GitHub Actions Workflow](/images/github-actions.png)
