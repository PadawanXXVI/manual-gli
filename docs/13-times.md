# Capítulo 13 – Times

## Objetivo
Explicar como o GitHub organiza a colaboração em **equipes**, com foco em revisões de código, permissões, organizações e autenticação corporativa (SSO).

---

## 1. Trabalhando em grupo
- GitHub facilita dividir tarefas e colaborar.  
- Cada integrante pode criar **branches**, abrir **issues** e contribuir via **pull requests**.  
- Comunicação pode ocorrer diretamente nas issues e PRs, sem depender de mensagens externas.  

📷 *Print sugerido:* tela de uma issue com múltiplos comentários de diferentes usuários.  

---

## 2. Pull Requests com revisores
- Um **Pull Request** pode ter revisores atribuídos.  
- Revisores podem:
  - Comentar no código.
  - Sugerir mudanças específicas.
  - Aprovar ou solicitar ajustes.  

Exemplo de PR pelo CLI já com revisor:
```bash
gh pr create --title "feat: novo recurso" --body "Descrição detalhada" --reviewer usuario1,usuario2
```

📷 *Print sugerido:* PR no GitHub com revisores atribuídos.  

---

## 3. Code review
- **Code review** é a prática de revisar alterações antes de integrá-las à `main`.  
- Benefícios:
  - Garante qualidade do código.
  - Promove aprendizado em equipe.
  - Evita erros em produção.  

Tipos de feedback no GitHub:
- **Comment** → comentário simples.  
- **Suggestion** → sugestão direta de código.  
- **Approve** → aprovado.  
- **Request changes** → mudanças necessárias.  

📷 *Print sugerido:* tela de PR com revisão mostrando comentários e sugestões de código.  

---

## 4. Organizações no GitHub
- **Organizações** permitem centralizar projetos de uma empresa, equipe ou turma.  
- É possível:
  - Criar **times** dentro da organização.  
  - Definir permissões diferentes para cada membro (leitura, escrita, admin).  
  - Centralizar múltiplos repositórios sob a mesma entidade.  

📷 *Print sugerido:* tela de uma organização no GitHub com lista de times.  

---

## 5. SSO / SAML em ambientes corporativos
- Algumas empresas usam **Single Sign-On (SSO)** para autenticação.  
- O GitHub integra com sistemas corporativos via **SAML**.  
- Benefícios:
  - Maior segurança.
  - Login único em múltiplos sistemas.
  - Controle centralizado de acessos.  

📷 *Print sugerido:* tela do GitHub pedindo login via SSO corporativo.  

---

## Conclusão
Colaborar em **times** no GitHub é muito mais do que compartilhar código: envolve revisar, aprender em conjunto e manter padrões de qualidade.  
Agora que você entende esse processo, no próximo capítulo vamos abordar como resolver problemas comuns com o **Troubleshooting**.  

---

✅ **Próximo passo**: avançar para o [Capítulo 14 – Troubleshooting](./14-troubleshooting.md).
