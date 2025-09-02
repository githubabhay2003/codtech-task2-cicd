# CODTECH Internship - Task 2: CI/CD Pipeline Setup

This repository contains the work for **Task 2** of the CODTECH DevOps Internship program.  
The objective was to build a CI/CD pipeline to automate the deployment of a web application.

---

## Objective
To build a **Continuous Integration/Continuous Deployment (CI/CD)** pipeline using **GitHub Actions** to automatically deploy a simple static web application to **GitHub Pages**.

---

## Tools Used
- **Git & GitHub**: For version control and hosting the repository.  
- **GitHub Actions**: To define and execute the CI/CD workflow.  
- **GitHub Pages**: To host the deployed static website.  

---

## CI/CD Pipeline Workflow
The automation is defined in the `.github/workflows/deploy.yml` file.  
Here’s a breakdown of how it works:

1. **Trigger**  
   The workflow is automatically triggered on every push to the `main` branch.

2. **Permissions**  
   The workflow is granted the necessary permissions to read the repository contents and write to the GitHub Pages deployment.

3. **Job: `deploy`**  
   A single job named **deploy** runs on an `ubuntu-latest` virtual machine.  
   It consists of the following steps:
   - **Checkout**: Uses `actions/checkout@v4` to check out the repository code.  
   - **Setup Pages**: Uses `actions/configure-pages@v4` to configure the environment for a GitHub Pages deployment.  
   - **Upload Artifact**: Uses `actions/upload-pages-artifact@v3` to take the repository contents (e.g., `index.html`) and upload them as a build artifact.  
   - **Deploy to GitHub Pages**: Uses `actions/deploy-pages@v4` to deploy the uploaded artifact to GitHub Pages, making the website live.  

---

## Demonstration
The pipeline automatically deploys the `index.html` file in this repository.  

**Live Site URL**: [https://githubabhay2003.github.io/codtech-task2-cicd/](https://githubabhay2003.github.io/codtech-task2-cicd/)

---

This project successfully demonstrates a working pipeline configuration and provides a live demonstration of automated deployment, fulfilling the task's deliverables.
