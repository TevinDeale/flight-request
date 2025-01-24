# Flight Request Approval System

## Overview
A ServiceNow application that streamlines the flight request and approval process. The system automates flight validation and approval workflows based on cost thresholds, integrating with external aviation data to ensure accuracy.

## Key Features

### Flight Information Management
- Dynamic flight code generation combining airline ICAO code and flight number
- Integration with AviationStack API for real-time flight validation
- Automated flight details retrieval and form population

### Approval Workflow
- Automated approval for flights under $300
- Manager approval routing for flights over $300
- Email notifications for approval/rejection decisions
- Rejection reason documentation and communication

### Technical Components

#### Custom Database
- Airline reference table with ICAO codes
- Flight request records with status tracking

#### Automation
- Business Rule: Automated flight code generation
- Subflow: Flight validation via AviationStack API
- Flow: Multi-level approval routing
- UI Actions: Flight details retrieval and approval request initiation

#### Integration
- Custom spoke implementation for AviationStack API
- Email notification system integration

## User Experience
Users submit flight requests through a form interface with automated validation and real-time flight information population. The system handles approval routing and communication automatically, providing transparency throughout the process.

## Security and Controls
- Cost-based approval thresholds
- Designated approval group for high-value requests
- Automated status tracking and documentation
