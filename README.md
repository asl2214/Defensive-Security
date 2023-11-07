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
We chose 15 counts as our threshold based on our baseline which we based off of the highest number of events that could possibly happen within the hour. 

$%$

Hourly count of the signature "an account was successfully logged on" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold:
![..](Images/successful_login_baseline.png)
![..](Images/successful-login-alert.png)
Similar to the process of our previous alert, we chose 22 counts as our threshold because normal activity indicates the highest activity as 21 counts within an hour. 

Hourly count of the signature "a user account was deleted" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/users_deleted_baseline.png)
![..](Images/users-deleted.png)
Finally, we chose 25 counts as our threshold based on the highest count being 22 events in one hour. 

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
![..](Images/international_activity_baseline.png)
![..](Images/IP-activity-outside-the-US.png)
From the normal activity count per hour, the highest number count we found was 120 events and so we chose 125 counts as our threshold. 

Hourly count of the HTTP POST Request Method was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold:
![..](Images/HTTP_Post_baseline.png)
![..](Images/HTTP-POST-alert.png)
The highest number of events that we found in our baseline 

### Dashboard

After successfully creating the reports and alerts, we created a dashboard to view fields that we thought were significant to know. 

![..](Images/apache_dashboard.png)

## Reviewing Attack Activity Logs

Next, we were provided logs from cyber attacks that VSI experienced due to (the most likely suspect) JobeCorp. The solutions that we got from normal activity logs were put to the test to check if they worked. 

## Windows Server Attack Logs

When we compared the reports, we found a striking difference in numbers compared to baseline logs in our reports. Most of our alerts were set off as well with the exception of the "users deleted" alert. 

### Reports

Severity Levels:
+ baseline
![..](Images/severity-levels-table.png)
+ attack
![..](Images/windows-severity-attack.png)
The attack log indicates a major difference in statistical numbers compared to normal activity in terms of severity level. There was a jump from 329 events to 1111 events in High severity and a slight decrease in informational severity from 4435 counts to 4283 counts. 

$~$

Success and failure login status:
+ baseline
![..](Images/percentage-of-status-success-and-failure.png)
+ attack
![..](Images/windows-status-attack.png)

### Alerts

## Apache Attack Logs

Similar to the results in our Windows Server Attack Logs, the Apache Attack Logs also found a significant difference in numbers across the board. 

### Reports



### Alerts

## Conclusion



## Extra
