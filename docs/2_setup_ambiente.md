# Configuração do ambiente Azure.

Neste arquivo, descrevo como configurei o ambiente do projeto Azure IAM Hardening, preparando tudo para realizar testes práticos de identidade e controle de acesso na Azure.

---

### Assinatura e Tenant

Para iniciar, utilizei uma assinatura Azure válida e configurei o tenant principal para o projeto. Essa etapa foi essencial para garantir que todos os recursos fossem criados dentro de um ambiente controlado, permitindo aplicar e testar permissões sem impactar outros ambientes.

Tipo de assinatura utilizada: (ex: Pay-As-You-Go)

Tenant configurado: (nome do tenant ou ID, se quiser incluir)

---

### Resource Groups

Criei Resource Groups específicos para organizar os recursos do projeto e facilitar a aplicação de políticas de acesso.

Exemplo de Resource Groups:

RG-Teste – utilizado para testes práticos de IAM.

RG-Dev – simulação de ambiente de desenvolvimento.

Essa organização ajuda a entender melhor como o RBAC se aplica a diferentes contextos dentro da Azure.

---

### Ferramentas Utilizadas

Para gerenciar e realizar os testes no ambiente, utilizei principalmente:

Portal Azure – para criação e configuração de recursos.

Microsoft Entra ID – para gerenciamento de usuários, grupos e roles.

(Outras ferramentas que você possa ter usado, como CLI ou PowerShell)

---
