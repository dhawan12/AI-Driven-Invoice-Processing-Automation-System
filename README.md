📄 AI-Driven Invoice Processing & Automation System (n8n)

An end-to-end automated invoice processing solution built using n8n, AI (LLMs), JavaScript, Microsoft SQL Server, and PowerShell.
This system processes scanned PDF invoices, extracts key financial data, validates it against a database, and automatically organizes files with robust error handling.

🚀 Features

📥 Automated ingestion of scanned PDF invoices from multiple directories

🤖 AI-powered extraction of invoice data from unstructured documents

🧠 Intelligent parsing and normalization of dates, amounts, and vendor details

🗄️ Vendor validation and duplicate invoice detection using SQL Server

📁 Automated file renaming, movement, and archival via PowerShell

⚠️ Error handling for incomplete, duplicate, or invalid invoices

🔁 Reusable sub-workflows for scalable processing

⏱️ Scheduled execution for continuous automation

🧠 Extracted Invoice Fields

The system automatically extracts and processes:

Invoice Number

Invoice Date

Vendor Name

Vendor Email

Final Amount (EUR, normalized)

🏗️ Architecture Overview

PDF Detection

Monitors configured folders for new scanned PDF invoices.

Text Extraction & AI Analysis

Extracts text from PDFs.

Uses AI (LLM) to identify and return structured invoice data in JSON format.

Data Cleaning & Transformation

JavaScript logic cleans AI output.

Normalizes date formats and currency values.

Database Validation (SQL Server)

Checks if vendor exists.

Inserts new vendors if needed.

Detects duplicate invoices using unique identifiers.

File System Automation

Renames invoices based on vendor, invoice number, and date.

Moves files to:

✅ Processed

❌ Unprocessed

🔁 Duplicate folders

Status Tracking

Updates invoice processing status in SQL tables.

🛠️ Tech Stack

Automation: n8n

AI / LLM: Google Gemini (via n8n LangChain nodes)

Programming: JavaScript

Database: Microsoft SQL Server

Scripting: PowerShell

File Handling: Windows File System

Data Formats: PDF, JSON

📂 Repository Structure
.
├── MainExtractionFlowGermanClient.json   # Main n8n workflow
├── ExtractionofScannedPDFs.json          # Reusable sub-workflow
├── README.md                             # Project documentation

⚙️ Setup & Usage

Import the .json workflow files into n8n.

Configure:

File system paths for scanned invoices

Microsoft SQL Server credentials

AI API credentials (Google Gemini)

Ensure PowerShell is enabled on the host machine.

Run manually or via the Schedule Trigger for automated execution.

✅ Use Cases

Accounts Payable Automation

Invoice Digitization & Archiving

Finance Process Automation

AI-based Document Processing

RPA / Workflow Automation Projects

📈 Impact

Reduced manual invoice processing effort

Improved data accuracy and consistency

Enabled scalable, reusable invoice workflows

Production-ready automation with logging and error handling

🔮 Future Enhancements

OCR fallback for low-quality scans

Email-based invoice ingestion

Dashboard for invoice processing status

Multi-currency support

Cloud storage integration (Azure / AWS / GDrive)
