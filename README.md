# Brute Force Attack and Malware Injection 

## Scenario

As part of my **Google Cybersecurity Professional Certificate**, I encountered a security breach scenario involving a **brute force attack** on the admin panel of the website **yummyrecipesforme.com**. A former employee carried out this attack to gain unauthorized access and lure users to a malicious website that contained malware.

---

## Incident Analysis

The attacker utilized a brute force method, repeatedly entering default administrative passwords until successfully gaining access. Once inside the admin panel, they altered the website’s source code, embedding **JavaScript** that prompted users to download a malicious file. This file redirected users to a fake version of the site, **greatrecipesforme.com**, where their systems were infected.

---

## Impact on Users

| **Impact**                  | **Description**                                                                               |
|-----------------------------|-----------------------------------------------------------------------------------------------|
| **Malware Distribution**     | Users were prompted to download a malicious file, leading to slow system performance.         |
| **Website Redirection**      | Users were redirected from the legitimate site to a fake one, compromising their experience.  |

---

## Investigation and Findings

To investigate the breach, I created a **sandbox environment** and used a **network protocol analyzer (tcpdump)** to track the suspicious activity:

| **Process**                  | **Description**                                                       |
|------------------------------|-----------------------------------------------------------------------|
| **DNS Request**               | Browser requested the IP address of yummyrecipesforme.com.            |
| **DNS Response**              | DNS server returned the correct IP.                                   |
| **HTTP Request**              | Browser requested the webpage.                                        |
| **Malware Download**          | Browser downloaded the malware file.                                  |
| **Redirection to Fake Site**  | Browser requested and connected to greatrecipesforme.com.             |

Further analysis of the downloaded file revealed the embedded **malware script** that redirected visitors to the fake website.

---

## Immediate Response

| **Immediate Action**                      | **Description**                                                                                   |
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| **Owner Attempted Access**                | The website owner attempted to regain control but was blocked due to a password change by the attacker. |
| **Mitigation by IT Team**                 | My team and I investigated, mitigated the event, and restored security.                            |

---

## Preventive Measures

| **Preventive Measure**                    | **Description**                                                                                   |
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| **Strong Password Policies**              | Enforced the use of strong, unique passwords and regular updates for administrative accounts.      |
| **Multi-Factor Authentication (MFA)**     | Added an extra layer of security for account access.                                               |
| **Regular Security Audits**               | Scheduled frequent security audits to identify vulnerabilities early.                              |
| **Intrusion Detection Systems (IDS)**     | Recommended deploying IDS to monitor suspicious activity.                                          |
| **Web Application Firewall (WAF)**        | Implemented a WAF to filter and monitor HTTP requests to the server.                               |
| **User Education**                        | Trained employees on best practices for password management and overall security.                  |

---

## Security Risk Assessment Report

### Part 1: Hardening Tools and Methods

| **Hardening Tool/Method**                 | **Description**                                                                                   |
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| **Multi-Factor Authentication (MFA)**     | Requires users to authenticate in more than one way before accessing the application.              |
| **Strong Password Policies**              | Policies that enforce password length, complexity, and regular updates.                            |
| **Firewall Maintenance**                  | Regular checks and updates of security configurations to stay ahead of potential threats.           |

---

### Part 2: Recommendations

| **Recommendation**                        | **Benefit**                                                                                        |
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| **Multi-Factor Authentication (MFA)**     | Reduces the chances of unauthorized access through brute force attacks by requiring more than one form of authentication. |
| **Strong Password Policies**              | Increases difficulty for malicious actors to gain unauthorized access by enforcing complexity and frequency of password changes. |
| **Regular Firewall Maintenance**          | Keeps the firewall’s traffic filtering rules up to date to protect against various cyber threats like DoS/DDoS attacks.       |

---

## Learning and Experience

This hands-on project provided valuable insights into the importance of robust password policies and proactive security measures. I also gained experience in responding to and mitigating real-world threats in a simulated environment, highlighting the need for continuous monitoring and regular security audits to prevent future incidents.

---

## Tools & Technologies Used

| **Tool/Technology**        | **Purpose**                                                      |
|----------------------------|------------------------------------------------------------------|
| **Sandbox Environment**     | Isolated environment for testing and analyzing the malware behavior. |
| **tcpdump**                 | Captured and analyzed network traffic related to the malware injection. |
| **Firewall & WAF**          | Configured to block malicious traffic and monitor HTTP requests. |

---

This project demonstrates my ability to apply cybersecurity best practices, detect and respond to breaches, and implement preventive measures in an educational setting. The experience further prepared me to handle real-world cybersecurity incidents and contribute to securing web applications effectively.

---
