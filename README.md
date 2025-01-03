"# Static_Website-Deployment_with_Jenkins" 

# CI/CD Pipeline for Static Website Deployment

This project demonstrates a simple CI/CD pipeline using Jenkins to automate the deployment of a static website (HTML, CSS, JavaScript) to an AWS S3 bucket. The pipeline integrates with GitHub for source code management

---

## Features
- **Automated Deployment**: Sync static website files to an S3 bucket.
- **GitHub Integration**: Automatically clone the repository during the build process.
  
---

## Prerequisites
1. **AWS Account** with an S3 bucket set up for static website hosting.
2. **Jenkins** installed and configured.
3. **AWS CLI** installed and configured on the Jenkins server.
4. **GitHub Repository** containing the static website code.

---

## Pipeline Steps
### 1. Host the Static Website on GitHub
- Upload your website files to a GitHub repository.

### 2. Configure Jenkins
- Create a Jenkins job and link it to the GitHub repository.
- Configure the job to:
  - Clone the repository.
  - Deploy the website files to the S3 bucket using `aws s3 sync`.

### 3. Automate Deployment to S3
- Use the following command to sync files:
  ```bash
  aws s3 sync . s3://YOUR_BUCKET_NAME --delete

