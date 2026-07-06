# Automation Guide

Title: Automation Guide
Version: 0.3.0
Status: Draft
Owner: AIG Engineering
Last Updated: 2026-07-06
Review Date: 2026-07-06
Approved By: AIG Engineering

## GitHub Automation for Document Updates

This repository includes a GitHub Actions workflow that can create or update a Markdown document directly from a workflow dispatch event.

## How it works

1. Open the Actions tab in GitHub.
2. Select the workflow named "Sync Documents".
3. Run it manually.
4. Provide:
   - document_path: the path to the file to create or update
   - document_content: the Markdown content to write
   - commit_message: optional commit message

## Notes

- The workflow requires the repository to allow GitHub Actions to write contents.
- In Settings > Actions > General, ensure workflow permissions allow read and write access.
- This is a manual workflow, but it can be extended to run from webhooks or external automation later.
