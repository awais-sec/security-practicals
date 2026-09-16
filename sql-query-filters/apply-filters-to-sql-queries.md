# Apply Filters to SQL Queries

## Project Description

This project involved analyzing organizational data to identify potential security issues through SQL. The task focused on examining login attempt patterns and employee machine information from company databases. As a security professional, I investigated failed login attempts occurring after office hours and analyzed employee distribution across departments and office locations. This work demonstrates practical application of SQL for security analysis and data investigation.

## Retrieve After-Hours Failed Login Attempts

I recently discovered a potential security incident that occurred after business hours, at 18:00.

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = 0;
```

19 login attempts were made after hours.

## Retrieve Login Attempts on Specific Dates

A suspicious event occurred on 2022-05-09. To investigate this event, I reviewed all login attempts that occurred on this day and the day before.

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';
```

With the help of `WHERE`, I isolated the logs for these two days. 75 login attempts were made across these two days.

## Retrieve Login Attempts Outside of Mexico

It was determined that this activity did not originate in Mexico, so I investigated login attempts that occurred outside of Mexico.

```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

`NOT` is used since we wanted to see only the attempts that were not in Mexico, and whenever a wildcard (`%`) is used, `LIKE` is needed. The results showed 144 login attempts from countries other than Mexico.

## Retrieve Employees in Marketing

My team wanted security updates for employees whose machines are in the East side building and who work in the Marketing department.

```sql
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

7 employees need security updates.

## Retrieve Employees in Finance or Sales

My team needed to push a security update to the Finance and Sales departments.

```sql
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';
```

## Retrieve All Employees Not in IT

My team reported that one more update needed to be made, but it had already been completed in the IT department — so all other departments still needed to be patched.

```sql
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

## Summary

The analysis successfully identified multiple security-related events, including failed login attempts outside business hours, and provided detailed employee access patterns by department and location. These findings helped identify potential vulnerabilities in authentication systems and access management. The results demonstrate how SQL can be effectively used to investigate security events and support organizational security posture.

---
*Awais Ahmed's own completed work.*
