# Azure Cost Management

This document describes the cost optimization practices adopted throughout the AZ-104 laboratories.

The objective is to minimize unnecessary Azure costs while maintaining realistic administration scenarios.

---

# Cost Management Strategy

The following practices are applied across all laboratories:

- Use a dedicated Azure subscription for study purposes.
- Organize resources into dedicated Resource Groups.
- Apply standard tags.
- Configure Azure Budgets.
- Prefer low-cost SKUs whenever possible.
- Remove resources after completing each lab.
- Review Azure Cost Management frequently.

---

# Recommended Budget

Recommended monthly budget:

| Setting | Value |
|----------|-------|
| Budget | USD 20–30 |
| Alerts | 50%, 80%, 100% |

Budgets provide visibility into Azure spending but do not replace resource cleanup.

---

# Resource Cost Guidelines

| Resource | Recommendation |
|----------|----------------|
| Resource Groups | No direct cost |
| Storage Accounts | Standard LRS |
| Virtual Machines | Small SKUs only |
| Public IP | Remove when no longer needed |
| Azure Bastion | Deploy only when required |
| Log Analytics | Minimize data retention |
| Recovery Services | Remove test backups |
| Snapshots | Delete after validation |

---

# Cleanup Strategy

Every laboratory should end with resource cleanup.

Example:

```bash
az group delete \
  --name rg-az104-wk01-core-lab \
  --yes \
  --no-wait
```

Deleting the Resource Group removes every resource contained inside it, provided that no Resource Locks exist.

---

# Cost Tags

| Tag | Purpose |
|-----|---------|
| Owner | Resource owner |
| Project | Project identification |
| Environment | Lab, Dev, Test, Production |
| Week | Study week |
| DeleteAfter | Planned cleanup date |
| CostCenter | Cost allocation |

---

# Common Cost Pitfalls

Always verify that the following resources were removed:

- Orphaned Managed Disks
- Public IP Addresses
- Snapshots
- File Shares
- Backup Vault items
- Log Analytics data
- Storage Accounts

---

# Cost Checklist

Before completing a laboratory:

- [ ] Virtual Machines stopped or removed
- [ ] Managed Disks removed
- [ ] Public IPs removed
- [ ] Snapshots deleted
- [ ] Backup items removed
- [ ] Resource Group deleted
- [ ] Cost Management reviewed
