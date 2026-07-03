# AZ-104 Labs — Microsoft Azure Administrator

Este repositório documenta minha jornada prática de estudos para a certificação **AZ-104: Microsoft Azure Administrator**.

O objetivo é consolidar conhecimentos de administração Azure por meio de laboratórios hands-on, simulando atividades reais de um administrador de nuvem, como criação de recursos, governança, RBAC, redes, armazenamento, máquinas virtuais, monitoramento, backup e automação.

## Objetivo

Criar um portfólio técnico com laboratórios práticos de Azure, demonstrando capacidade de:

- Administrar recursos no Microsoft Azure.
- Organizar ambientes com Resource Groups, tags e naming convention.
- Aplicar boas práticas de governança e controle de custos.
- Configurar Azure RBAC e permissões por escopo.
- Implementar Storage Accounts, Blob Storage e Azure Files.
- Criar e gerenciar Virtual Machines.
- Configurar VNets, subnets, NSGs, route tables e private access.
- Implementar monitoramento com Azure Monitor e Log Analytics.
- Automatizar recursos com Azure CLI, PowerShell, ARM e Bicep.
- Documentar validação, troubleshooting e limpeza de recursos.

## Contexto

Tenho experiência em infraestrutura, Active Directory, GPO, DNS, DHCP, VMware, SCCM, Windows Server, segurança e IAM.  
Este repositório faz parte da minha transição e aprofundamento em **Azure Administration, Cloud Security, Microsoft Entra ID e Azure Security Engineering**.

## Tecnologias e ferramentas utilizadas

- Microsoft Azure
- Microsoft Entra ID
- Azure Resource Manager
- Azure CLI
- Azure PowerShell
- Bicep
- Azure Portal
- Azure Storage
- Azure Virtual Machines
- Azure Virtual Network
- Azure Monitor
- Log Analytics
- Recovery Services Vault
- GitHub

## Estrutura do repositório

```text
AZ104-Labs/
├── README.md
├── week-01-governance-basics/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-02-entra-id-rbac/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-03-rbac-policy-governance/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-04-storage-accounts/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-05-blob-files-lifecycle/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-06-arm-bicep-automation/
│   ├── README.md
│   ├── commands.azcli
│   ├── templates/
│   └── screenshots/
├── week-07-virtual-machines/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-08-scale-app-containers/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-09-vnet-subnets-dns/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-10-nsg-routes-peering/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-11-bastion-private-endpoints-lb/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-12-monitor-log-analytics-alerts/
│   ├── README.md
│   ├── queries.kql
│   ├── commands.azcli
│   └── screenshots/
├── week-13-backup-recovery/
│   ├── README.md
│   ├── commands.azcli
│   └── screenshots/
├── week-14-final-project/
│   ├── README.md
│   ├── architecture.md
│   ├── commands.azcli
│   └── screenshots/
├── week-15-exam-review/
│   ├── README.md
│   ├── wrong-questions.md
│   └── notes.md
└── docs/
    ├── study-notes.md
    ├── naming-convention.md
    ├── cost-control.md
    └── security-notes.md
