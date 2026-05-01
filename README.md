# Future_CS_01 - Vulnerability Assessment Report

## Task Overview
Passive Vulnerability Assessment of live website as part of the Future Interns Cyber Security Track.

## Websites Assessed
- **https://nexactf.tech**

## Tools Used
- **Nmap** - A Network reconnaissance and service/version detection
- **OWASP ZAP (Passive Scan)** - An Automated passive vulnerability scanning
- **Canva** - A Professional report design

## A Summary of the Key Findings

| Risk Level | Number of Alerts | Notable Issues |
| ---------- | ---------------- | -------------- |
| **High**   | 1                | Sql-Injection  |
| **Medium** | 2                | Unsafe CSP (`script-src 'unsafe-inline'` and `style-src 'unsafe-inline'`) | 
| **Low**    | Multiple         | Missing security headers (HSTS, X-Frame-Options, etc.) |

### Critical Finding
- **SQL Injection** vulnerability on `https://nexactf.tech` — This is a serious issue that could allow attackers to manipulate the backend database.

### Medium Risk Findings
- Content Security Policy allows `'unsafe-inline'` for both scripts and styles, weakening protection against XSS attacks.
