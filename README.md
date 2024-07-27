# Apple Books Script

## Introduction

This script renames all the PDF files in the Apple Books app based on the title and author extracted from the text within each PDF. This will help you to organize your Apple Books collection more efficiently.

## Project Structure

The project is divided into two distinct parts:

1. **Apple Books Interface:**
   - This part aims to provide functions to interact with the Apple Books app specifically for handling PDF files. This will act as a small library that we can test rigorously.

2. **PDF Content Extraction and Title/Author Decision:**
   - This part of the project will:
      - Extract text content from each PDF.
      - Pass the extracted content to a Large Language Model (LLM) to decide the correct title and author.
      - Use the Apple Books "API" developed in Part 1 to update the metadata of the PDF files with the decided title and author.

## Detailed Steps

1. **Installation:**
   - Ensure you have `pdftotext` and `exiftool` installed. You can install these using Homebrew:
     ```bash
     brew install poppler exiftool
     ```

2. **Apple Books Interface:**
   - Develop a module that provides an interface to interact with PDF files in the Apple Books app.
   - Functions to list all PDF files, read/write metadata, etc.

3. **PDF Content Extraction and Title/Author Decision:**
   - Extract text from each PDF using `pdftotext`.
   - Pass the extracted text to an LLM to determine the correct title and author.
   - Use the functions from the Apple Books interface to update the metadata of the PDF files.

## Usage:

1. **Run the Script:**
   - Place the script in the same directory as the `README.md`.
   - Execute the script:
     ```bash
     ./rename_pdfs.sh
     ```

## Note
- The script assumes the extracted title and author information is correct; validate this input where necessary.

## Example:

Before:
```
/path/to/apple_books/
├── file1.pdf
└── file2.pdf
```

After running the script:
```
/path/to/apple_books/
├── Author1-Title1.pdf
└── Author2-Title2.pdf
```

