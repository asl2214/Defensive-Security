## Overview
For this project, we played the role of a SOC analyst at a small company called Virtual Space Industries (VSI). The scenario that was given was that a rival company called JobeCorp was rumored to launch a cyberattack on VSI. Our job was to create a SIEM that would monitor potential attacks on VSI's systems and applications. The team was given **Windows Server Logs** and **Apache Server Logs** that represented normal internet activity. The Windows Server Logs contain intellectual property of VSI's next-generation virtual reality programs while Apache Server Logs are from VSI's main public-facing website. Baseline logs were then compared to attack logs to check the efficacy of the thresholds chosen for alerts. 

## Reviewing Normal Windows Server Logs

We first analyzed Windows Server Logs of normal activity. The fields we looked at were signature_id, signature, user, status, and severity. Three reports were created: a report of the table of signatures and associated signature ID's, severity levels and the percentages of each level, and a comparison of the success and failure of Windows activity. Three Alerts were created based on the fields of failed Windows activity, successful login signature, and deleted user account signature. All reports and emails were sent to SOC@VSI-company.com. 

### Reports

Table of signatures and associated signature IDs was created from the the signature_id field for identification: 
![..](Images/signature_id-and-signature-table.png)

Severity levels and the percentages of each level report allowed for quick understanding of the severity levels of the logs being viewed:
![..](Images/severity-levels-table.png)

Comparison of the success and failure of Windows activity presented if there was any suspicious activity based on the number of failed activities on the server: 
![..](Images/percentage-of-status-success-and-failure.png)

### Alerts

Hourly count of failed Windows activity was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/failed_windows_activity_baseline.png)
![..](Images/failed-windows-activity.png)

Hourly count of the signature "an account was successfully logged on" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold:
![..](Images/successful_login_baseline.png)
![..](Images/successful-login-alert.png)

Hourly count of the signature "a user account was deleted" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/users_deleted_baseline.png)
![..](Images/users-deleted.png)

### Dashboard

Once these reports and alerts were created, a dashboard was created for easier viewing. 

![..](Images/Windows_Server_Monitoring_Logs_Dashboard.png)

## Reviewing Normal Apache Server Logs
Next, we analyzed Apache Server Logs of normal activity. The fields we looked at were methods, referer_domain, status, clientip, and useragent. Three reports were also generated according to these fields - a table of different HTTP request methods, top 10 referrer domains to VSI's website, and the count of each HTTP response code. Two alerts were made to follow up after the reports: hourly international activity and hourly count of the HTTP POST request method. All reports and emails were sent to SOC@VSI-company.com. 

### Reports

Table of HTTP Request Methods activity: 
![..](Images/HTTP-Methods-logs.png)

Top 10 referrer domains to VSI's website:
![..](Images/top-10-referrer-domains-logs.png)

Count of each HTTP Response Codes: 
![..](Images/HTTP-Response-Codes-log.png)

### Alerts

Hourly count of international activity was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/IP-activity-outside-the-US.png)

Hourly count of the HTTP POST Request Method was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold:
![..](Images/HTTP-POST-alert.png)


### Dashboard

After successfully creating the reports and alerts, we created a dashboard to view fields that we thought were significant to know. 

![..](Images/apache_dashboard.png)

## Reviewing Attack Activity Logs




## Conclusion



## Extra
