# ServiceNow Administration Fundamentals - Assignment Instructions

# ServiceNow Administration Fundamentals - Workload 1 Instructions

## Assignment Overview

**Company Context**: You're a ServiceNow Administrator at Uber, where reliable network infrastructure is critical for maintaining ride-hailing services across hundreds of cities worldwide.

**Your Role**: As a junior ServiceNow admin on the IT Operations team, you've been tasked with fixing a critical gap in the incident management system that supports Uber's network infrastructure.

**Why This Matters**: Last month, a critical network outage in the San Francisco data center went unnoticed for 2 hours because the notification system wasn't working properly, causing widespread service disruptions and affecting thousands of riders and drivers. The incident resulted in significant revenue loss and regulatory scrutiny.

**The Scenario**: Your manager discovered that critical network incidents aren't triggering email notifications to the Network Operations team. The system was supposed to automatically alert engineers within minutes of a critical incident being created, but notifications aren't being sent. You need to investigate and fix whatever is preventing the notification system from working before the next critical incident occurs.

Your task is to fix the system so that urgent network incidents trigger immediate email notifications to IT engineers, preventing SLA breaches.

## Current System State

Your instance includes:
- Flow Designer workflow: "Kura Workload 1"
- Email notification: "Incident Assignment Notification"
- User group: "Networking Operations" 
- SLA definition: "Urgency High" (1 hour response time)

## Assignment Objectives

### 1. Fix the Flow Designer Workflow
- What is the status of "Kura Workload 1" flow?
- The SLA "Urgency High" SLA required engineers to respond within 1 hour. Is the flow currently being triggered and sending notifications for 'Critical' priority incidents?
- Ensure the workflow connects to the notification system

### 2. Connect Flow to Email Notification System
The flow should trigger the "Incident Assignment Notification" which should be sent to the "Network Operations" group.
- Is the notification correctly configured to send emails to the "Network Operations" group?
- Test that notifications are actually sent when the workflow triggers

### 3. Verify User Group Configuration
- Ensure the notification references the correct group name that exists in your system
- Fix any name inconsistencies between groups and notifications
- Does the "Network Operations" group have any members assigned?

### 4. Test and Validate the Working System
- Create test incidents with network category and critical priority
- Verify emails are actually sent and received
- Confirm the fixed workflow prevents SLA breaches through timely alerts

### 5. AI Scenario Analysis

**Hypothetical Scenario:** Your company operates globally across multiple time zones. Critical incidents often occur outside business hours when senior engineers aren't available. The current escalation process follows a rigid hierarchy that doesn't account for engineer expertise, current availability, or incident complexity, leading to prolonged resolution times.

In your README.md, include an "AI Scenario" section explaining how an AI agent could enhance your incident notification system to:
- Intelligently route incidents based on engineer expertise and availability
- Consider time zones and current workloads when selecting responders  
- Learn from historical resolution patterns to improve future routing decisions

## Deliverables

### 1. GitHub Repository Structure
```
/your-repo-name
├── README.md
├── kura-workload-complete.xml (update set file)
├── Diagram.png
```

### 2. Update Set Requirements
Your update set MUST contain these **records**:
- Working Flow Designer workflow records ("Kura WL1")
- **Actual email records from sys_email table (proof emails were sent)**
- User group records for "Network Operations"
- **Test incident records demonstrating the working system**
- All supporting table entries that make the system functional

### 3. README.md Content Requirements
- **System Overview**: Description of the working incident notification system
- **Implementation Steps**: How you fixed the workflow and configured notifications
- **Architecture Diagram**: Visual representation of the complete system flow
- **Testing Evidence**: Proof that emails are actually being sent
- **AI Scenario**: How AI agents could enhance incident routing (100-150 words)
- **Setup Instructions**: How someone else could replicate your working system

## Submission Instructions

1. **Test your complete system thoroughly**
2. **Create your update set with all working components and evidence**
3. **Upload to GitHub with proper documentation**
4. **Submit your repository URL to Canvas**