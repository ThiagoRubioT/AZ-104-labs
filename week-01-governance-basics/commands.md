# Azure CLI Commands - Week 01

This document contains all Azure CLI commands used during the Week 01 laboratory.

---

# Resource Groups

## Create Resource Group

```bash
az group create \
  --name rg-az104-wk01-shell-lab \
  --location eastus \
  --tags \
      Owner=Thiago \
      Purpose="AZ-104 Study" \
      Environment=Study \
      Week=01 \
      DeleteAfter=2026-10-31 \
      CostCenter=Study
```

---

## Show Resource Group

```bash
az group show \
    --name rg-az104-wk01-shell-lab \
    --output table
```

---

## List Resource Groups

```bash
az group list \
    --output table
```

---

# RBAC

## Get Resource Group ID

```bash
RG_ID=$(az group show \
    --name rg-az104-wk01-shell-lab \
    --query id \
    -o tsv)
```

---

## Create Reader Assignment

```bash
az role assignment create \
    --assignee developer@thiagorubio.com.br \
    --role Reader \
    --scope $RG_ID
```

---

## List Role Assignments

```bash
az role assignment list \
    --scope $RG_ID \
    --output table
```

---

# Resource Locks

## Create CanNotDelete Lock

```bash
az lock create \
    --name lock-rg-az104-wk01-shell-cannotdelete \
    --resource-group rg-az104-wk01-shell-lab \
    --lock-type CanNotDelete
```

---

## List Locks

```bash
az lock list \
    --query "[?level=='CanNotDelete'].{LockName:name,ResourceGroup:resourceGroup}" \
    --output table
```

---

## Delete Lock

```bash
az lock delete \
    --name lock-rg-az104-wk01-shell-cannotdelete \
    --resource-group rg-az104-wk01-shell-lab
```

---

# Cost Management

## Azure Budget

Attempted using Azure CLI:

```bash
az consumption budget create \
    --budget-name "budget-az104-lab-monthly" \
    --category "cost" \
    --amount 20 \
    -s 2026-03-07 \
    -e 2026-10-31 \
    --time-grain Monthly
```

Result:

```
Invalid budget configuration,
please use filter interface with 2019-05-01-preview version.
```

The budget was created using the Azure Portal instead.

---

# Cleanup

## Delete Resource Group

```bash
az group delete \
    --name rg-az104-wk01-shell-lab \
    --yes \
    --no-wait
```

---

## Delete Resource Group (Core Lab)

```bash
az group delete \
    --name rg-az104-wk01-core-lab \
    --yes \
    --no-wait
```

---

# Notes

- Azure Cloud Shell was used during all exercises.
- Authentication performed using Microsoft Entra ID.
- Resource Groups were created in East US.
- A custom domain (thiagorubio.com.br) was used for user accounts.
