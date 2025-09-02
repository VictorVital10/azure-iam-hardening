# Testes de Acesso

Neste arquivo, descrevo os testes práticos realizados no projeto Azure IAM Hardening, com foco em validar como os diferentes usuários e roles interagem com os recursos do Azure.

---

## Cenários de Testes

**TESTE 1:** Usuário Analista (Permissão somente para leitura) - verifiquei se o usuário com permissões limitadas conseguia criar novos recursos, atribuir funções e criar novas roles (RBAC).

**RESULTADOS DO TESTE 1:**

![RG Failure](../images/access_test/Failure/RG_Failure.png)

*Imagem 9: um novo grupo de recursos não pode ser criado a partir do usuário Analista.*

---

![VM Falha](../images/access_test/Failure/VM_Failure.png)

*Imagem 10: Falha ao tentar criar uma VM com o usuário Analista.*

---

![RBAC Failure](../images/access_test/Failure/RBAC_Failure.png)

*Imagem 11: usuário Analista não tem as permissões necessárias para atribuir e criar funções para outros usuários.*

---

**TESTE 2:** Usuário Developer (Permissão para criar e alterar recursos) - tentativa de criar recursos, atribuir funções e criar novas roles (RBAC).

**RESULTADOS DO TESTE 2:**

![RBAC Success](../images/access_test/Success/Vm_Success.png)

*Imagem 12: Usuário Dev obteve sucesso ao tentar criar uma Vm.*

---

![RBAC Success](../images/access_test/Success/RBAC_Success.png)

*Imagem 13: Usuário Dev tem as permissões necessárias para atribuir e criar funções para outros usuários.*

---

![RG Success](../images/access_test/Success/RG_Success.png)

*Imagem 14: Novo grupo de recursos criado a partir do Usuário Dev.*

---

### Procedimentos

Para cada teste, realizei os seguintes passos:

- Login no Portal Azure com o usuário do cenário.

- MFA ativo utilizando o Microsoft Authenticator em todas as contas

- Tentativa de realizar ações permitidas e não permitidas.

- Registro dos resultados e mensagens de erro recebidas.

- Comparação com as permissões configuradas via RBAC.

---

### Resultados Observados

Usuário Analista com permissões mínimas encontrou acesso restrito ao tentar criar recursos e RBAC conforme esperado, garantindo que o princípio do privilégio mínimo fosse respeitado.

Usuário Developer com permissões elevadas conseguiu gerenciar roles e recursos sem restrições, permitindo validar a configuração de permissões elevadas.

Os testes ajudaram a identificar potenciais riscos e ajustes necessários na atribuição de roles.

### Aprendizados

Testar cenários práticos é essencial para compreender o impacto do RBAC.

Documentar os resultados ajuda a manter rastreabilidade das permissões e facilita futuros ajustes.