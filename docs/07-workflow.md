# Capítulo 07 – Workflow (ciclo Git)

## Objetivo
Explicar o fluxo de trabalho básico com Git e GitHub, mostrando como as mudanças passam do computador do usuário até o repositório remoto.  

---

## 1. O que é um commit?
- Um **commit** é como uma "foto" do estado dos arquivos em determinado momento.  
- Serve para registrar alterações de forma organizada.  
- Boas práticas:
  - Mensagens curtas e objetivas.
  - Usar verbos no **imperativo** (ex.: `docs: adicionar capítulo 07`).  

Exemplo:
```bash
git add arquivo.md
git commit -m "docs: adicionar capítulo 07 - workflow"
```

📷 *Print sugerido:* VS Code mostrando arquivos modificados e o campo para mensagem de commit.  

---

## 2. Trabalhando com branches
- Uma **branch** é uma linha paralela de desenvolvimento.  
- Permite trabalhar em novas funcionalidades sem alterar a branch principal (`main`).  

Criando uma branch:
```bash
git checkout -b minha-branch
```

Trocando de branch:
```bash
git checkout main
```

📷 *Print sugerido:* lista de branches no VS Code (GitLens ou menu de branch).  

---

## 3. Push (enviando alterações)
Após criar commits, você envia as mudanças para o GitHub com `push`.  

```bash
git push origin minha-branch
```

📷 *Print sugerido:* terminal Git Bash mostrando `git push` concluído com sucesso.  

---

## 4. Pull Request (PR)
- Um **PR (Pull Request)** é um pedido para mesclar suas alterações em outra branch (geralmente `main`).  
- É usado para revisão e colaboração.  

Criando PR pelo GitHub CLI:
```bash
gh pr create --title "docs: adicionar capítulo 07" --body "Primeira versão do workflow"
```

📷 *Print sugerido:* tela do GitHub Web mostrando a página de criação de PR.  

---

## 5. Merge
Após a revisão, as alterações são unificadas (merge).  
No GitHub, pode ser feito clicando no botão **Merge pull request**.  

Tipos comuns de merge:
- **Merge commit**: junta o histórico inteiro.  
- **Squash**: condensa todos os commits em um só.  
- **Rebase**: reorganiza o histórico de forma linear.  

📷 *Print sugerido:* tela do GitHub com PR aprovado e pronto para merge.  

---

## 6. Fluxo resumido
1. Criar branch.  
2. Fazer commits.  
3. `push` para o GitHub.  
4. Abrir PR.  
5. Revisar e aprovar.  
6. Merge para `main`.  

📷 *Print sugerido:* fluxograma simples mostrando fluxo → branch → commit → push → PR → merge.  

---

## Conclusão
O ciclo Git ajuda a organizar o trabalho de forma colaborativa e segura.  
Agora que você já entende o fluxo básico, no próximo capítulo vamos aprender a **colaborar no GitHub** usando issues, labels, milestones e projects.  

---

✅ **Próximo passo**: avançar para o [Capítulo 08 – Colaboração](./08-colaboracao.md).
