# n8n-web-team-project-consolidation
Web Team daily automation (n8n + Google Sheets): Every weekday evening, reads today's entries, extracts unique project names from task lists (looking for "project:…"), and fills the "Projects" and "No_of_Projects_Working_On" columns for better reporting and timesheet visibility.

Trigger: Cron / Schedule – Mon–Fri 19:00 PKT
Input: Google Sheet "DailyLogsData" – rows where Date = today
Parsed column: "In-Progress Tasks" (configurable in code)
Detection pattern: lines containing "project:" or "Project:"
Output columns updated: Projects (multi-line list), No_of_Projects_Working_On (number)
Purpose: Make monthly/weekly reporting easier by having clean project lists per person/day
