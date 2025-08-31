# Capítulo 08 – Colaboração

## Objetivo
Explicar como o GitHub organiza a colaboração em projetos, usando **issues**, **labels**, **milestones** e **projects (v2)** para planejar e acompanhar o progresso.

---

## 1. Issues
- **O que são:** registros de tarefas, bugs, ideias ou melhorias.  
- Servem como **to-do list** do projeto.  
- Podem ser criadas pelo site ou pelo GitHub CLI.  

Exemplo CLI:
```bash
gh issue create --title "Escrever capítulo 08 - Colaboração" --body "Incluir conteúdo sobre issues, labels e milestones."
```

📷 *Print sugerido:* tela de criação de uma issue no GitHub Web.  

---

## 2. Labels
- **O que são:** etiquetas visuais que ajudam a classificar issues.  
- Exemplos neste manual:
  - `docs` → capítulos do manual.  
  - `revisão` → aguardando revisão.  
  - `print-pendente` → precisa incluir prints.  

Exemplo CLI:
```bash
gh label create "docs" --description "Documentação" --color 0366d6
```

📷 *Print sugerido:* lista de labels aplicadas em uma issue.  

---

## 3. Milestones
- **O que são:** agrupamentos de issues que representam entregas maiores (ex.: versão do manual).  
- No manual, usamos `v1.0 – Primeira edição completa`.  

📷 *Print sugerido:* tela de milestone no GitHub mostrando progresso (% concluído).  

---

## 4. Projects (v2)
- **O que são:** quadros estilo Kanban para organizar issues e PRs.  
- Colunas típicas: **Backlog → Em Progresso → Concluído**.  
- Permitem visualizar rapidamente o andamento do projeto.  

Exemplo CLI (adicionar issue a um project):
```bash
ISSUE_URL=$(gh issue view 1 --json url --jq .url)
gh project item-add 1 --url "$ISSUE_URL" --owner usuario
```

📷 *Print sugerido:* quadro Project v2 mostrando issues em diferentes colunas.  

---

## 5. Fluxo recomendado neste manual
1. Criar milestone (`v1.0`).  
2. Abrir issues para cada capítulo.  
3. Aplicar labels adequadas (`docs`, `print-pendente`, etc.).  
4. Acompanhar andamento no Project.  

---

## Conclusão
Usando **issues, labels, milestones e projects**, você consegue transformar qualquer trabalho — até mesmo a escrita de um manual — em um processo bem organizado.  

---

✅ **Próximo passo**: avançar para o [Capítulo 09 – GitHub CLI](./09-gh-cli.md).
