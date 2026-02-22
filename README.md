# Quilter Advisor Assistant

A RAG-based question answering system for Quilter advisor support documentation. 
The assistant retrieves relevant content from approved PDF sources and generates 
grounded answers, refusing to respond outside the scope of those documents.

## Overview

- Ingests and processes Quilter advisor support PDFs
- Indexes content using a Chroma vector database
- Accepts natural language queries via an interactive notebook interface
- Answers are strictly grounded in the supplied documentation
- Falls back to directing users to the Contact Centre when information is unavailable

## Setup

### Requirements
- Python 3.12.3
- An OpenAI API key

### Running

Open and run `notebook.ipynb` from the first cell. The notebook will handle 
ingestion, vector DB construction, and the assistant interface automatically.

## Platform

Developed and tested on TUXEDO OS, Linux x86_64, Python 3.12.3. Windows 
compatibility is not guaranteed — the core pipeline is portable, but path handling 
or Chroma/library builds may require minor adjustments on Windows.

## Notes

- The Chroma database is built fresh on each full run; no pre-built index is included
- PDFs are not included in the repository and must be sourced from the Quilter website