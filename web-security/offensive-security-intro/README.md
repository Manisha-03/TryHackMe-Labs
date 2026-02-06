# Offensive Security Intro

## Overview 
This lab was my introduction to basic offensive security concepts using a deliberately vulnerable banking application hosted on TryHackMe. The goal was to understand how simple misconfigurations in web applications can be
identified and abused.

## Objective
- Find hidden or unlinked pages on a web application
- Identify insecure administrative functionality
- Practice basic web enumeration techniques

## Tools Used
- dirb
- TryHackMe AttackBox (VM)
- Web browser

## Approach
I started by performing directory enumeration against the target website to identify pages that were not accessible through the normal user interface.After discovering hidden endpoints, I manually reviewed them in the browser
to understand their purpose and potential security impact.

## Findings
- The `/images` directory was publicly accessible
- A hidden `/bank-transfer` endpoint allowed administrative actions without requiring authentication

## Impact
The exposed bank transfer page allowed account balances to be modified without any form of authorization. In a real-world scenario, this could lead to financial fraud or data manipulation.

## Key Takeaways
- Hidden pages should never be assumed to be secure
- Enumeration is a critical first step in web application testing
- Business logic flaws can be as dangerous as technical vulnerabilities

## Disclaimer
This activity was completed in a legal, sandboxed TryHackMe environment for learning and educational purposes only.
