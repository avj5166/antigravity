# 📊 VA Operations Tracker — Google Sheets Setup Guide

> Copy this structure exactly into Google Sheets. One sheet = one source of truth for your entire consultancy.

---

## SHEET 1: "STUDENT MASTER" (Main Dashboard)

### Columns to Create (in order, left to right)

| Column | Header Name | Type | Notes |
|---|---|---|---|
| A | Student ID | Text | VA-001, VA-002... auto-increment |
| B | Full Name | Text | Student's full name |
| C | Phone | Number | With country code |
| D | Email | Email | Primary email |
| E | WhatsApp Number | Number | May differ from phone |
| F | Parent Name | Text | Father/Mother name |
| G | Parent Phone | Number | Emergency contact |
| H | City | Text | City in India |
| I | Target Country | Dropdown | France (for now) |
| J | Target Program | Text | Masters / Bachelors / PhD |
| K | Field of Study | Text | Engineering, Business, etc. |
| L | Target Intake | Dropdown | Sep 2025 / Jan 2026 / Sep 2026 |
| M | Date of Enrollment | Date | When they joined your consultancy |
| N | Assigned Counselor | Text | Your name / staff name |
| O | **CURRENT STAGE** | Dropdown | See Stage List below |
| P | Stage Start Date | Date | When they entered current stage |
| Q | Stage Deadline | Date | When this stage must be done |
| R | Days in Stage | Formula | =TODAY()-P(row) |
| S | Status | Dropdown | On Track / At Risk / Urgent / Complete |
| T | Notion Portal Link | URL | Link to their personal Notion page |
| U | Last Updated | Date | =TODAY() when you update |
| V | Notes | Text | Free-form counselor notes |
| W | Total Fee Charged | Number | In INR |
| X | Fee Paid | Number | In INR |
| Y | Fee Due | Formula | =W(row)-X(row) |
| Z | Visa Outcome | Dropdown | Pending / Approved / Rejected |

---

## STAGE DROPDOWN OPTIONS (for Column O)

Paste this exact list into your Google Sheets dropdown for Column O:

```
01 - Initial Inquiry
02 - Enrolled / Agreement Signed
03 - Profile Assessment
04 - University Shortlisting
05 - Document Collection (Academic)
06 - SOP / LOR Writing
07 - University Applications Submitted
08 - Campus France Account Created
09 - Campus France Documents Submitted
10 - Campus France Interview Scheduled
11 - Campus France Interview Done
12 - Campus France Attestation Received
13 - Waiting for University Offer Letter
14 - Offer Letter Received
15 - Visa Document Preparation
16 - VFS Appointment Booked
17 - Visa Application Submitted
18 - Visa Under Processing
19 - Visa Approved ✅
20 - Visa Rejected ❌
21 - Pre-Departure Briefing Done
22 - Student Departed 🛫
```

---

## CONDITIONAL FORMATTING RULES (Color Coding)

Set these rules on Column S (Status):

