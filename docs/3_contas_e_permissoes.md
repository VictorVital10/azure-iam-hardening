# Contas e Permissões

Neste arquivo, descrevo a configuração de usuários, grupos e permissões no projeto Azure IAM Hardening, com foco em entender na prática como o controle de acesso funciona dentro da Azure.

---
 
### Criação de Usuários

Criei usuários específicos para testes de permissões, simulando diferentes papéis dentro de um ambiente corporativo.

Usuário Admin-Teste: conta com permissões elevadas para administração do ambiente.

Usuário Dev: conta com permissões limitadas para desenvolvimento e testes controlados.

Outros usuários de suporte ou teste, conforme necessário para os cenários.

---

### Grupos de Usuários

Organizei os usuários em grupos para facilitar a aplicação de políticas de acesso e seguir boas práticas de RBAC.

Exemplo de grupos:

* Grupo-Admins – usuários com permissões de administrador.

* Grupo-Dev – usuários com permissões restritas ao Resource Group de testes.

---

### Atribuição de Roles (RBAC)

Atribuí roles específicas a cada usuário ou grupo, aplicando o princípio do mínimo privilégio:

* Owner – acesso total em Resource Groups selecionados.

* Contributor – criação e gerenciamento de recursos sem permissões administrativas completas.

* Reader – apenas visualização de recursos, sem alterações.

Essa etapa foi essencial para testar e compreender como diferentes papéis impactam o acesso a recursos e operações na Azure.

---

### Observações Práticas

Durante a configuração, percebi alguns pontos importantes:

A separação de grupos facilita a aplicação de políticas consistentes e evita atribuições excessivas de permissões.

Testar diferentes combinações de usuários e roles ajuda a internalizar como o RBAC funciona no dia a dia.

---