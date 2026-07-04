# Azure Security Notes

This document summarizes the security practices adopted throughout this repository.

The objective is to execute Azure laboratories following security best practices while avoiding exposure of sensitive information.

---

# Sensitive Information

The following information is never published:

- Subscription ID
- Tenant ID
- Client ID
- Client Secrets
- Storage Access Keys
- SAS Tokens
- Passwords
- Private Keys
- Personal or corporate email addresses
- Corporate environment information

---

# Screenshot Guidelines

Before publishing screenshots, verify that they do not expose sensitive information.

Always hide:

- Subscription IDs
- Tenant IDs
- Client IDs
- Secrets
- Access Keys
- SAS URLs
- Tokens
- Public IPs
- Corporate data

---

# Identity Security

The following practices are adopted:

- Enable Multi-Factor Authentication whenever possible
- Apply the Principle of Least Privilege
- Prefer Azure RBAC Groups instead of direct user assignments
- Remove temporary permissions after testing
- Review guest accounts regularly
- Separate administrative and standard accounts

---

# Storage Security

- Disable anonymous access
- Require HTTPS
- Enforce TLS 1.2 or newer
- Prefer Microsoft Entra ID authentication
- Limit SAS permissions
- Configure short SAS expiration times

---

# Network Security

- Avoid Public IPs whenever possible
- Use Network Security Groups
- Restrict RDP and SSH access
- Prefer Azure Bastion
- Use Private Endpoints whenever appropriate

---

# Resource Cleanup

After every laboratory:

- Remove unused resources
- Remove temporary permissions
- Remove temporary SAS tokens
- Delete Resource Groups
- Verify orphaned resources

---

# Disclaimer

This repository is intended for educational purposes and technical portfolio development.

All laboratories are executed in a personal Azure environment.

No production resources, corporate information or sensitive credentials are published.
