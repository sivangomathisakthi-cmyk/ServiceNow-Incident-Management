# ServiceNow Incident Management

## Project Title

**Implement Client Script & UI Policy (Incident)**

## Project Description

This project demonstrates the implementation of Client Scripts and UI
Policies in ServiceNow Incident Management.

The purpose of this project is to control Incident form behavior,
validate user input, automatically update field values, and maintain
consistent data entry.

## Objectives

- Implement UI Policies on the Incident table.
- Make fields mandatory based on conditions.
- Control field read-only behavior dynamically.
- Automatically populate field values using Client Scripts.
- Validate Incident records before submission.
- Prevent unwanted list-editing changes.
- Maintain data accuracy and consistency.

## Technologies Used

- ServiceNow
- JavaScript
- Client Scripts
- UI Policies
- Incident Management

## UI Policy

### High Impact Control

**Table:** Incident

**Condition:** Impact is 1 - High

When the Impact of an Incident is set to High:

- Assignment Group becomes mandatory.
- Urgency becomes read-only.
- The policy is reversed when the condition becomes false.

## Client Scripts

### 1. onChange Client Script

When Impact is changed to High, the script automatically sets
Urgency to High.

It also displays an informational message to the user.

### 2. onSubmit Client Script

Before submitting an Incident, the script checks whether:

- Impact is High.
- Assigned To is empty.

If both conditions are true, the Incident cannot be submitted and
an error message is displayed.

### 3. onCellEdit Client Script

This script prevents the State field from being changed through
list editing.

The user is asked to open the Incident form instead.

## Project Structure

```text
ServiceNow-Incident-Management/
│
├── README.md
│
├── Client-Scripts/
│   ├── onChange.txt
│   ├── onSubmit.txt
│   └── onCellEdit.txt
│
├── UI-Policies/
│   └── High-Impact-Control.txt
│
└── Screenshots/
    ├── UI-Policy.png
    ├── onChange.png
    ├── onSubmit.png
    ├── onCellEdit.png
    ├── Test-Error.png
    └── Final-Output.png
