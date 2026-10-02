# Auto Ticket Classification Using Flow Designer in ServiceNow

## 📌 Project Overview

**Auto Ticket Classification Using Flow Designer** is a ServiceNow-based automation project developed using the **ServiceNow Developer Instance**.

The project automates the classification and routing of IT support tickets. When an incident is created in ServiceNow, the configured Flow Designer flow evaluates the ticket information and automatically determines the appropriate category and assignment group based on predefined conditions.

The main purpose of the project is to reduce manual ticket classification, improve ticket routing, and make the incident management process more efficient.

---

## 🎯 Problem Statement

In a traditional IT support environment, newly created incidents may need to be manually reviewed and assigned to the appropriate support team.

Manual classification can:

- Increase the time required to process tickets
- Cause incorrect categorization
- Result in tickets being assigned to the wrong support group
- Increase repetitive work for IT support teams
- Delay the initial handling of user issues

Therefore, an automated solution is required to classify and route tickets based on the information provided in the incident.

---

## 💡 Proposed Solution

This project uses **ServiceNow Flow Designer** to automate ticket classification.

The flow is configured to monitor newly created incident records. Based on the information available in the incident, the flow evaluates predefined conditions and performs the required actions.

### Workflow

```text
User creates an incident
        ↓
Incident record is created in ServiceNow
        ↓
Flow Designer is triggered
        ↓
Incident information is evaluated
        ↓
Classification conditions are checked
        ↓
Category/Subcategory is updated
        ↓
Assignment Group is determined
        ↓
Ticket is routed to the appropriate support team
```

---

## 🎯 Objectives

1. To automate IT ticket classification using ServiceNow Flow Designer.
2. To reduce manual intervention in ticket categorization.
3. To automatically route incidents to appropriate support groups.
4. To improve consistency in ticket classification.
5. To reduce errors caused by manual ticket assignment.
6. To demonstrate workflow automation using ServiceNow.
7. To improve the overall incident management process.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **ServiceNow Developer Instance** | Development and implementation environment |
| **Flow Designer** | Automation and workflow creation |
| **Incident Management** | Creation and management of support tickets |
| **ServiceNow Tables** | Storage of incident information |
| **Conditions and Actions** | Ticket classification and routing logic |

---

## ⚙️ ServiceNow Components Used

### 1. Incident Management

The Incident table is used to create and manage IT support tickets.

The incident contains information such as:

- Number
- Caller
- Short Description
- Description
- Category
- Subcategory
- Priority
- State
- Assignment Group
- Assigned To

### 2. Flow Designer

Flow Designer is the main automation component of this project.

It is used to define:

- Trigger conditions
- Classification conditions
- Actions
- Ticket updates
- Assignment group routing

### 3. Flow Trigger

The flow is configured to start when the required incident record is created or when the configured incident condition is satisfied.

### 4. Flow Logic

The flow checks the information available in the incident and compares it with the configured classification conditions.

### 5. Flow Actions

After identifying the ticket type, the flow updates the required incident fields and routes the ticket to the appropriate assignment group.

---

## 🔄 Ticket Classification Process

The project uses predefined conditions for classifying different types of tickets.

For example:

| Ticket Type | Example Issue | Classification | Assignment |
|-------------|---------------|----------------|------------|
| Hardware | Laptop is not working | Hardware | Hardware Support |
| Software | Application is not opening | Software | Software Support |
| Network | Internet is not working | Network | Network Support |
| Password | Password reset required | Account/Password | Service Desk |
| Access | Application access required | Access Request | Access Support |

> The exact categories and assignment groups can be modified according to the configuration implemented in the ServiceNow Developer Instance.

---

## 🏗️ System Workflow

```text
              ┌──────────────────┐
              │      User        │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Create Incident  │
              │   in ServiceNow  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │  Flow Designer   │
              │     Trigger      │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Evaluate Ticket  │
              │    Information   │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Classification   │
              │    Conditions    │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Update Incident  │
              │ Category/Fields  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Assign Support   │
              │      Group       │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Ticket Ready for │
              │     Support      │
              └──────────────────┘
```

---

## 🔧 Implementation in ServiceNow

### Step 1: Create Incident

