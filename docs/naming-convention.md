# Convenção de Nomes

Este documento descreve o padrão de nomenclatura utilizado nos laboratórios da certificação AZ-104.

## Objetivo

O objetivo da convenção de nomes é manter os recursos do Azure organizados, fáceis de identificar e simples de remover após cada laboratório.

## Padrão geral

<tipo-do-recurso>-az104-wk<numero-da-semana>-<finalidade>-lab

## Exemplos

| Recurso                 | Exemplo                  |
| ----------------------- | ------------------------ |
| Resource Group          | `rg-az104-wk01-core-lab` |
| Storage Account         | `staz104wk04lab001`      |
| Virtual Network         | `vnet-az104-wk09-lab`    |
| Subnet                  | `snet-az104-wk09-app`    |
| Network Security Group  | `nsg-az104-wk10-web`     |
| Route Table             | `rt-az104-wk10-lab`      |
| Public IP               | `pip-az104-wk07-win01`   |
| Network Interface       | `nic-az104-wk07-win01`   |
| Virtual Machine         | `vm-az104-wk07-win01`    |
| Managed Disk            | `disk-az104-wk07-data01` |
| Log Analytics Workspace | `law-az104-wk12-lab`     |
| Recovery Services Vault | `rsv-az104-wk13-lab`     |

## Prefixos utilizados

| Prefixo | Tipo de recurso         |
| ------- | ----------------------- |
| `rg`    | Resource Group          |
| `st`    | Storage Account         |
| `vnet`  | Virtual Network         |
| `snet`  | Subnet                  |
| `nsg`   | Network Security Group  |
| `rt`    | Route Table             |
| `pip`   | Public IP               |
| `nic`   | Network Interface       |
| `vm`    | Virtual Machine         |
| `disk`  | Managed Disk            |
| `law`   | Log Analytics Workspace |
| `rsv`   | Recovery Services Vault |
| `kv`    | Key Vault               |

## Tags utilizadas

| Tag           | Exemplo      |
| ------------- | ------------ |
| `Owner`       | `Thiago`     |
| `Project`     | `AZ-104`     |
| `Environment` | `Lab`        |
| `Week`        | `01`         |
| `Purpose`     | `Study`      |
| `CostCenter`  | `Study`      |
| `DeleteAfter` | `2026-10-31` |

## Observações

Storage Accounts possuem regras específicas de nomenclatura:
- Devem ter nome globalmente único.
- Devem conter apenas letras minúsculas e números.
- Não podem conter hífen.
- Devem ter entre 3 e 24 caracteres.

Exemplo válido:
`staz104wk04lab001`
