# CoMail AI – **Automated Resume Tailoring & Cold Email Job Outreach Agent**

This Capstone Project is part of the 5-Day AI Agents Intensive Course with Kaggle X Google Dec 2025. And here we are developing an agent which falls in the category of **concierge agent**

## **Overview**

CoMail AI is an intelligent automation agent designed to streamline the job application process from start to finish. Using the user’s resume and structured job data, the agent generates tailored resumes, personalized cover letters, recruiter outreach emails, and—upon approval—automatically sends out polished job application emails. CoMail AI makes the job search faster, more efficient, and consistently high-quality.

---

## **Problem Statement**

Tailoring a resume, writing a custom cover letter, and drafting a recruiter outreach email for each job is repetitive, time-consuming, and mentally draining. Job seekers applying to many positions struggle with consistency and personalization. Traditional tools offer piecemeal help, but none automate the entire workflow end-to-end.

---

## **Solution**

CoMail AI automates the full cold-email job application workflow. Given the user’s resume and a structured database containing job title, hiring manager name, hiring manager email, and job description, the agent performs the following:

1. **Extracts keywords and role expectations** from the job description.
2. **Tailors the resume** to highlight relevant skills and achievements.
3. **Generates a professional, customized cover letter** for each job.
4. **Creates a personalized cold outreach email** addressed to the recruiter or hiring manager.
5. **Packages attachments** (tailored resume + cover letter).
6. **Sends the email automatically**, or optionally requests user approval before sending.

---

## Sequential Workflows - The Assembly Line

Multi-Agent: Sequential 
Architecture: Comail AI agent pipeline 

User input : Get the job description from google sheet and update the cover letter, draft email and send to reciter/hiring manager
Info extractor Agent —> Draft Email Agent ——> Send Email Agent —> Editor Agent —> Output


info_file: We provide a file that has list of email ids, name of recruiter/hiring manager, company name. 

1. Info extractor Agent : extract required information from info_file 

2. Cover letter generation Agent: Role specific Cover letter generation
3. Draft Email Agent: Recruiter outreach email creation
4. Send Email Agent: Send email to recruiter with attachment (Email + Cover letter + Resume)
5. Editor Agent: Edits the draft copy of email.

## **Key Features**

### **1. Automated Resume Tailoring**

* Keyword extraction from job descriptions
* ATS-optimized rewording of bullets and skills
* Emphasis on relevant experience and project highlights

### **2. Role-Specific Cover Letter Generation**

* Personalized, job-driven cover letters
* Strong alignment with job description responsibilities
* Consistent professional tone

### **3. Recruiter Outreach Email Creation**

* Smart personalization using recruiter name, job title, and company
* Concise, impactful messaging
* Professional call-to-action

### **4. Email Sending Module**

* **Option A:** Automatic sending directly to the recruiter
* **Option B:** “Approval Mode” → user reviews the email before sending
* Supports SMTP, Gmail API, or Outlook API

### **5. Scalable Workflow**

* Batch processing for multiple job listings
* Consistent formatting and attachment structure
* Perfect for weekly job application cycles

---

## **Proposed Technical Stack**

* **Language:** Python
* **LLM:** OpenAI API or similar
* **Database:** SQLite or PostgreSQL
* **Document Processing:** python-docx for resume & cover letter generation
* **Email Sending:** SMTP, Gmail/Outlook API
* **Optional Orchestration:** Prefect for workflow automation
* **Logging and Tracking:** For job status, sent emails, and drafts

---

## **Impact**

CoMail AI provides job seekers with:

* Significant reduction in repetitive writing
* Higher-quality, role-aligned applications
* Increased efficiency and confidence
* Better recruiter response rates
* The ability to apply for more jobs with less effort

---

