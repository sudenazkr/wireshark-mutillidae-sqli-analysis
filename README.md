# wireshark-mutillidae-sqli-analysis
Analysis of SQL Injection attack traffic using Wireshark on OWASP Mutillidae
# Wireshark SQL Injection Traffic Analysis (Mutillidae)

## 📌 Project Description
This project demonstrates how SQL Injection attack traffic can be captured 
and analyzed using Wireshark. The attack was performed on OWASP Mutillidae, 
a deliberately vulnerable web application, within a controlled lab environment.

## 🧪 Lab Environment
- Kali Linux (Attacker & Traffic Capture)
- Metasploitable 2 (Victim)
- OWASP Mutillidae II
- Wireshark

## 🎯 Attack Scenario
A SQL Injection login bypass attack was performed on the Mutillidae login page.
The goal was to observe how malicious input appears at the network level.

## 🔍 Traffic Analysis Steps
1. Wireshark capture was started on the Kali Linux machine.
2. A normal login request was sent to the application.
3. A SQL Injection payload was submitted via HTTP POST request.
4. HTTP traffic was filtered using Wireshark filters.
5. The malicious payload was identified inside the HTTP POST packet.

## 🚨 Findings
- User credentials and SQL Injection payloads were transmitted in clear text.
- This occurred because the application uses HTTP instead of HTTPS.
- Any attacker on the same network could capture and read sensitive data.

## 🛡️ Security Insight
Using HTTPS would encrypt the traffic and prevent attackers from reading 
credentials and payloads, although it would not eliminate the vulnerability itself.

## 📷 Screenshots
See the screenshots folder for captured packets and payload evidence.
