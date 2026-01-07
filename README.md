# dt-business-analyst-assignment
DT Business Analyst Role Test Drive Assignment

This assignment simulates the kind of real-world problem-solving DT Analysts and Fellows do inside busy clinics and healthcare businesses.
The focus is on clarity of thought, practical system design, and respect for doctor and staff time, rather than perfect data or heavy tools.


## Task 1: Clinic Inventory Statistical Audit

Objective

The objective of this task is not full inventory reconciliation, but to design daily statistical micro-audits that can detect sales-entry errors and inventory mismatches early in a clinic environment where medicines are manually entered and not barcoded.

The system is designed to:

>Work with imperfect, real-world data
>Take minimal staff time
>Reduce revenue leakage
>Improve SOP discipline without increasing the doctor’s cognitive load
>Where Inventory Errors Are Most Likely to Occur

Based on real clinic operations, inventory errors most commonly occur in the following situations:

1.High-volume medicines
Fast-moving medicines are frequently sold and are more likely to have missed or incorrect sales entries.

2.Unit conversion mistakes
Errors such as entering tablets instead of strips or bottles instead of units slowly accumulate and distort stock levels.

3.Shift changes and handovers
Sales made near shift changes are sometimes entered late or not entered at all.

4.Peak hours and emergencies
During rush hours, patient care takes priority over system entry, increasing the chance of skipped or delayed entries.

5.Backdated or delayed data entry
Entries made from memory later in the day often contain quantity errors.

Daily Statistical / Randomized Micro-Audit Checks

These checks are designed to be lightweight, repeatable, and realistic for daily clinic use.

1. Random Item Check (Daily)

Randomly select 5–10 medicines each day

For each item, check:
Opening Stock + Purchases − Sales ≈ Current Stock

Small tolerances are acceptable

Purpose:
Creates discipline because staff know any item can be checked, without creating pressure.
2. High-Volume Medicine Focus Check

Identify the top-selling medicines

Compare daily sales with stock movement

Flag cases where:

Sales increase but stock does not reduce

Stock reduces without recorded sales

Purpose:
Targets areas with the highest revenue risk.
3. Negative or Zero Stock Detection

Flag:

Negative stock values

Zero stock while sales are still occurring

Purpose:
These almost always indicate missed entries or unit errors.
4. Simple Sales Spike Detection

Compare today’s sales with the average of the last 7–10 days

Flag:

Sudden spikes

Sudden drops to zero for regularly sold items

Purpose:
Detects abnormal patterns rather than exact mismatches.
5. Rotation-Based Category Checks

Assign different categories on different days
(e.g., antibiotics, syrups, injectables)

Purpose:
Ensures full coverage over time without overwhelming staff.

How These Checks Improve SOP Discipline

Checks are predictable in process but unpredictable in items, discouraging shortcuts

Errors are caught early, avoiding month-end firefighting

Accountability improves without blame

Doctors are kept out of daily inventory issues and only see repeated or high-risk patterns

Task 1 Summary

This system focuses on:

>Detection over perfection
>Patterns over punishment
>Daily discipline over periodic audits

It reduces revenue leakage while fitting naturally into a busy clinic workflow.


## Task 2: Patient Care & Communication System Design

Objective

The objective is to design a simple patient communication and follow-up system using HMS data and Google Sheets that reduces WhatsApp chaos while preserving care quality and minimizing doctor involvement in routine communication.

Classification of Patient Messages

Patient messages can be classified into two broad categories:

Automated Messages

>Appointment reminders
>Follow-up reminders
>Lab report readiness notifications
>Prescription refill reminders

Human-in-the-Loop Messages

>New symptoms
>Adverse medication reactions
>Emergency or urgent concerns
>Complex follow-up questions

This classification ensures automation without compromising patient safety.

Google Sheet–Based Control System

A Google Sheet acts as a lightweight control center with fields such as:

>Patient ID
>Visit date
>Follow-up due date
>Message type
>Message status
>Doctor intervention required (Yes/No)

Routine messages are automatically handled, while only flagged cases reach the doctor.

Reducing Doctor Cognitive Load

>Doctors review only escalated cases
>Staff manage routine communication through the sheet
>Patient care quality is preserved without constant interruptions
>Communication becomes structured instead of reactive

Optional Automation (High-Level)

This system can later be automated using:

>Google Apps Script for triggers
>Messaging APIs for SMS/WhatsApp delivery

Automation is optional and can be added gradually without disrupting workflows.

Overall Conclusion

Both systems are designed with the same principles:

>Respect for doctor time
>Practical implementation inside real clinics
>Low friction for staff
>Early detection of issues rather than delayed correction

The focus is on thinking clearly and designing systems that actually work, not on heavy tools or perfect data.
