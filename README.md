# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
Captured Web Activity and Email Header Information

1.Open Wireshark and start capturing on the active interface (Wi- Fi/Ethernet).

2.Perform activities like opening a website or sending an email through a client (e.g., Gmail via browser or Thunderbird).

3.Stop the capture once done.

![image](https://github.com/user-attachments/assets/542c0f6e-4603-4b08-9ef6-95f67327fc51)

# Analyzing Web Browser Artifacts

Analyze Queries:
.Filter: http

![image](https://github.com/user-attachments/assets/87e04602-61d2-403c-9697-81b2a983f7db)

.Filter: tcp

![image](https://github.com/user-attachments/assets/d8cd4137-8fcf-48d0-a744-30d5d20c167f)

Inspect HTTP GET/POST requests

![image](https://github.com/user-attachments/assets/f45b260a-1642-43b6-8cc0-89ac035f65ee)

Follow TCP Stream to reconstruct page request flow: Right-click a packet → Follow → TCP Stream.

![image](https://github.com/user-attachments/assets/2919482b-f034-48c1-8753-037b2efe1904)

Analyze dns Queries:

.Filter: dns

![image](https://github.com/user-attachments/assets/95ddd548-b81f-4fcc-95b0-41e13a3915fe)

# Email Header Analysis

# .Apply relevant filters
```
 For SMTP: tcp.port == 25 or 587
```

![image](https://github.com/user-attachments/assets/2884bcea-8ed4-46e2-af92-df87885912a0)


# .Locate email data

# .Look for SMTP packets to see sender/receiver email addresses. Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

# .Extract Email Header Fields Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.

![image](https://github.com/user-attachments/assets/0013f0bd-e597-4437-8518-fa68d3a8153a)




## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark.

