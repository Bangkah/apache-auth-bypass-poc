# CVE-2026-1337 - Apache WebPortal SQL Injection PoC

Proof of Concept (PoC) script to demonstrate an authentication bypass vulnerability via SQL Injection affecting Apache WebPortal versions **3.2.0 through 3.4.5**.

## Overview
This script targets the login endpoint of the vulnerable application, using a standard SQL Injection payload injected into the user identifier field to bypass authentication mechanisms without requiring valid credentials.

* **Vulnerability Type:** SQL Injection (Authentication Bypass)
* **Target Endpoint:** `/auth/login`
* **Affected Software:** Apache WebPortal (Versions 3.2.0 - 3.4.5)
* **Author:** sec-research

---

## Prerequisites

Make sure you have Python 3 installed along with the required HTTP library. You can install the dependencies using pip:

```bash
pip install requests

```

---

## Usage

Run the script from your terminal by specifying the target's IP address or domain name along with the port number.

```bash
python3 exploit.py --target <target-ip-or-domain> --port <port-number>

```

### Example:

```bash
python3 exploit.py --target 192.168.1.50 --port 80

```

---

## Disclaimer

> **IMPORTANT:** This software is provided for educational purposes and authorized security research / penetration testing only. Do not use this script against systems you do not own or do not have explicit legal authorization to test. The creator assumes no liability for any misuse or damage caused by this program.

---

## Mitigation

If you are running an affected version of Apache WebPortal, update immediately to version **3.4.6** or later, where parameterized queries and robust input sanitization are implemented to resolve this vulnerability.


```
