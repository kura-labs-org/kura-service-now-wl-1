# ServiceNow Administration Fundamentals - Assignment Instructions

## Overview

**Company Context**: You're a ServiceNow Administrator at Uber, where reliable network infrastructure is critical for maintaining ride-hailing services across hundreds of cities worldwide.

**Your Role**: As a junior ServiceNow admin on the IT Operations team, you've been tasked with fixing a critical gap in the incident management system that supports Uber's network infrastructure.

**Why This Matters**: Last month, a critical network outage in the San Francisco data center went unnoticed for 2 hours because the notification system wasn't working properly, causing widespread service disruptions and affecting thousands of riders and drivers. The incident resulted in significant revenue loss and regulatory scrutiny.

**The Scenario**: Your manager discovered that critical network incidents aren't triggering email notifications to the Network Operations team. Yesterday, someone created a Critical priority incident for a network outage, but no notifications were sent to the team. The system was supposed to automatically alert engineers within minutes of a critical incident being created. You need to investigate and fix whatever is preventing the notification system from working before the next critical incident occurs.

Review ServiceNow's [Priority Lookup Rules](https://www.servicenow.com/docs/bundle/yokohama-it-service-management/page/product/incident-management/task/def-prio-lookup-rules.html) to understand how Priority is calculated from Impact and Urgency values.

Your task is to fix the system so that urgent network incidents trigger immediate email notifications to IT engineers, preventing SLA breaches.

## Current System State

Your instance includes:
- Flow Designer workflow: "Kura Workload 1"
- Email notification: "Incident Assignment Notification"
- User group: "Networking Operations" 
- SLA definition: "Urgency High" (1 hour response time)

## Assignment Objectives

### 1. Configure the Flow Properly
Configure the flow to trigger notifications for critical network incidents.

### 2. Ensure Notifications Reach the Proper Team
Ensure the notification system alerts the correct team when critical incidents occur.

### 3. Test and Validate the Working System
- Create test incidents with **network category and critical priority**
- Verify emails are actually sent and received
- Confirm the fixed workflow prevents SLA breaches through timely alerts

### 4. AI Scenario Analysis

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
├── Diagram.png (Draw.io architecture diagram)
```

### 2. Update Set Requirements

Your update set MUST contain these **records**:
- Working Flow Designer workflow records ("Kura WL1")
- **Actual email records from sys_email table (proof emails were sent)**
- User group records for "Network Operations"
- **Test incident records demonstrating the working system**
- All supporting table entries that make the system functional

#### Creating Your Update Set

1. Navigate to the 'All' tab
2. Search 'local update set'
3. Create a new update set
   - Give the update set a name
   - Click 'Submit and make current'
4. Add the required items to the update by navigating to their corresponding table records and clicking 'add to update set' when you have the records open
5. **Hint**: You can add a flow to an update set by opening the flow and clicking the ellipses button next to 'edit flow' button and clicking 'force save'

### 3. README.md Content Requirements
- **System Overview**: Description of the working incident notification system
- **Implementation Steps**: How you fixed the workflow and configured notifications
- **Architecture Diagram**: Visual representation of the complete system flow. Use Draw.io
- **AI Scenario**: How AI agents could enhance incident routing (100-150 words)

## Submission Instructions

1. **Test your complete system thoroughly**
2. **Create your update set with all working components and evidence**
3. **Upload to GitHub with proper documentation**
4. **Submit your repository URL to Canvas**