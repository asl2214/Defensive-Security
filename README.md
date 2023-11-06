## Overview
For this project, we played the role of a SOC analyst at a small company called Virtual Space Industries (VSI). The scenario that was given was that a rival company called JobeCorp was rumored to launch a cyberattack on VSI. Our job was to create a SIEM that would monitor potential attacks on VSI's systems and applications. The team was given **Windows Server Logs** and **Apache Server Logs** that represented normal internet activity. The Windows Server Logs contain intellectual property of VSI's next-generation virtual reality programs while Apache Server Logs are from VSI's main public-facing website. 

## Reviewing Normal Windows Server Logs

We first analyzed Windows Server Logs of normal activity. The fields we looked at were signature_id, signature, user, status, and severity. Three reports were created: a report of the table of signatures and associated signature ID's, severity levels and the percentages of each level, and a comparison of the success and failure of Windows activity. Three Alerts were created based on the fields of failed Windows activity, successful login signature, and deleted user account signature. All reports and emails were sent to SOC@VSI-company.com. 

### Reports

Table of signatures and associated signature IDs was created from the the signature_id field for identification: 
![..](Images/blah)

Severity levels and the percentages of each level report allowed for quick understanding of the severity levels of the logs being viewed:
![..](Images/blah)

Comparison of the success and failure of Windows activity presented if there was any suspicious activity based on the number of failed activities on the server: 
![..](Images/blah)

### Alerts

Hourly count of failed Windows activity was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/blah)

Hourly count of the signature "an account was successfully logged on" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold:
![..](Images/blah)

Hourly count of the signature "a user account was deleted" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/blah)

### Dashboard

Once these reports and alerts were created, a dashboard was created for easier viewing. 

![..](Images/blah)



## Reviewing Normal Apache Server Logs
Next, we analyzed Apache Server Logs of normal activity. The fields we looked at were methods, referer_domain, status, clientip, and useragent. Three reports were also generated according to these fields - a table of different HTTP request methods, top 10 referrer domains to VSI's website, and the count of each HTTP response code. Two alerts were made to follow up after the reports: hourly international activity and hourly count of the HTTP POST request method. All reports and emails were sent to SOC@VSI-company.com. 

### Reports

Table of signatures and associated signature IDs was created from the the signature_id field for identification: 
![..](Images/blah)

Severity levels and the percentages of each level report allowed for quick understanding of the severity levels of the logs being viewed:
![..](Images/blah)

Comparison of the success and failure of Windows activity presented if there was any suspicious activity based on the number of failed activities on the server: 
![..](Images/blah)

### Alerts

Hourly count of failed Windows activity was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/blah)

Hourly count of the signature "an account was successfully logged on" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold:
![..](Images/blah)

Hourly count of the signature "a user account was deleted" was created as an alert to notify of any suspicious increase if the amount passed the chosen threshold: 
![..](Images/blah)

### Dashboard

Once these reports and alerts were created, a dashboard was created for easier viewing. 

![..](Images/blah)

## Reviewing Attack Activity Logs



## Conclusion



## Extra
