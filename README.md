# Description of SQL Email Cleanup Project

## Situation
American University’s database contained outdated and bounced email addresses of a sheer number of users, reducing the effectiveness of solicitation campaigns like fundraising and cluttering contact records. Ensuring accurate contact information was critical to improving outreach and maintaining a clean database.

## Task
My task was to develop a SQL script to identify and deactivate bounced email addresses, select the next preferred email (users have more than one email in the database) for each user based on business rules, and update the database accordingly to enhance solicitation accuracy and database integrity.

## Action
**Data Aggregation**: Wrote a SQL script to create a temporary table (aa_bounced) that joined bounced email data (aa_enBounced) with active contact and email records, flagging bounced emails for analysis.

**Email Prioritization Logic**: Implemented a ROW_NUMBER() function to rank emails per constituent based on business rules (e.g., prioritizing non-.edu, alumni, or recent emails), ensuring the most suitable email was selected as preferred.

**Status Updates**: Generated lists to update preferred email statuses and deactivate bounced emails, using dynamic naming conventions (e.g., CONVERT(Date, getDate())) for auditability.

**Automation**: Designed the script to run monthly, ensuring continuous database maintenance.

## Result
The SQL script successfully identified and deactivated bounced emails while updating preferred email statuses, improving solicitation accuracy by ensuring reliable contact information. This enhanced fundraising campaign effectiveness and maintained a clean, efficient database, aligning with organizational goals for operational excellence.
