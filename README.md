# YummyRecipesForMe.com Security Incident Analysis

This repository contains the investigation results for a simulated security incident affecting `yummyrecipesforme.com`. A former employee successfully executed a **brute-force attack** against the administrative login portal. This led to unauthorized access, 
allowing the attacker to modify the website’s source code, embed JavaScript to trigger a file download, and redirect users to a fake website,
distributing malware.

---

## Contents

| File/Folder            | Description                                                  |
|------------------------|--------------------------------------------------------------|
| `raw-evidence.txt`            | Raw data/logs.          |
| `security_incident_report.md` | Summary of findings, protocols, recommendations. |
| `README.md`            | This file, high-level summary.               |

---


## Summary of Incident

1. The attacker used default admin credentials he acquired through a brute-force attack.
2. Gained access to the admin panel of `yummyrecipesforme.com`.
3. Modified the website’s source code to include JavaScript that redirected users & prompted a malicious file download
4. Multiple users reported malware symptoms after running the file.
5. Analysis shows an unauthorized redirect and system compromise.

---

## Recommendations

### To Prevent Brute Force Attacks:
- Change default passwords on all administrative accounts.
- Account lockout after multiple failed login attempts.
- Use multi-factor authentication (MFA)
- Enforce strong password policies
- Monitor logs for suspicious login patterns.
