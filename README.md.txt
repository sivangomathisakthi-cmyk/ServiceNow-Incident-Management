# ServiceNow Incident Management

## Project Title
Implement Client Script & UI Policy (Incident)

## Objective
This project demonstrates the use of ServiceNow UI Policies and Client Scripts
to control Incident form behavior and maintain consistent data entry.

## UI Policy

### High Impact Control
- Table: Incident
- Condition: Impact is 1 - High
- Assignment Group: Mandatory
- Urgency: Read-only

## Client Scripts

### 1. onChange
Automatically sets Urgency to High when Impact is High.

### 2. onSubmit
Prevents submission when Impact is High and Assigned To is empty.

### 3. onCellEdit
Prevents State from being changed using list editing and asks the user
to open the Incident form.

## Testing
The project was tested for:
- High Impact Incident validation
- Assigned To mandatory behavior
- Urgency field behavior
- State list editing restriction
- State update from the Incident form

## Conclusion
This project demonstrates how UI Policies and Client Scripts can be used
in ServiceNow to enforce dynamic field behavior, validate data, and
maintain data quality.