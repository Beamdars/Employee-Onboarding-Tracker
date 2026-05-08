# Entity Relationship Diagram

End-to-end flow:
HR submits new hire via Power Apps form
       ↓
Power Automate creates item in [New Hires] SP list
       ↓
Flow auto-creates task items in [Onboarding Tasks] SP list
(one row per task, linked to the new hire)
       ↓
IT staff update task status directly in SharePoint list
(or via a simple Power Apps view on top of the list)
       ↓
Power Automate monitors list for overdue/blocked tasks
       ↓
Reminders at T-5 days, escalations at T-2 days
       ↓
HR gets readiness summary email on start date
       ↓
Power BI reads SP lists → live dashboard
