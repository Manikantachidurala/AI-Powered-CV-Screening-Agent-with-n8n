# AI-Powered-CV-Screening-Agent-with-n8n

🤖 AI-Powered CV Screening Agent


A low-code AI-powered automation built using n8n, Groq API, and Google Workspace tools to streamline and automate resume screening for HR teams and hiring managers.

This agent takes candidate info from a form, summarizes the profile using Groq LLM, evaluates fit for a specific job, and logs the result in a Google Doc and Sheet — all automatically.

📌 Key Features
📝 Form Submission via Google Forms

🧠 Real-time Summarization using Groq API

📋 Candidate Evaluation against a job description

🎯 Scoring System (1–10) based on skills & fit

📄 Summary Generation into Google Docs

📊 Rating and Logs saved in Google Sheets

🔐 OAuth 2.0 Security using Google Credentials

🔁 Fully automated with n8n Workflow

🛠️ Tech Stack
Tool	Purpose
n8n	Low-code workflow automation
Groq API	High-speed LLM for summarization
Google Forms	Input collection from candidates
Google Docs API	Output storage & document generation
Google Sheets	Summary and rating log
OAuth 2.0	Google account authentication
HTTP Request Node	Connect to external AI API
JSON	CV and JD data formatting
🚀 How It Works
graph TD
  A[Google Form Submission] --> B[n8n Trigger Node]
  B --> C[Collect & Structure Data]
  C --> D[Groq API: Summarize & Evaluate]
  D --> E[Parse AI Response]
  E --> F[Generate Google Doc + Sheet Entry]
🧠 Sample Prompt Logic (Used in n8n)
You are an HR expert. Based on the CV and job description below, summarize the candidate and rate their suitability for the role on a scale of 1 to 10. Keep it short and clear.

CV:
{{ $json["cv_text"] }}

Job Description:
{{ $json["job_description"] }}
🔐 Authentication Setup
Create a Google Cloud Project

Enable Google Docs API, Google Sheets API, and Drive API

Set up OAuth 2.0 consent screen

Add Client ID & Secret to n8n's Google OAuth node

✅ Use Cases
📌 Real-time CV screening in hiring pipelines

🔍 Shortlisting candidates based on job role match

📄 Auto-generating formatted HR summaries

📊 Creating structured records for candidate tracking




Recruiters & HR professionals managing bulk applications

Technical hiring automation for startups and agencies