| Status | Background Color | Text Color |
|---|---|---|
| On Track | Light Green (#b7e1cd) | Dark Green |
| At Risk | Light Yellow (#fce8b2) | Dark Orange |
| Urgent | Light Red (#f4cccc) | Dark Red |
| Complete | Light Blue (#c9daf8) | Dark Blue |

---

## SHEET 2: "DOCUMENT TRACKER"

One row per student. Track every required France visa document.

### France Student Visa — Master Document Checklist

| Column | Document | Status Options |
|---|---|---|
| A | Student ID | Link to Sheet 1 |
| B | Student Name | Pull from Sheet 1 |
| C | Valid Passport (6+ months validity) | Not Submitted / Submitted / Verified ✅ / Issue ❌ |
| D | Passport Copy (all pages) | same |
| E | 2 Recent Passport Photos (35x45mm) | same |
| F | Completed Visa Application Form (CERFA) | same |
| G | Campus France Attestation | same |
| H | University Admission Letter (Lettre d'Admission) | same |
| I | Academic Transcripts (10th, 12th, Degree) | same |
| J | Degree/Diploma Certificates | same |
| K | Official Translation (if not in French/English) | same |
| L | Financial Proof - Bank Statement (Last 6 months) | same |
| M | Financial Proof - Fixed Deposit / Scholarship Letter | same |
| N | Financial Proof - ITR of sponsor (Last 2 years) | same |
| O | Proof of Accommodation in France | same |
| P | Health Insurance (covering entire stay) | same |
| Q | Travel Insurance | same |
| R | Cover Letter / Application Letter | same |
| S | OFII Form (filled, not signed) | same |
| T | Visa Fee Receipt (€99 paid at VFS) | same |
| U | Return Ticket (sometimes required) | same |
| V | Birth Certificate | same |
| W | Gap Certificate (if applicable) | same |
| X | Work Experience Letter (if applicable) | same |
| Y | IELTS / TCF / DELF Score Card (if required) | same |
| Z | All Documents Complete? | YES / NO |

---

## SHEET 3: "UNIVERSITY TRACKER"

Track each student's university applications.

| Column | Header | Notes |
|---|---|---|
| A | Student ID | |
| B | Student Name | |
| C | University 1 Name | |
| D | University 1 Program | |
| E | University 1 Deadline | Date |
| F | University 1 Applied? | Yes / No |
| G | University 1 Status | Applied / Offer Received / Rejected / Accepted |
| H | University 2 Name | |
| I | University 2 Program | |
| J | University 2 Deadline | |
| K | University 2 Applied? | |
| L | University 2 Status | |
| M | University 3 Name | |
| N | University 3 Program | |
| O | University 3 Deadline | |
| P | University 3 Applied? | |
| Q | University 3 Status | |
| R | University 4 Name | |
| S | University 4 Program | |
| T | University 4 Deadline | |
| U | University 4 Applied? | |
| V | University 4 Status | |
| W | Final University Chosen | |
| X | Acceptance Letter Received | Yes / No |
| Y | Notes | |

---

## SHEET 4: "DEADLINES CALENDAR"

All upcoming deadlines in one view — sorted by date.

| Column | Header |
|---|---|
| A | Student ID |
| B | Student Name |
| C | Deadline Type |
| D | Deadline Date |
| E | Days Until Deadline (=D(row)-TODAY()) |
| F | Status |
| G | Responsible Person |

### Deadline Types to Track:
- Campus France Account Deadline
- Campus France Interview Date
- University Application Deadline
- Scholarship Application Deadline
- VFS Appointment Date
- Visa Decision Expected By
- Flight Date

**Sort Column E (Days Until) ascending** — students closest to deadlines always appear at top.

---

## SHEET 5: "WEEKLY DASHBOARD" (Summary View)

Use these formulas to see your business at a glance:

```
Total Active Students:     =COUNTIF(Sheet1!Z:Z,"<>Visa Rejected")-COUNTIF(Sheet1!Z:Z,"Visa Approved")
Visas Approved This Month: =COUNTIFS(Sheet1!Z:Z,"Visa Approved",Sheet1!U:U,">="&DATE(YEAR(TODAY()),MONTH(TODAY()),1))
At Risk Students:          =COUNTIF(Sheet1!S:S,"At Risk")
Urgent Students:           =COUNTIF(Sheet1!S:S,"Urgent")
Revenue This Month:        =SUMIFS(Sheet1!W:W,Sheet1!M:M,">="&DATE(YEAR(TODAY()),MONTH(TODAY()),1))
Fee Outstanding:           =SUM(Sheet1!Y:Y)
```

---

## HOW TO USE DAILY (5-Minute Morning Routine)

1. Open Sheet 4 (Deadlines) — check anything due in the next 7 days
2. Open Sheet 1 (Student Master) — filter for "Urgent" or "At Risk" students
3. Update Column O (Current Stage) for anyone who moved forward yesterday
4. Update Column U (Last Updated) for any student you touch
5. Open their Notion page and update their stage there too (see Document 03)

---

## GOOGLE SHEETS SETUP TIPS

### Freeze Rows
- Freeze Row 1 (headers) so they stay visible when scrolling
- View → Freeze → 1 row

### Data Validation (Dropdowns)
- Select the column → Data → Data Validation → List of items → paste the options

### Protect Sheets
- Right-click on Sheet tab → Protect Sheet → only you can edit formulas

### Share with Students
- Do NOT share this sheet with students — this is internal only
- Student-facing information goes on their Notion portal (see Document 03)

---

*Document 01 of 05 | VA Consultancy Operations System*
