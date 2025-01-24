# 🎀 Elecom-NoSQL 🎀
## Overview

A severe NoSQL injection vulnerability has been identified in the **Elecom WAB-S733IW-AC/PD Wireless Access Point**, allowing malicious actors to manipulate database queries through crafted payloads. This critical flaw could enable unauthorized access to sensitive information, potentially exposing configuration data, user details, and other confidential assets.

## Vulnerability Details

By exploiting this vulnerability, adversaries can bypass intended access controls, compromising the device's security. The issue arises when the device fails to properly validate and sanitize user inputs, especially during POST requests to the `/adv_virtual.asp` endpoint. Specific payload parameters, such as `%5b%26exists%5d=false` and `%5b%26exists%5d=true`, have proven effective in manipulating database queries, highlighting a lack of robust input validation and sanitization.

## Impact

Successful exploitation of this vulnerability can lead to significant consequences, including but not limited to:

1. **Database Tampering**: Malicious users can inject queries to modify, delete, or retrieve sensitive data, compromising the confidentiality and integrity of the device's database.
2. **Access Control Bypass**: Attackers can bypass authentication and authorization mechanisms, gaining unauthorized access to the device and its associated systems.
3. **Data Exposure**: Sensitive information, such as configuration data and user credentials, can be retrieved through this vulnerability.
