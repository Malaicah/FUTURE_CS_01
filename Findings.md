# Detailed Findings - Vulnerability Assessment

**Websites Scanned:**  
- https://nexactf.tech  
- https://example.com  

**Date:** 08 April 2026 - 08 May 2026  


## High Risk Finding

### 1. SQL Injection (High Risk)
**Affected Site:** nexactf.tech  

**Simple Explanation:**  
Attackers can insert harmful code into the website’s forms (like login or registration). This could let them steal, change, or delete important information from the database.

**Fix Steps:**  
- Use secure coding methods (prepared statements) when talking to the database.  
- Check and clean all user inputs before using them.


## Medium Risk Findings

### 2. Unsafe Content Security Policy (Medium Risk)
**Affected Site:** nexactf.tech  

**Simple Explanation:**  
The website allows dangerous inline code (JavaScript and CSS). This makes it easier for attackers to inject harmful scripts (XSS attacks).

**Fix Steps:**  
- Update the security policy to block unsafe inline code.  
- Use safer methods (nonces or hashes) for any code that must run inline.


## Low Risk Findings

### 3. Missing Important Security Headers (Low Risk)
**Affected Sites:** Both websites  

**Simple Explanation:**  
The websites are missing basic protection headers. These headers help stop attacks like clickjacking and data interception.

**Fix Steps:**  
- Add these headers:  
  - Strict-Transport-Security (forces secure HTTPS)  
  - X-Frame-Options (prevents clickjacking)  
  - X-Content-Type-Options (stops dangerous content guessing)

### 4. Server Information Visible (Low Risk)
**Simple Explanation:**  
The website shows what software and version it is using. This gives attackers useful clues to target weaknesses.

**Fix Steps:**  
- Hide the server version information from visitors.


**Note:**  
All scans were done safely in passive mode only. No attacks were performed on the websites.
