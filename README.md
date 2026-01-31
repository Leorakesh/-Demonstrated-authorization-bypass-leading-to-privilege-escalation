# -Demonstrated-authorization-bypass-leading-to-privilege-escalation
Day 38 of 100 days challenge 

Day 38 – Authorization Bypass & Privilege Escalation

On Day 38, I explored how authorization bypass vulnerabilities can allow attackers to perform privilege escalation, gaining access to restricted functionality and sensitive data.

What is Authorization Bypass?

Authorization ensures users can only access what they are permitted to.
An authorization bypass happens when an application fails to properly check user roles, allowing a low-privileged user to act as a higher-privileged one.

Example risk:

Normal user accessing admin endpoints

Modifying IDs in requests (IDOR)

Missing role validation on APIs

What is Privilege Escalation?

Privilege escalation occurs when an attacker moves from:

Low privilege → High privilege (Admin / Root)

This can lead to:

Account takeover

Data leakage

System compromise

Full application control

Common Causes

Missing role checks

Broken access control

Insecure Direct Object References (IDOR)

Trusting client-side validation

Misconfigured APIs

Testing Techniques

Change user IDs in requests

Access admin endpoints as a normal user

Replay requests with modified roles

Test API routes without tokens

Inspect frontend restrictions

Prevention Methods

Enforce server-side authorization

Use RBAC (Role-Based Access Control)

Validate every request

Restrict sensitive endpoints

Log and monitor access attempts

Key Takeaway

Authorization bypass is one of the fastest ways attackers gain full control. Always validate permissions on the server side, not the client.
