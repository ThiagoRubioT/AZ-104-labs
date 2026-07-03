# Controle de Custos

Este documento descreve as práticas de controle de custos utilizadas nos laboratórios da certificação AZ-104.

## Objetivo

O objetivo é praticar administração Azure evitando cobranças desnecessárias durante os estudos.

## Práticas adotadas

- Utilizar uma assinatura Azure dedicada para estudos.
- Criar Resource Groups separados por semana ou laboratório.
- Aplicar tags nos recursos sempre que possível.
- Configurar Budget na assinatura.
- Usar SKUs de baixo custo nos laboratórios.
- Evitar deixar máquinas virtuais ligadas sem necessidade.
- Evitar recursos caros quando não forem necessários.
- Excluir recursos após a conclusão dos labs.
- Revisar o Azure Cost Management com frequência.

## Budget recomendado

Para ambiente de laboratório, recomenda-se criar um budget mensal baixo.

Exemplo:
Budget mensal: R$ 50 a R$ 100
Alertas: 50%, 80% e 100%
O objetivo do budget é gerar alertas e visibilidade sobre o consumo. Ele não deve ser tratado como substituto para limpeza dos recursos.

## Boas práticas por tipo de recurso
| Recurso            | Prática de custo                                         |
| ------------------ | -------------------------------------------------------- |
| Resource Groups    | Não geram custo direto                                   |
| Storage Accounts   | Usar Standard LRS e poucos arquivos                      |
| Virtual Machines   | Usar tamanhos pequenos e desligar/remover após o lab     |
| Public IPs         | Evitar quando não forem necessários                      |
| Azure Bastion      | Usar apenas em labs específicos e remover depois         |
| Log Analytics      | Controlar retenção e volume de ingestão                  |
| Backup             | Usar apenas nos labs necessários e limpar após validação |
| Snapshots          | Remover após os testes                                   |
| Discos gerenciados | Verificar se discos órfãos foram removidos               |

## Estratégia de limpeza
Cada laboratório deve conter comandos de limpeza para remover os recursos criados.
Exemplo: 
az group delete \
  --name rg-az104-wk01-core-lab \
  --yes \
  --no-wait
A exclusão do Resource Group remove todos os recursos contidos nele, desde que não existam locks impedindo a exclusão.

## Tags relacionadas a custo
| Tag           | Finalidade                                |
| ------------- | ----------------------------------------- |
| `Owner`       | Identifica o responsável pelo recurso     |
| `Project`     | Identifica o projeto de estudo            |
| `Environment` | Indica se é Lab, Dev, Prod etc.           |
| `Week`        | Identifica a semana do estudo             |
| `DeleteAfter` | Indica quando o recurso deve ser removido |
| `CostCenter`  | Apoia organização e análise de custos     |

## Recursos que podem gerar custo mesmo após testes

Alguns recursos podem continuar gerando custo se não forem limpos corretamente.
Exemplos:
 - Discos gerenciados órfãos após exclusão de VMs.
 - Public IPs não utilizados.
 - Snapshots antigos.
 - File shares excluídos com soft delete habilitado.
 - Itens protegidos por backup.
 - Dados retidos no Log Analytics.
 - Storage Accounts com dados, versões ou snapshots.

## Checklist de custo

Antes de finalizar um laboratório, validar:
 [ ] As VMs foram desligadas ou removidas.
 [ ] Os discos órfãos foram removidos.
 [ ] Os Public IPs não utilizados foram removidos.
 [ ] Os snapshots temporários foram apagados.
 [ ] Os backups de teste foram removidos, quando aplicável.
 [ ] O Resource Group do lab foi excluído, se não for mais necessário.
 [ ] O Cost Management foi revisado.


