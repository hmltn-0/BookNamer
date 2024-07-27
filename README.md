# Apple Books Script

## Introduction

This script renames all the PDF files in the Apple Books app based on the title and author extracted from the text within each PDF. This helps you organize your Apple Books collection automatically.

## Project Structure

The project has the following components:

1. **Apple Books Interface:**
   - A small API library to interact with the Apple Books app (including different modalities like desktop app versus iCloud).
   - Functions to list all PDF files, read/write metadata, etc.
   
2. **PDF Content Extraction and Title/Author Decision:**
   - Extract text content from each PDF.
   - Pass the extracted content to a Large Language Model (LLM) to decide the correct title and author.
   
## Detailed Steps

1. **Installation:**
   We'll be using the following libraries:
   - Python
   - pdf2text
   - requests
   - llama?

2. **Apple Books Interface:**
   - Develop a module that provides an interface to interact with PDF files in the Apple Books app.

3. **PDF Content Extraction and Title/Author Decision:**
   - Extract text from each PDF using `pdftotext`.
   - Pass the extracted text to an LLM to determine the correct title and author.
   - Use the functions from the Apple Books Interface to update the metadata of the PDF files.

## Usage:

1. **Run the Script:**
   Simply download the script and run it:
   ```shell
   ./rename_ibooks.sh
   ```

## Example:

Before:

```
example titles and authors:
1231223432
unknown new

qenlksdoh
arixvc3
```

After running the script:

```
categories of homological blah blah
spencer pacy

invocation as metalogic
sunniva jayson
```
