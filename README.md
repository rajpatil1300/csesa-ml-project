# Automated Regulatory Compliance Auditor

## Project Overview
This project is a Natural Language Processing (NLP) tool designed to automate the initial phase of regulatory compliance auditing. In the financial and legal sectors, professionals often spend hours manually cross-referencing business documents against voluminous rulebooks. This system automates that process.

The application ingests a library of regulatory rules (in JSON format) and a set of business documents (in text format). It utilizes TF-IDF (Term Frequency-Inverse Document Frequency) vectorization and Cosine Similarity to semantically map specific clauses in the documents to relevant regulations in the knowledge base.

## Features
- **Knowledge Base Ingestion:** Parses unstructured JSON regulatory data into a structured DataFrame.
- **Semantic Search Engine:** Uses Scikit-Learn to build a Vector Space Model of the regulations.
- **Automated Auditing:** Scans new documents, splits them into paragraphs, and flags sections that reference specific rules.
- **Relevance Scoring:** Assigns a confidence score to every match to help auditors prioritize their review.

## Technical Architecture
- **Language:** Python 3.8+
- **Key Libraries:** - `pandas`: Data manipulation and structured storage.
  - `scikit-learn`: Implementation of TF-IDF and Cosine Similarity.
  - `numpy`: Numerical operations.
- **Input Data:**
  - Regulatory Rules: JSON format containing rule IDs and text passages.
  - Target Documents: Plain text (.txt) files representing contracts or reports.

## Installation and Usage

1. **Prerequisites**
   Ensure you have Python installed. Install the required dependencies:
   ```bash
   pip install pandas scikit-learn numpy jupyter
