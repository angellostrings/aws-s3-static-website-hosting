# AWS S3 Static Website Hosting

> Cloud Computing Assessment 2 - Hosting a static website on Amazon S3

[![AWS S3](https://img.shields.io/badge/AWS-S3-FF9900?style=flat&logo=amazons3)](https://aws.amazon.com/s3/)
[![Region](https://img.shields.io/badge/Region-eu--north--1-blue)](https://aws.amazon.com/about-aws/global-infrastructure/)
[![Status](https://img.shields.io/badge/Status-Live-brightgreen)](http://michael-angelo-s3-1092.s3-website.eu-north-1.amazonaws.com)

## 🌐 Live Website
**URL:** http://michael-angelo-s3-1092.s3-website.eu-north-1.amazonaws.com

Click the link to view the live site.

## 📋 Project Details
- **Student:** Michael Angelo
- **Bucket Name:** `michael-angelo-s3-1092`
- **Region:** `eu-north-1` (Stockholm)
- **Date:** 29th October, 2026
- **Course:** Cloud Computing - Assessment 2

## 📖 Overview
This project demonstrates how to host a static website using Amazon S3. The website contains personal identification details to prove ownership and is configured for public access without 403 errors.

The assignment required:
1. Bucket name with personal identifier
2. Specific region (eu-north-1)
3. Static website hosting enabled
4. Public access via bucket policy

## 🚀 How I Did It

### Step 1: Create S3 Bucket
- Went to AWS S3 Console
- Region: eu-north-1 (Stockholm)
- Bucket name: michael-angelo-s3-1092
- Unchecked "Block all public access"

### Step 2: Enable Static Website Hosting
- Properties tab > Static website hosting > Enable
- Index document: `index.html`
- Copied the endpoint URL

### Step 3: Upload Website File
Created `index.html` with:
- Title: AWS S3 Static Website Hosting
- Name: Michael Angelo
- Gender: Male
- Date: 29th October, 2026

### Step 4: Make it Public
Added Bucket Policy to allow public read:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::michael-angelo-s3-1092/*"
    }
  ]
}
### Step 5: Verify
Opened endpoint - Website loaded successfully with no 403 Forbidden error.

## 📁 Files in this Repo
## 🛠️ Technologies Used
- AWS S3 - Storage and static hosting
- HTML5 - Website structure
- IAM Bucket Policy - Public access management
- GitHub - Documentation

## 📸 Screenshots
*Add your 2 screenshots here after uploading:*
- Live website with URL bar showing eu-north-1
- S3 Properties page showing Static hosting: Enabled

## 🎯 What I Learned
- How to create and configure S3 buckets in specific regions
- Difference between S3 endpoint and website endpoint
- How to write bucket policies for public access
- Troubleshooting 403 Forbidden errors
- Hosting costs and real-world use cases for S3

## 🔗 Links
- Live Site: http://michael-angelo-s3-1092.s3-website.eu-north-1.amazonaws.com
- AWS S3 Docs: https://docs.aws.amazon.com/s3/

---
Author: Angelo Michael | GitHub: @angellostrings
