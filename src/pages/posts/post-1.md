
---

### Quick Notes: Windows Privilege Escalation via Active Directory

**1. Key Concepts in AD Escalation:**
- **Active Directory (AD)** is a prime target for privilege escalation due to its extensive role in managing network resources, user accounts, and permissions.
- Attackers look for **misconfigurations, outdated policies**, and **vulnerabilities** in AD to escalate privileges.

**2. Common Attack Vectors:**
- **Weak Passwords**: Weak or default passwords across accounts allow attackers to escalate privileges.
- **Unpatched Systems**: Exploiting vulnerabilities on unpatched machines for higher-level access.
- **Kerberos Attacks**: Attacks like **Pass-the-Ticket (PTT), Kerberoasting**, or **Pass-the-Hash (PTH)** leverage vulnerabilities in Kerberos authentication.
- **Misconfigured AD Groups**: Mismanaged groups (like giving too many permissions to a single group) enable attackers to escalate privileges if they compromise one member.

**3. Important Tools for AD Escalation:**
- **BloodHound**: Tool for mapping AD relationships to find potential escalation paths.
- **Mimikatz**: Extracts credentials from memory for attacks like **Pass-the-Hash**.
- **Impacket**: Collection of Python scripts useful for network recon and exploitation.
- **PowerView**: Part of PowerSploit, used to gather AD information (users, groups, permissions).

**4. Recommended AD Hardening Tips:**
- **Password Policies**: Enforce strong passwords, multifactor authentication (MFA), and regularly rotate passwords.
- **Regular Patching**: Ensure systems are patched to avoid known vulnerabilities.
- **Group Policy Object (GPO)** Hardening: Review GPOs for unnecessary permissions and harden sensitive group memberships.
- **Limit Admin Access**: Only grant admin privileges to necessary accounts and use **Privileged Access Workstations (PAWs)** for admin tasks.
- **Audit and Monitor AD**: Regularly audit AD logs for suspicious activities, monitor for new group memberships or admin privilege escalation.

**5. Attack Mitigation Strategies:**
- Use **Least Privilege Principle** to limit exposure in case of compromise.
- Implement **tiered access models** in AD to prevent full compromise from a single escalation point.
- Perform **regular vulnerability assessments** and **penetration testing** focused on AD security.

