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

## Validação

- Resource Group criado com sucesso pelo Azure Portal.
- Resource Group criado com sucesso pelo Azure CLI.
- Tags aplicadas corretamente.
- Recursos visíveis no Azure Portal.

## Lições aprendidas

- Resource Groups organizam recursos por ciclo de vida.
- Tags ajudam em governança, custo e identificação de ownership.
- Azure CLI permite criar recursos de forma rápida e reproduzível.
- Separar recursos por semana/lab facilita limpeza e controle de custos.

## Comandos utilizados

Os comandos completos estão disponíveis em: [`commands.azcli`](./commands.azcli)

## Limpeza dos recursos
Para evitar custos desnecessários, os recursos criados neste laboratório podem ser removidos com o comando abaixo:

```bash
az group delete \
  --name rg-az104-wk01-core-shell-lab \
  --yes \
  --no-wait
az group delete \
  --name rg-az104-wk01-core-lab \
  --yes \
  --no-wait


