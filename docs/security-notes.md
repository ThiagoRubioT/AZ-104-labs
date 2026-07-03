```markdown
# Notas de Segurança

Este documento descreve as práticas de segurança aplicadas nos laboratórios da certificação AZ-104.

## Objetivo

O objetivo é executar laboratórios Azure de forma segura, evitando exposição de dados sensíveis e aplicando boas práticas básicas de Cloud Security.

## Informações sensíveis que não devem ser publicadas

As seguintes informações não devem ser publicadas neste repositório:

- Subscription ID.
- Tenant ID.
- Client ID.
- Client Secret.
- Access Keys.
- SAS Tokens.
- Senhas.
- Chaves privadas.
- E-mails pessoais ou corporativos sensíveis.
- IPs públicos usados para acesso pessoal.
- Dados reais de empresas.
- Nomes internos de ambientes corporativos.
- Informações de clientes ou terceiros.

## Cuidados com screenshots

Antes de publicar prints no GitHub, validar se não aparecem informações sensíveis.

Itens que devem ser ocultados ou removidos:

- Subscription ID.
- Tenant ID.
- Nome completo da assinatura, se for sensível.
- E-mail ou UPN da conta.
- Access keys.
- SAS URLs.
- Tokens.
- Secrets.
- IPs públicos sensíveis.
- Dados de empresa real.

## Práticas de controle de acesso

- Utilizar Azure RBAC para controle de permissões.
- Atribuir permissões a grupos sempre que possível.
- Aplicar o princípio do menor privilégio.
- Evitar uso desnecessário da role Owner.
- Preferir roles específicas, como Reader, Contributor, Network Contributor ou Storage Blob Data Reader.
- Remover permissões temporárias após os testes.
- Evitar atribuições diretas para usuários quando grupos puderem ser utilizados.

## Práticas de segurança para Storage

- Bloquear acesso público anônimo, salvo quando o laboratório exigir o contrário.
- Exigir HTTPS.
- Utilizar TLS 1.2 ou superior.
- Evitar exposição de access keys.
- Preferir autenticação com Microsoft Entra ID quando possível.
- Gerar SAS tokens com escopo limitado.
- Utilizar SAS tokens com expiração curta.
- Evitar SAS com permissões amplas, como escrita ou exclusão, sem necessidade.

## Práticas de segurança para rede

- Evitar IP público quando não for necessário.
- Utilizar NSGs para controlar tráfego de entrada e saída.
- Restringir portas administrativas, como RDP e SSH.
- Preferir Azure Bastion ou acesso privado quando aplicável.
- Utilizar Private Endpoints para serviços sensíveis quando o cenário exigir.
- Validar regras efetivas de segurança durante troubleshooting.

## Práticas de identidade

- Utilizar MFA sempre que possível.
- Evitar uso de contas administrativas para tarefas do dia a dia.
- Criar usuários e grupos de laboratório separados.
- Utilizar grupos para atribuições RBAC.
- Revisar usuários convidados.
- Remover contas de teste ao final dos laboratórios, quando não forem mais necessárias.

## Práticas de limpeza segura

Após cada laboratório:

- Remover recursos que não serão reutilizados.
- Remover permissões temporárias.
- Remover SAS tokens ou garantir que tenham expiração curta.
- Excluir Resource Groups de laboratório.
- Verificar se não ficaram discos, IPs públicos, snapshots ou backups órfãos.

## Aviso

Este repositório tem finalidade educacional e de portfólio.

Os laboratórios são executados em ambiente pessoal de estudos e não contêm dados de produção, informações corporativas reais ou credenciais sensíveis.
