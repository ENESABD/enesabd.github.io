---
title: "Docker & GitHub Actions Automation"
date: 2025-12-03T12:00:00-05:00
draft: false
---

## Project Overview

This project focuses on modern DevOps practices, specifically **containerization** and **CI/CD automation**.

### Docker Containerization

I containerized the Laravel application using **Docker** and **Docker Compose**. I also created a `setup.sh` script to automate the build and startup process.

#### Step 1: Building Images

The script first builds the custom Docker images for PHP, Nginx, and MySQL.

![Docker Build Process](/images/docker-setup-1.png)

#### Step 2: Starting Containers

Once built, the containers are started in detached mode. The script then waits for the database to be ready.

![Docker Containers Starting](/images/docker-setup-2.png)

#### Step 3: Application Setup

Finally, the script installs dependencies, generates keys, and runs migrations inside the container.

![Docker Application Setup](/images/docker-setup-3.png)

### GitHub Actions

I implemented **GitHub Actions** to automate the deployment process. The workflow triggers on every push to the `main` branch, building the Hugo site and deploying it to GitHub Pages.

![GitHub Actions Success](/images/github-actions-success.png)
