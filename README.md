# Streamlining IT Procurement: Automating Standard Laptop Procurement

## 📌 Project Overview

The **Standard Laptop Procurement Automation** project is a ServiceNow-based solution designed to streamline and automate the IT hardware procurement process.

The system uses **Service Catalog** and **Flow Designer** to automate the lifecycle of a standard laptop request, starting from request submission and approval through task creation and assignment to the Hardware team.

The solution reduces manual task creation, improves request visibility, minimizes processing delays, and provides a consistent workflow for handling laptop procurement requests.

---

## 🎯 Project Objective

To design and deploy an automated, end-to-end IT procurement solution within **ServiceNow** using **Service Catalog** and **Flow Designer**.

The main objectives are to:

- Streamline standard laptop hardware requests.
- Automate the approval workflow.
- Automatically create fulfillment tasks for approved requests.
- Assign hardware configuration tasks to the appropriate team.
- Reduce manual intervention and processing delays.
- Improve visibility and tracking of procurement requests.
- Provide timely notifications to users and stakeholders.

---

## 👥 Target Users

### 1. End Users / Employees
Employees can request a standard laptop through the Service Catalog by providing the required information.

### 2. Approvers / Managers
Managers can review submitted laptop requests and approve or reject them based on the request details.

### 3. IT Fulfillment / Service Desk
The Hardware/IT team automatically receives structured tasks for laptop configuration, provisioning, and delivery.

---

## 🚀 Modules & Features Implemented

### 1. Service Catalog / Catalog Items

A custom **Standard Laptop Order** Catalog Item is created to allow employees to submit laptop requests.

The catalog item can include variables such as:

- Laptop Model
- Department
- Delivery Location
- Justification
- Requested For

---

### 2. Workflows & Automation – Flow Designer

An automated **Flow Designer** workflow is configured to process submitted laptop requests.

The flow performs the following operations:

1. Detects a new Standard Laptop request.
2. Initiates the approval process.
3. Processes the approval decision.
4. Creates a Catalog Task for approved requests.
5. Assigns the task to the Hardware team.
6. Updates the task with the required laptop configuration details.
7. Completes the procurement workflow.

### Workflow

```text
Employee
   ↓
Standard Laptop Catalog Item
   ↓
Submit Request
   ↓
Approval
   ↓
Approved?
 ┌───────────────┐
 │               │
YES              NO
 │               │
 ↓               ↓
Create         Reject /
Catalog Task    Close
 │
 ↓
Assign to Hardware
 │
 ↓
Laptop Configuration
 │
 ↓
Provisioning & Delivery
 │
 ↓
Request Completed
