Sure! Here is a README file that explains the usage and functionality of the provided Google Apps Script code:

---

# Google Sheets Script Project

## Overview

This project consists of a Google Apps Script that enhances the functionality of a Google Sheet. The script performs three main functions:

1. Restricts editing based on user roles.
2. Generates feedback for resumes in the sheet using the Gemini API.
3. Sends the generated resume feedback to specified email addresses.

## Features

1. **Edit Restriction**: Ensures only the respective user or an admin can edit certain rows.
2. **Feedback Generate**: Uses the Gemini API to generate feedback for texts in the sheet.
3. **Email Summaries**: Sends the generated Feedback to specified email addresses.
4. **Dedaline management**: Sends the missed deadline mail to specified email address if the resume is not submitted.

## Files

The project consists of four main script files:

1. `emailprotection.gs` - Handles the edit restrictions.
2. `deadlinemanagement.gs` - Manages the deadline.
3. `GenerateResumeFeedback.gs` - Sends the generated summaries via email.
4. `button.gs` - For a button on menu bar of the sheet to run the script.

## Installation and Setup

1. **Create a Google Sheet**:
   - Create a new Google Sheet.
   - Add two sheets within the Google Sheet: `Student` and `Admins`.

2. **Configure the Sheets**:
   - **Student Sheet**: The first column (A) should contain the student email addresses, the second column (B) should have the resume pdf link, and the third column (C) will store the generated feedback.
   - **Admins Sheet**: The first column (A) should contain the email addresses of the admin users.

3. **Open the Script Editor**:
   - In your Google Sheet, navigate to `Extensions` > `Apps Script`.

4. **Create the Script Files**:
   - Create the four script files (`emailprotection.gs`, `deadlinemanagement.gs`, `generarteResumeFeedback.gs`, and `main.gs`) in the Apps Script editor.

5. **Copy the Provided Code**:
   - Copy the provided code into their respective script files in the Apps Script editor.

6. **Save the Scripts**:
   - Save each script file.


### 1. Edit Restriction

The `emailprotection.gs` function checks if the user attempting to edit a row is either the owner of the email in the first column or an admin. If the user is not authorized, the change is reverted and a message is shown.

### 2. Generating Feedback

The `generateResumeFeedback.gs` function fetches text entries from column B of the `Student` sheet, sends them to the Gemini API for summarization, and writes the summaries to column D and send the feedback to the respective emails.

- **API Key**: Ensure you have a valid Gemini API key and replace the placeholder in the script with your actual key.

### 3.deadlinemanagement.gs

The `sendSummariesByEmail` function automates the process of sending reminder emails to the respective row owners if a resume is not submitted by the deadline.


### Running the Scripts

- To generate feedback click on custom menu in the sheet on the menu bar.

## Debugging

- Use `Logger.log` statements to debug and view logs in the Apps Script editor under `View > Logs`.
- Ensure proper permissions are granted to the script for accessing the Google Sheet and sending emails.


