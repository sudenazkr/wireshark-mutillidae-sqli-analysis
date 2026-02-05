# SQL Injection Traffic Analysis with Wireshark

## 1. Objective
The objective of this analysis is to understand how a SQL Injection attack
appears at the network level and how it can be identified using Wireshark.

---

## 2. Attack Preparation
- The attacker machine is Kali Linux.
- The victim machine is Metasploitable 2 running OWASP Mutillidae.
- Wireshark was started on the Kali machine before sending any requests.

---

## 3. Normal Login Traffic
A normal login attempt was sent using standard credentials.


## Step 1 – Creating a User Account for Testing

### Screenshot
<img width="1657" height="883" alt="Ekran görüntüsü 2026-02-05 152329" src="https://github.com/user-attachments/assets/ff455f6d-ea44-4373-8984-08b103f2f96c" />

### Description
In this step, a new user account was created on the Mutillidae vulnerable web application.
This account will be used in the following steps to perform and analyze **SQL Injection attacks**.

Creating a valid user account allows us to interact with authenticated features of the application and observe how user-supplied input is processed by the backend.

### Purpose of This Step
The purpose of this step is to prepare a test user for later SQL Injection attempts and network traffic analysis using **Wireshark**.

## Step 2 – SQL Injection Attempt on Login Function

### Screenshot
<img width="1641" height="1045" alt="Ekran görüntüsü 2026-02-05 165644" src="https://github.com/user-attachments/assets/659063f1-0f2c-4b29-9bcf-074ce8d65688" />

### Description
In this step, an SQL Injection attempt was performed on the login functionality of the Mutillidae web application using the previously created user account.

Instead of submitting a normal password, an SQL Injection payload was injected into the password field to manipulate the backend SQL query logic.

### Injected Payload
```sql
' OR 1=1#




