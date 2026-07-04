# Azure Naming Conventions

This document describes the naming standards adopted throughout this repository.

The goal is to keep Azure resources organized, consistent and easy to identify across all laboratory environments.

---

# General Naming Pattern

```
<resource-type>-az104-wk<week-number>-<purpose>-lab
```

Example:

```
rg-az104-wk01-core-lab
```

---

# Resource Naming Examples

| Azure Resource | Example |
|----------------|---------|
| Resource Group | `rg-az104-wk01-core-lab` |
| Storage Account | `staz104wk04lab001` |
| Virtual Network | `vnet-az104-wk09-lab` |
| Subnet | `snet-az104-wk09-app` |
| Network Security Group | `nsg-az104-wk10-web` |
| Route Table | `rt-az104-wk10-lab` |
| Public IP | `pip-az104-wk07-win01` |
| Network Interface | `nic-az104-wk07-win01` |
| Virtual Machine | `vm-az104-wk07-win01` |
| Managed Disk | `disk-az104-wk07-data01` |
| Log Analytics Workspace | `law-az104-wk12-lab` |
| Recovery Services Vault | `rsv-az104-wk13-lab` |
| Key Vault | `kv-az104-wk11-lab` |

---

# Resource Prefixes

| Prefix | Resource |
|---------|----------|
| rg | Resource Group |
| st | Storage Account |
| vnet | Virtual Network |
| snet | Subnet |
| nsg | Network Security Group |
| rt | Route Table |
| pip | Public IP |
| nic | Network Interface |
| vm | Virtual Machine |
| disk | Managed Disk |
| law | Log Analytics Workspace |
| rsv | Recovery Services Vault |
| kv | Key Vault |

---

# Standard Tags

| Tag | Example |
|-----|---------|
| Owner | Thiago |
| Project | AZ-104 |
| Environment | Lab |
| Week | 01 |
| Purpose | Study |
| CostCenter | Study |
| DeleteAfter | 2026-10-31 |

---

# Storage Account Naming Rules

Storage Accounts have specific Azure naming requirements:

- Globally unique
- Lowercase letters and numbers only
- No hyphens
- Between 3 and 24 characters

Example:

```
staz104wk04lab001
```
