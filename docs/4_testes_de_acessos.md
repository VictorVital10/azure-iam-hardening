# Testes de Acesso

Neste arquivo, descrevo os testes práticos realizados no projeto Azure IAM Hardening, com foco em validar como os diferentes usuários e roles interagem com os recursos do Azure.

---

### Cenários de Teste

Para entender melhor o comportamento do RBAC e o impacto do privilégio mínimo, criei alguns cenários de teste:

Usuário Dev tentando criar recursos: verifiquei se o usuário com permissões limitadas conseguia criar VMs ou modificar recursos fora do Resource Group permitido.

Usuário Admin-Teste gerenciando permissões: testei se o usuário com permissões elevadas conseguia atribuir roles e alterar configurações críticas.

Usuário Reader tentando acessar recursos restritos: validei que contas com apenas permissão de leitura não conseguiam modificar nada.

---

### Procedimentos

Para cada teste, realizei os seguintes passos:

Login no Portal Azure com o usuário do cenário.

Tentativa de realizar ações permitidas e não permitidas.

Registro dos resultados e mensagens de erro recebidas.

Comparação com as permissões configuradas via RBAC.

---

### Resultados Observados

Usuários com permissões mínimas tiveram acesso restrito conforme esperado, garantindo que o princípio do privilégio mínimo fosse respeitado.

Usuário Admin-Teste conseguiu gerenciar roles e recursos sem restrições, permitindo validar a configuração de permissões elevadas.

Testes ajudaram a identificar potenciais riscos e ajustes necessários na atribuição de roles.

### Aprendizados

Testar cenários práticos é essencial para compreender o impacto do RBAC.

Documentar os resultados ajuda a manter rastreabilidade das permissões e facilita futuras auditorias ou ajustes.