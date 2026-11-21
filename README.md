# AI-Based Automated Data Entry from Emails

An AI-powered automation system that extracts important information from emails and automatically stores it in Google Sheets using n8n and OpenAI.

## Project Overview

Manual data entry from emails can be time-consuming and repetitive. This project automates the process by using an AI agent to read incoming emails, extract relevant information, structure the data, and save it directly into Google Sheets.

## Features

- **Automatic Email Monitoring:** Checks Gmail for incoming emails every minute.
- **AI-Powered Extraction:** Uses OpenAI GPT-4.1-mini to extract information from email content.
- **Structured Output:** Organizes extracted information into predefined JSON fields.
- **Google Sheets Integration:** Automatically appends extracted information to a spreadsheet.
- **Feedback Analysis:** Identifies feedback sentiment as positive, neutral, or negative.

## Information Extracted

The workflow is designed to extract:

- Name
- Email
- Address
- Gender (when explicitly provided)
- Feedback

Missing information is represented as null.

## Workflow Architecture

```text
Gmail Trigger
     |
     v
Get a Message
     |
     v
AI Agent (OpenAI GPT-4.1-mini)
     |
     v
Structured Output Parser
     |
     v
Google Sheets (Append Row)
```

## Technologies Used

- **n8n:** Workflow automation
- **OpenAI GPT-4.1-mini:** AI-based information extraction
- **Gmail:** Email monitoring and retrieval
- **Google Sheets:** Data storage
- **JSON:** Structured data exchange

## Repository Structure

```text
Automated_DataEntry_from_Email/
│
├── Demo/
│   └── Automated_DataEntry.mp4
│
├── Doc/
│   └── projectdoc.docx
│
├── Workflow/
│   └── data-entry-form-public.json
│
├── README.md
└── .gitignore
```

## Setup Instructions

1. Create or log in to an n8n instance.
2. Import `Workflow/data-entry-form-public.json`.
3. Connect your Gmail account using OAuth2 credentials.
4. Configure your OpenAI API credentials.
5. Connect your Google Sheets account.
6. Select your Google Spreadsheet and configure the required columns.
7. Test the workflow with sample emails.
8. Activate the workflow after successful testing.

**Note:** The public workflow JSON does not contain the original account credentials or spreadsheet ID. You must configure your own connections before running it.

## Project Documentation

The semester project report is available in the `Doc/` folder.

## Project Demonstration

A video demonstration is available in the `Demo/` folder.

## Future Improvements

- Extract information from email attachments.
- Add advanced data validation.
- Support multiple email accounts.
- Improve error handling and logging.
- Integrate with CRM systems.

## Security

- API keys and passwords must never be committed to GitHub.
- OAuth credentials should be configured securely inside n8n.
- Private email and customer information should not be included in public test data.

## Contributors

- 23SW041
- 23SW044

---

**Academic Project:** Automated Data Entry from Emails  
**Category:** AI-Based Workflow Automation