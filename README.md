# Altschool Africa - EC2 + ALB + S3 Deployment Project with Ansible

This repository contains the configuration and automation files used to deploy a simple website on AWS EC2 instances as part of the Altschool Africa 2nd Semester Final Exam.

## Project Summary

The goal was to deploy a basic HTML page that displays the EC2 instance’s IP address, automate the setup of NGINX using Ansible, and configure an Application Load Balancer (ALB) to distribute traffic. Additionally, the same site was deployed to an S3 bucket for comparison.

## Repository Contents

- **index.html** — Default static HTML page.
- **templates/** — Jinja2 template files for dynamically generating the index.html on each EC2 instance, displaying the instance’s hostname.
- **hosts** — Ansible inventory file listing the EC2 instances.
- **playbook.yaml** — Ansible playbook to install NGINX, deploy the website, and ensure the service starts on boot.

## How It Works

- The playbook uses the Jinja2 template to customize the HTML page per instance.
- NGINX is installed and configured via Ansible.
- The website is accessible through the ALB DNS name only (configured in AWS).

## Documentation

A detailed walkthrough of the entire deployment process and comparisons with S3 static hosting is available on my Medium article:

[From Code to Cloud: Deploying a Scalable Web Application with EC2, ALB, and S3](https://medium.com/@devOpswithJay/from-code-to-cloud-deploying-a-scalable-web-application-with-ec2-alb-and-s3-3e73f65831a5)

