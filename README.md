# 🤖 n8n ATS Resume Score Checker

> An AI-powered resume screening workflow that analyzes PDF resumes, generates an ATS score using Google Gemini, stores candidate results in Google Sheets, and sends automated email notifications.

![n8n](https://img.shields.io/badge/n8n-Automation-orange?style=for-the-badge&logo=n8n)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini-AI-blue?style=for-the-badge&logo=google)
![Gmail](https://img.shields.io/badge/Gmail-Email-red?style=for-the-badge&logo=gmail)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Database-green?style=for-the-badge&logo=googlesheets)
![License](https://img.shields.io/badge/License-Apache%202.0-blue?style=for-the-badge)

---

## 📌 Overview

The **n8n ATS Resume Score Checker** is an AI-powered resume screening automation built using **n8n** and **Google Gemini**.

It automates the initial resume screening process by accepting a candidate's resume, extracting the PDF content, analyzing it with AI, generating an ATS score and summary, storing candidate information in Google Sheets, and sending automated email notifications.

### 🎯 Main Flow

**Resume Upload → PDF Extraction → AI Analysis → ATS Score → Google Sheets → Email Notifications**

---

## ✨ Features

- 📄 Upload resumes in PDF format
- 👤 Collect candidate details
- 📧 Collect candidate email
- 🔗 Collect LinkedIn profile
- 📑 Extract text from uploaded resumes
- 🤖 AI-powered resume analysis using Google Gemini
- 📊 Generate ATS score out of 100
- 📝 Generate AI-based resume summary
- 📋 Store candidate information in Google Sheets
- 📩 Send HR/recruiter notification
- 📧 Send confirmation email to candidate
- ⚡ Automated workflow using n8n

---

## 🔄 Workflow Architecture

```text
                    ┌──────────────────────┐
                    │      Candidate       │
                    │   Application Form   │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │     Resume PDF       │
                    │       Upload         │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   PDF Text           │
                    │   Extraction         │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    Google Gemini     │
                    │     AI Analysis      │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   ATS Score +        │
                    │   AI Summary         │
                    └──────────┬───────────┘
                               │
                 ┌─────────────┴─────────────┐
                 │                           │
                 ▼                           ▼
        ┌──────────────────┐       ┌──────────────────┐
        │  Google Sheets   │       │  Email           │
        │  Candidate Data  │       │  Notifications   │
        └──────────────────┘       └──────────────────┘

🧠 How It Works
1️⃣ Candidate Submission

The candidate fills out the application form with:

Full Name
Email ID
LinkedIn Profile
Resume PDF
2️⃣ Resume Text Extraction

The uploaded PDF resume is processed and converted into text so that the content can be analyzed by the AI model.

3️⃣ AI Resume Analysis

The extracted resume text is sent to Google Gemini for analysis.

The AI generates:

Compatibility Rating
ATS Score
Resume Summary
Screening Recommendation
4️⃣ Store Candidate Data

Candidate details and the AI-generated resume analysis are automatically added to Google Sheets.

This creates a simple candidate tracking system for recruiters.

5️⃣ Email Automation

After processing, automated emails are sent.

📧 Candidate

The candidate receives a confirmation email informing them that their resume has been successfully received.

📩 HR / Recruiter

The recruitment side receives candidate information and the AI screening result.

🛠️ Tech Stack
Technology	Purpose
n8n	Workflow automation
Google Gemini	AI resume analysis
Gmail	Automated email notifications
Google Sheets	Candidate data storage
PDF Extraction	Resume text extraction
📂 Project Structure
n8n_ATS_Resume_Score_Checker/
│
├── README.md
│
└── n8n_ATS_Resume_Score_Checker.json
🚀 Getting Started
Prerequisites

You need:

n8n
Google Gemini API credentials
Gmail credentials
Google Sheets credentials
A Google Sheet for storing candidate results
📥 Import the Workflow
Step 1

Open your n8n instance.

Step 2

Go to:

Workflows → Import from File
Step 3

Select:

n8n_ATS_Resume_Score_Checker.json
Step 4

Configure your credentials:

Google Gemini
Gmail
Google Sheets
Step 5

Select/configure your Google Sheet.

Step 6

Activate the workflow.

📊 Example Output

The AI generates an ATS score and resume summary.

Example:

ATS Score: 82/100

Summary:
The resume is well structured and highlights relevant
experience, but could be improved with more targeted
keywords.

The result is then stored in Google Sheets and used in the automated email workflow.

🎯 Use Cases

This workflow can be used for:

👨‍💼 Recruitment teams
🏢 Small businesses
🎓 College placement cells
💼 Job application portals
🤖 HR automation
📄 Resume screening
🚀 AI automation projects
🔧 Future Improvements

The project can be extended with:

 Job Description input
 Resume vs Job Description matching
 Keyword gap analysis
 Skills extraction
 Experience matching
 Education matching
 Resume improvement suggestions
 Candidate ranking
 Multiple job roles
 Recruiter dashboard
 Web-based frontend
 Database integration
 PDF report generation
🧠 Advanced ATS Pipeline

A future version can use a more detailed scoring pipeline:

Resume
   │
   ▼
PDF Text Extraction
   │
   ▼
Skill Extraction
   │
   ▼
Job Description Matching
   │
   ▼
Keyword Analysis
   │
   ▼
Experience Matching
   │
   ▼
Education Matching
   │
   ▼
Formatting Analysis
   │
   ▼
Weighted ATS Score
   │
   ▼
AI Recommendations
   │
   ▼
Final Resume Report
⚠️ Limitations

The ATS score is generated using an AI model and should be considered an automated screening indicator, not a final hiring decision.

For production-level recruitment systems, deterministic scoring rules and additional validation can be added.

🔐 Security

Never upload API keys, passwords, OAuth tokens, or other secrets to GitHub.

Configure credentials directly inside n8n.

Before making the repository public, always review exported workflow files and remove sensitive information.

📸 Project Screenshots

You can add screenshots of the project here:

n8n Workflow
![n8n Workflow](screenshots/workflow.png)
Application Form
![Application Form](screenshots/form.png)
Google Sheets Output
![Google Sheets](screenshots/google-sheets.png)
ATS Result
![ATS Result](screenshots/ats-result.png)
📈 Project Flow
Candidate
    ↓
Application Form
    ↓
Resume PDF
    ↓
PDF Text Extraction
    ↓
Google Gemini
    ↓
ATS Score + AI Summary
    ↓
Google Sheets
    ↓
Email Automation
👨‍💻 Author
Harish Devarakonda

B.Tech Computer Science Engineering

Interested in:

Artificial Intelligence
AI Automation
n8n
Java
Frontend Development
AI-powered workflows
📄 License

This project is licensed under the Apache License 2.0.

⭐ If you find this project useful, consider giving the repository a star!
