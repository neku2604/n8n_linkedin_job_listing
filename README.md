
LinkedIn Job Listing Automation (n8n Workflow)

This project contains an n8n workflow that automates the process of collecting job details from LinkedIn job URLs and exporting the structured data into Excel/Sheets/Notion or any other target system.

🚀 What This Workflow Does

Accepts a list of LinkedIn job URLs

Fetches each job page using HTTP Request (with proxy/headers handling)

Extracts key job details such as:

Job Title

Company Name

Location

Posted Date

Job Description

Stores the extracted data in Excel or Google Sheets

Includes basic error handling for unavailable or blocked job pages

🛠️ Built With

n8n (No-code Automation Platform)

HTTP Request Node

Function / Set Nodes

Spreadsheet Node (Excel/Google Sheets)

📦 Files Included

linkedin-job-listing.json — Import this file directly into n8n using
Workflow → Import from File

🧩 How to Use

Clone the repo or download the JSON file

Open your n8n instance

Go to Workflow → Import

Select the JSON file

Add your list of LinkedIn URLs

Run the workflow

⚠️ Note

LinkedIn blocks direct scraping.
To avoid errors, use:

A scraping API (ScraperAPI, Zyte, BrightData), OR

Add browser-like headers in HTTP Request.
