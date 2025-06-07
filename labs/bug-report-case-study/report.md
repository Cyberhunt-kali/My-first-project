# 🐞 Vulnerability Report - Case Study

## 🔍 Target:
[REDACTED] (Public Government Website)

## 🛠️ Type of Vulnerability:
- Broken Authentication (IDOR)
- Information Disclosure
- Unauthenticated Access to Private Data

## 📋 Steps to Reproduce:
1. Visit: `https://finance.jharkhand.gov.in/viewBill?billNo=1001`
2. Without login, change `billNo` to `1002`, `1003`, etc.
3. You will see financial details of other users


## 🔐 PoC (Proof of Concept):

```http
GET /viewBill?billID=12345 HTTP/1.1
Host: [REDACTED]

