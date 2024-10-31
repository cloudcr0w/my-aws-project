<h1> My AWS Project 🌐 : :construction: under construction :construction:</h1> 

Project Description: My AWS Project is a simple, automated web service hosted on AWS. This project demonstrates cloud deployment using various AWS services, including automated CI/CD, a static frontend, and a backend with a database.

# Features ✨
Frontend: A simple HTML/CSS/JS interface, delivered globally via CloudFront from an S3 bucket.

Backend: A Node.js server hosted on EC2, connected to a MySQL database on Amazon RDS.

Automation: GitHub Actions CI/CD pipeline for automated deployment.

# AWS Services Used 📦

* EC2: Hosts the backend server.
* S3: Stores static frontend assets.
* Route 53: Manages the domain <a href=http://crow-project.click>crow-project.click</a>
* CloudFront: Distributes assets via a CDN.
* RDS: MySQL database for backend data.
* GitHub Actions: CI/CD pipeline to deploy changes automatically.

# Prerequisites 🛠️

1. AWS CLI: Install AWS CLI and configure it.
<pre> aws configure </pre>
2. Git: Install Git.
3. Node.js: Install Node.js.

# Installation & Setup 🚀
Clone the Repository

Open your terminal (use WSL if on Windows):
<pre>git clone git@github.com:cloudcr0w/my-aws-project.git
cd my-aws-project  </pre>
    

# Frontend Setup
Upload Files to S3:

<pre>aws s3 sync frontend s3://my-aws-project-assets --acl public-read</pre>
CloudFront Distribution: Set up a CloudFront distribution pointing to your S3 bucket.

# Backend Setup

Deploy EC2 Instance and connect:

<pre>aws ec2 run-instances --image-id ami-0abcdef1234567890 --instance-type t2.micro --key-name MyKeyPair</pre>

Database Setup (RDS):
<pre>aws rds create-db-instance --db-instance-identifier my-aws-project-db --db-instance-class db.t2.micro --engine mysql</pre>

# Route 53 Domain
Configure DNS records in Route 53 for crow-project.click.

# CI/CD Workflow 🔄
GitHub Actions deploys changes automatically:

# GitHub Actions Workflow (.github/workflows/deploy.yml):

This configures S3 sync and backend server updates.
Pushing Changes:
To deploy:
<pre> git add .
git commit -m "Update project"
git push origin main
</pre>

# How to Use 🌍

Access the Website: Visit crow-project.click.
Testing Backend: Verify backend connections and database access.
Contributions 🤝
Feel free to fork the repository and submit a pull request. Contributions and improvements are welcome!

