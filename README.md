📌 DevOps Project 1 – Static Website CI/CD using AWS S3 & GitHub Actions
🔥 Project Overview

This project demonstrates how to host a static website on AWS S3 and automate deployment using GitHub Actions, following DevOps best practices and security principles.

Whenever code is pushed to GitHub, the website is automatically deployed to AWS S3 using CI/CD.

🎯 Project Goal

Host a static website on AWS S3

Automate deployment using GitHub Actions

Use IAM with least privilege

Follow real-world DevOps workflow

🧰 Tools & Technologies Used

AWS S3 – Static website hosting

IAM – Secure access & least privilege

AWS CLI – Programmatic AWS access

Git & GitHub – Version control

GitHub Actions – CI/CD automation

Linux (Ubuntu / WSL) – Development environment

🏗️ Architecture
Developer
   ↓
GitHub Repository
   ↓ (push to main)
GitHub Actions (CI/CD)
   ↓
AWS S3 Bucket
   ↓
Static Website accessible via browser

📁 Repository Structure
devops-project-01-static-website-cicd/
├── website/
│   ├── index.html
│   └── error.html
├── .github/
│   └── workflows/
│       └── deploy.yml
├── docs/
└── README.md


website/ → deployable files only

.github/workflows/ → CI/CD pipeline

docs/ → documentation

⚙️ CI/CD Workflow Explanation

GitHub Actions triggers on every push to main

AWS credentials are securely loaded from GitHub Secrets

Website files are synced to S3 using aws s3 sync

Old files are removed using --delete

🔐 Security Best Practices Followed

Root user not used

IAM user with least privilege

AWS credentials stored in GitHub Secrets

No secrets committed to repository

🧠 Key Learnings

Difference between 403 (permission) and 404 (file not found) in S3

How S3 static website hosting works

How to automate deployments using GitHub Actions

Importance of least privilege in IAM