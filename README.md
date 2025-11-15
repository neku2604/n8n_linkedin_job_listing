# n8n LinkedIn Job Automation

An automated n8n workflow that fetches LinkedIn (or other) job listings via RSS, processes them with OpenAI, and logs structured data to Google Sheets for tracking and analysis.

## ✨ Overview

This repository provides an n8n automation workflow that:

- Reads job listings from a configured RSS feed  
- Sends each listing to OpenAI for summarization, classification, or enrichment  
- Optionally refines the output through additional prompt steps  
- Writes the processed job information into a Google Sheet, enabling a structured job tracking system

Use this to build an automated job-curation pipeline without manual effort.

---

## ✅ Features

- **Automated Job Fetching**: Pull new job listings via RSS  
- **AI Processing**: Use OpenAI to analyze and summarize job descriptions  
- **Data Refinement**: Refine or reformat data with additional prompts  
- **Google Sheets Logging**: Save job metadata and enriched content in a spreadsheet  
- **Configurable Limits**: Use a limiter node to avoid processing too many entries at once  
- **Flexible Trigger Options**: Run manually, on a schedule, or via webhook  

---

## 🧱 Architecture / Workflow

Here is a high-level overview of the workflow:

1. **Trigger** — workflow starts (manual trigger or schedule)  
2. **RSS Read** — fetches job listings from RSS  
3. **Limiter** — caps the number of items to process per run  
4. **HTTP Request** — retrieves full job details from the listing URL  
5. **OpenAI (Message Model)** — processes raw job data  
6. **Additional Message Models** — optional steps for refining or structuring AI output  
7. **Google Sheets** — append or update a row for each job listing

---

## 🛠 Getting Started

### Prerequisites

- An **n8n** instance (self-hosted or cloud)  
- An **OpenAI API key**  
- A **Google account** with a Google Sheet to store job data  
- Google Sheets API credentials (OAuth) configured in your n8n instance  
