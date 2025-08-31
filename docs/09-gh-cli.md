# Capítulo 09 – GitHub CLI (gh)

## Objetivo
Apresentar o **GitHub CLI (`gh`)**, a ferramenta oficial de linha de comando que permite interagir com o GitHub sem precisar abrir o navegador.

---

## 1. O que é o GitHub CLI
- Ferramenta oficial, mantida pelo GitHub.  
- Permite criar e gerenciar repositórios, issues, pull requests, releases e workflows diretamente do terminal.  
- Ajuda a ganhar produtividade e integrar automações.  

📷 *Print sugerido:* tela do terminal Git Bash mostrando `gh --version`.  

---

## 2. Comandos básicos para repositórios
- Criar novo repositório:
```bash
gh repo create nome-repo --public
```

- Clonar repositório:
```bash
gh repo clone usuario/nome-repo
```

- Ver informações de um repositório:
```bash
gh repo view usuario/nome-repo
```

📷 *Print sugerido:* saída de `gh repo view` mostrando descrição do repositório.  

---

## 3. Comandos para issues
- Criar uma issue:
```bash
gh issue create --title "Título da issue" --body "Descrição detalhada"
```

- Listar issues abertas:
```bash
gh issue list
```

- Visualizar detalhes de uma issue:
```bash
gh issue view 1
```

📷 *Print sugerido:* saída de `gh issue list` mostrando issues abertas.  

---

## 4. Comandos para pull requests
- Criar PR:
```bash
gh pr create --title "feat: novo capítulo" --body "Descrição da mudança"
```

- Listar PRs:
```bash
gh pr list
```

- Visualizar um PR específico:
```bash
gh pr view 5
```

📷 *Print sugerido:* saída de `gh pr view` mostrando detalhes do PR.  

---

## 5. Comandos para releases
- Criar uma release:
```bash
gh release create v1.0 --notes "Primeira versão completa"
```

- Listar releases:
```bash
gh release list
```

📷 *Print sugerido:* tela do GitHub Web mostrando a release criada.  

---

## 6. Comandos para Actions (workflows)
- Ver status dos últimos workflows executados:
```bash
gh run list
```

📷 *Print sugerido:* saída de `gh run list` listando execuções de Actions.  

---

## Conclusão
O **GitHub CLI** amplia a produtividade no uso do GitHub, evitando a dependência da interface web.  
No próximo capítulo, veremos como **automatizar tarefas repetitivas** usando aliases, extensões e scripts.

---

✅ **Próximo passo**: avançar para o [Capítulo 10 – Automação](./10-automacao.md).
