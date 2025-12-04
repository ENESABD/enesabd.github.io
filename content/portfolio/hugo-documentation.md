---
title: "Documentation with Hugo"
date: 2025-12-03T12:00:00-05:00
draft: false
featured_image: "/images/hugo-docs-overview.png"
description: "Transforming Marp documentation into a professional static site using Hugo, hosted on GitHub Pages."
---

## Project Overview

This website itself is a project demonstrating the use of **Hugo**, a fast static site generator, to create a professional portfolio and documentation site.

### Site Structure

The site is organized into two main sections: **Documentation** and **Portfolio**.

#### Documentation Section

The API documentation was migrated from Marp to Hugo, featuring a clean and navigable layout.

![Documentation Overview](/images/hugo-docs-overview.png)

Each module, such as Authentication, has its own dedicated page with detailed endpoint descriptions.

![Documentation Module](/images/hugo-docs-module.png)

### Deployment to GitHub Pages

The site is hosted on **GitHub Pages**. The deployment is handled automatically by GitHub Actions.

#### Settings

In the repository settings, GitHub Pages is configured to serve the content from the `gh-pages` branch (or via the Actions workflow).

![GitHub Pages Settings](/images/github-pages-settings.png)

#### Live Site

The final result is a publicly accessible website available at the configured domain.

![Live Site](/images/github-pages-live.png)
