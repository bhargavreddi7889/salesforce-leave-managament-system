# Leave Management System (Salesforce)

A simple and efficient Leave Management System built on Salesforce Platform using Clicks-Not-Code approach.  
The system allows employees to submit leave requests and enables managers/approvers to approve or reject them.  
Status updates and email notifications are handled automatically.

---

## Features
- Custom Leave Request Object
- Submit leave for approval
- Manager approval workflow
- Auto status updates (Submitted → Approved / Rejected)
- Email notifications to employee on approval or rejection
- Dashboard to view leave requests

---

##  Objects & Fields

### Custom Object: `Leave_Request__c`
| Field Label | API Name | Type | Description |
|---|---|---|---|
| Employee Name | Employee_Name__c | Lookup(User) | Who is requesting leave |
| Approver | Approver__c | Lookup(User) | Who approves the leave |
| Start Date | Start_Date__c | Date | Leave start date |
| End Date | End_Date__c | Date | Leave end date |
| Leave Type | Leave_Type__c | Picklist | Sick, Casual, Earned, Emergency |
| Reason | Reason__c | Long Text Area | Reason for leave |
| Status | Status__c | Picklist | Submitted, Approved, Rejected (Default: Submitted) |

---

## Approval Workflow
**Approval Process Name:** Leave Request Approval

| Event | Action |
|---|---|
| On Submission | Sends request to Approver |
| On Approval | Status → Approved & send approval email |
| On Rejection | Status → Rejected & send rejection email |

---

## ✉ Email Alerts
- `Leave_Approved_Notification` → Sent to Employee on Approval
- `Leave_Rejected_Notification` → Sent to Employee on Rejection

---

##  UI / Dashboard
Built using **Lightning App Builder**:
- List View of Leave Requests
- Used for Instructor / HR demonstration

---

## ✅ How to Test
1. Go to **Leave Requests** → **New**
2. Fill request → Set Approver = yourself (demo case)
3. Click **Submit for Approval**
4. Open **Related → Approval History**
5. Click **Approve** (or Reject)
6. Check Status + Email

---

## 📸 Screenshots
See `/screenshots` folder in this repository (add yours).

---

## 💡 Conclusion
This project demonstrates practical skills in:
- Salesforce Customization
- Approval Automation
- Email Alerts Configuration
- Lightning UI Configuration

This is fully deployable for real small team HR workflows.

