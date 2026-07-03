# AZ-104 Lab 01 — Resource Group e Tags

## Objetivo
Criar um Resource Group no Azure usando Portal e Azure CLI, aplicando tags para organização e controle de custos.

## Recursos criados
- Resource Group: rg-az104-wk01-core-lab
- Resource Group via CLI: rg-az104-wk01-core-shell-lab
- Região: East US

## Tags aplicadas
- Owner: Thiago
- Purpose: AZ-104 Study
- Environment: Lab
- Week: 01
- DeleteAfter: 2026-10-31
- CostCenter: Study

## Comando utilizado
```bash
az group create \
  --name rg-az104-wk01-core-shell-lab \
  --location eastus \
  --tags Owner=Thiago Purpose='AZ-104 Study' Environment=Lab Week=01 DeleteAfter=2026-10-31 CostCenter=Study
