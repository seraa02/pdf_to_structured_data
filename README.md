# PDF to Structured Data Pipeline

This repository provides a complete pipeline to convert clinical History & Physical PDF documents into clean, tabular CSVs suitable for downstream analysis.

## Features

- **pdf_structured**: Demo notebook for parsing one PDF into a structured CSV  
- **multiple_pdf_structured**: Notebook for processing a folder of PDFs and aggregating outputs  
- **Section Extraction**: Regex-based slicing of standard H&P sections (Chief Complaint, History of Present Illness, Physical Exam, etc.)  
- **LLM Parsing**: use llama 3 on groq via LangChain to enforce a strict `Date,Category,Section,Description` schema  
- **Detailed vs Compact Outputs**:
-  **output_structured.csv**: structured csv generated from pdfs
-  **csv_outputs**: structured csv generated from multiple pdfs (folder)
  - **csv_1.csv**: one row per individual finding (maximum granularity)  
  - **csv_2.csv**: groups entries by Date + Category with semicolon-delimited descriptions (easier scanning)  

## Prerequisites

- Python 3.8 or higher  
- A valid Groq API key (set in environment variable `GROQ_API_KEY`)  



