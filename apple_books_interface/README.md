# Apple Books Interface

## Introduction

This module provides two methods to interact with the Apple Books app for handling PDF files: via iCloud and Desktop.

## Methods of Interaction

### 1. iCloud

**Advantages:**
- Can be accessed from any device with internet connectivity; can hypothetically be run from any computer or even a remote server scheduled automatically, rather than on your own personal computer with your books on it.

**Disadvantages:**
- May require reverse engineering or an unofficial API to interact with iCloud, as no official API is readily available.
- Potentially limited by iCloud's own API restrictions and rate limits.

### File Access:
- Hard to ascertain direct file paths to the PDFs as they are managed by iCloud.
- Requires knowledge of iCloud's internal structure and API endpoints.

### 2. Desktop App

**Advantages:**
- Easier to access file paths directly for the local PDF files.
- More control over file handling and metadata manipulation as files are stored locally.

**Disadvantages:**
- Requires you to have a functioning, up-to-date MacBook, and to run the script on it.

### File Access:
- Direct access to the file paths of the PDF files in the local Books directory.
- Easier to find and manipulate the files stored in Books' local directory.

## Conclusion

Both methods have their own sets of advantages and disadvantages. The choice between them depends on the specific needs of the user. Locally on a MacBook is much easier, but iCloud may be useful in some fallback cases.
