# AI-Powered-CV-Screening-Agent-with-n8n

 AI-Powered CV Screening Agent
A low-code automation project that uses n8n, Groq API, and Google Docs to automate CV screening for HR teams and hiring managers.

This AI agent automatically summarizes resumes, compares them against a job description, rates candidates, and stores the output in a Google Doc — all in a seamless, secure workflow.

📌 Features
🔄 Resume submitted via Google Form or API

📑 Summary generated using Groq's LLM

🎯 Compared against job description (JD)

📊 Scored on a scale of 1–10

📁 Summary + rating sent to Google Docs

🔐 Secured with Google OAuth 2.0

⚙️ Workflow created using n8n (open-source automation)

🛠️ Tech Stack
n8n – Workflow automation

Groq API – High-speed LLM for summarization

Google Docs API – Store and manage outputs

Google OAuth – Authentication and access control

HTTP Request Node – To interact with external APIs

OpenAI/Groq Prompting – For rating and summarization logic

JSON – For structured CV input and job descriptions

🚀 How It Works
graph TD
  A[Form Submission or API Upload] --> B[n8n Trigger Node]
  B --> C[Extract CV Data]
  C --> D[Groq API: Summarize CV]
  D --> E[Compare with Job Description]
  E --> F[Rate Candidate (1–10)]
  F --> G[Send Summary + Score to Google Docs]
🧠 Prompt Logic (Example)
You are an HR expert. Rate the candidate based on the provided CV and job description on a scale of 1 to 10.
Explain your reasoning in 2–3 sentences.

CV:
{{ $json["cv_text"] }}

Job Description:
{{ $json["job_description"] }}
🔐 Authentication
Set up Google Cloud Project

Enable Google Docs API

Configure OAuth 2.0 credentials

Add your credentials to n8n using the Google OAuth node

✅ Use Cases
Automated resume screening for hiring pipelines


Recruiters & HR professionals managing bulk applications

Technical hiring automation for startups and agencies

