```markdown
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

```text
Budget mensal: R$ 50 a R$ 100
Alertas: 50%, 80% e 100%
