# JARN Ansible Assessment — Markdown ➜ Google Doc (Colab)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jai-nayani/meeting-notes-to-google-doc/blob/main/Meeting_Notes_to_Google_Doc_Colab.ipynb)

Repository: https://github.com/jai-nayani/meeting-notes-to-google-doc

A personalized, production-quality Colab notebook that converts markdown meeting notes into a well-formatted Google Doc using the Google Docs API.

## Table of Contents
- [Overview](#overview)
- [Setup (Colab)](#setup-colab)
- [Required Scope](#required-scope)
- [Dependencies (installed in the notebook)](#dependencies-installed-in-the-notebook)
- [Deliverables](#deliverables)
- [Evaluation Fit](#evaluation-fit)
- [Author](#author)

## Overview
- Creates a new Google Doc programmatically
- Maps headings: H1 (title), H2 (sections), H3 (sub-sections)
- Preserves nested bullets and indentation (ordered + unordered)
- Converts `- [ ]` into real Google Docs checkboxes
- Styles @mentions (bold + color)
- Distinct footer styling (grey)
- Robust retries for transient API errors

## Setup (Colab)
1. Open `Meeting_Notes_to_Google_Doc_Colab.ipynb` in Google Colab.
2. Run the Install cell.
3. Run the Authenticate cell and upload your OAuth `credentials.json`.
4. Upload your markdown (or use `examples/original-meeting-notes.md` or `examples/product-team-sync.md`).
5. Run the conversion cell; a Google Docs link will be printed.

### Required Scope
- https://www.googleapis.com/auth/documents

## Dependencies (installed in the notebook)
- google-api-python-client
- google-auth-httplib2
- google-auth-oauthlib
- markdown-it-py==3.0.0
- beautifulsoup4==4.12.3

## Deliverables
- Working Colab notebook: `Meeting_Notes_to_Google_Doc_Colab.ipynb`
- Example markdown: `examples/original-meeting-notes.md`, `examples/product-team-sync.md`
- README with setup and run instructions

## Evaluation Fit
- Functionality: Creates a fully formatted Google Doc as specified
- Code Quality: Clear structure, meaningful names, humanized comments
- Error Handling: Exponential backoff retries for 429/5xx
- Documentation: This README + inline guidance in the notebook

## Author
Prepared by: Jai Adithya Ram Nayani
