# **Bug Tracking for CSOP Background Fund Management System**

### **Overview**
The bug tracking system is an essential tool for identifying, recording, and resolving issues in the CSOP Background Fund Management System. It provides a systematic approach to monitor defects and ensure their timely resolution to maintain the stability of the system.

### **Bug Reporting Process**

1. **Identify the Bug**: 
   - A bug is any unexpected behavior or defect in the system, including errors, crashes, performance issues, or incorrect results.
   - Testers and users report bugs when they encounter issues during testing or usage.

2. **Create a Bug Report**: 
   - Bug reports are created in the bug tracking system to capture detailed information about the issue.

   **Required Information for a Bug Report**:
   - **Title**: A brief description of the issue.
   - **Description**: Detailed explanation of the bug, including steps to reproduce, expected results, and actual results.
   - **Priority**: The severity of the bug (Low, Medium, High, Critical).
   - **Status**: The current state of the bug (Open, In Progress, Resolved, Closed).
   - **Environment**: The environment where the bug was found (e.g., Production, Staging, Development).
   - **Screenshots/Logs**: Attach screenshots, error logs, or any other supporting documents.

   **Example Bug Report**:
   - **Title**: Incorrect performance data for the Global Equity Fund.
   - **Description**: When retrieving performance metrics for the Global Equity Fund (ticker: GEF001), the Time-weighted Return (TWR) is showing an incorrect value of 10% when it should be 8%.
   - **Steps to Reproduce**:
     1. Go to the fund details page for "Global Equity Fund."
     2. Click on "Performance Metrics."
     3. Observe the TWR value.
   - **Expected Result**: The TWR value should be 8%.
   - **Actual Result**: The TWR value is incorrectly shown as 10%.
   - **Priority**: High
   - **Status**: Open
   - **Environment**: Staging

3. **Track the Bug**:
   - Once reported, the bug is assigned a status (e.g., Open, In Progress) and tracked until resolved.

4. **Fix and Testing**:
   - The development team investigates the issue, applies a fix, and tests it to verify the bug has been resolved.

5. **Resolution and Closure**:
   - After testing, the bug is marked as "Resolved" if fixed, and "Closed" once confirmed.

### **Bug Tracking Example Workflow**

1. **Bug Created**: A bug is reported for the API returning incorrect performance data.
2. **Bug Assignment**: The bug is assigned to a developer for investigation.
3. **Investigation and Fix**: The developer fixes the issue in the codebase and tests locally.
4. **QA Testing**: The QA team tests the fix in a staging environment.
5. **Bug Closure**: After successful validation, the bug is marked as closed.

### **Bug Tracking Tools**

We use [Jira](https://www.atlassian.com/software/jira) as our bug tracking system.