An incident is created from the ServiceNow interface with the required issue details.

### Step 2: Configure Flow Designer

Navigate to:

**All → Process Automation → Flow Designer**

Create a new flow for incident classification.

### Step 3: Configure the Trigger

Configure the trigger based on the incident condition required for the project.

### Step 4: Add Classification Conditions

Configure conditional logic to identify the type of issue from the incident information.

For example:

```text
IF ticket information matches Hardware condition
        ↓
Set Hardware classification
        ↓
Assign Hardware Support
```

### Step 5: Configure Actions

Configure Flow Designer actions to update the required incident fields.

Possible actions include:

- Update Category
- Update Subcategory
- Update Assignment Group
- Update other required fields
- Add Work Notes if required

### Step 6: Activate the Flow

After configuring and testing the flow, activate it so that it can process applicable incident records.

---

## 🧪 Testing

Different incident scenarios are created in the ServiceNow Developer Instance to verify the behavior of the flow.

### Sample Test Cases

| Test Case | Incident Description | Expected Result |
|-----------|----------------------|-----------------|
| TC01 | Laptop is not working | Hardware classification and appropriate assignment |
| TC02 | Application is not opening | Software classification and appropriate assignment |
| TC03 | Internet connection problem | Network classification and appropriate assignment |
| TC04 | Password reset required | Account/Password classification and appropriate assignment |
| TC05 | User requires application access | Access classification and appropriate assignment |

The actual test results can be documented using screenshots from the ServiceNow Developer Instance.

---

## 📸 Screenshots

Screenshots of the actual ServiceNow implementation can be added here.

### Flow Designer

Add screenshot of the configured Flow Designer flow.

`Screenshot: Flow Designer configuration`

### Incident Creation

Add screenshot showing the incident before classification.

`Screenshot: Incident created in ServiceNow`

### Automated Classification

Add screenshot showing the updated category/subcategory.

`Screenshot: Automatically classified incident`

### Assignment Group

Add screenshot showing the assignment group selected by the flow.

`Screenshot: Automatically assigned support group`

---

## ✅ Expected Results

After successful execution of the flow:

- The incident is processed automatically.
- The ticket is classified according to the configured conditions.
- Relevant incident fields are updated.
- The ticket is routed to the appropriate assignment group.
- Manual classification effort is reduced.
- The incident management workflow becomes more structured.

---

## 🌟 Advantages

- Reduces repetitive manual work.
- Provides consistent ticket classification.
- Improves ticket routing.
- Reduces the possibility of incorrect assignment.
- Makes the incident management process more efficient.
- Uses ServiceNow's built-in automation capabilities.
- Can be modified and extended as business requirements change.

---

## ⚠️ Limitations

- Classification depends on the conditions configured in Flow Designer.
- Tickets with unclear or unexpected information may not match the configured conditions.
- Changes in categories or assignment groups may require modifications to the flow.
- Rule-based classification may not handle complex or ambiguous ticket descriptions without additional logic.

---

## 🚀 Future Enhancements

The project can be extended with advanced ServiceNow capabilities such as:

- AI-based ticket classification
- Natural Language Understanding
- Automatic priority prediction
- Predictive assignment
- ServiceNow Virtual Agent integration
- Automated notifications
- SLA-based escalation
- Performance dashboards and reporting
- Integration with additional ServiceNow applications

---

## 📊 Project Outcome

The project demonstrates how **ServiceNow Flow Designer** can be used to automate the classification and routing of IT support tickets.

By implementing predefined classification logic, the system can reduce manual ticket handling and provide a structured process for routing incidents to the appropriate support teams.

---

## 👥 Project Information

**Project Title:** Auto Ticket Classification Using Flow Designer

**Platform:** ServiceNow Developer Instance

**Domain:** IT Service Management (ITSM)

**Technology:** ServiceNow Flow Designer

**Project Type:** Naan Mudhalvan Project

**Team Members:**
- Member 1: *Your Name*
- Member 2: *Team Member Name*
- Member 3: *Team Member Name*

---

## 📚 References

- ServiceNow Developer Documentation
- ServiceNow Flow Designer Documentation
- ServiceNow IT Service Management Documentation
