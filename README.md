# AI-Powered Lead Qualification & Automated Follow-Up System

An AI-driven lead management automation built using n8n, OpenAI, Gmail, and Google Sheets.

The workflow automatically captures incoming leads, analyzes their intent using an LLM, assigns a lead score, classifies the lead, sends personalized emails, checks for customer replies, and manages automated follow-ups.

## Workflow Architecture

Form Submission  
↓  
Google Sheets Lead Storage  
↓  
AI Lead Analysis  
↓  
JavaScript JSON Parsing  
↓  
Lead Classification  
↓  
HIGH / MEDIUM / LOW Routing  
↓  
Automated Email  
↓  
Wait Period  
↓  
Gmail Reply Detection  
↓  
Conditional Reply Check  
↓  
Lead Status Update

## Features

- Automated lead capture through an n8n form
- AI-powered lead scoring
- Lead classification into HIGH, MEDIUM, and LOW categories
- LLM-based intent analysis
- Dynamic lead routing
- Personalized email automation
- Automated waiting period for follow-up
- Gmail reply detection
- Conditional follow-up logic
- Google Sheets lead status tracking
- Prevention of unnecessary follow-up emails

## Tech Stack

- n8n
- OpenAI API
- JavaScript
- Gmail API
- Google Sheets

## Workflow

![Full Workflow](screenshots/01-full-workflow.png)

## AI Lead Analysis

The LLM analyzes the submitted lead and returns structured information including:

- Lead Score
- Category
- Intent
- Recommended Action

![AI Lead Analysis](screenshots/03-ai-lead-analysis.png)

## Dynamic Lead Routing

Leads are classified as:

- HIGH: 70-100
- MEDIUM: 40-69
- LOW: 0-39

The n8n Switch node dynamically routes leads based on the AI-generated category.

![Lead Routing](screenshots/04-lead-routing.png)

## Automated Email Follow-Up

Qualified leads automatically receive a personalized email based on their form submission.

![Automated Email](screenshots/05-automated-email.png)

## Reply Detection

The workflow waits for a defined period and checks Gmail for a response from the lead.

If a reply is detected, the lead is marked as `REPLIED`.

If no reply is detected, an automated follow-up email is sent.

![Reply Detection](screenshots/06-reply-detection.png)

## Lead Status Tracking

Google Sheets is used to maintain lead records and automatically update the lead status.

![Lead Status](screenshots/07-lead-status-sheet.png)

## Project Outcome

This project demonstrates how AI and workflow automation can be combined to automate lead qualification, customer communication, reply detection, and follow-up management.

## Author

Aanya Jain
