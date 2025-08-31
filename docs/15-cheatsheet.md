# Capítulo 15 – Cheat-Sheet

## Objetivo
Oferecer uma referência rápida com os principais comandos do **Git** e do **GitHub CLI (`gh`)**, além de links úteis para aprofundar os estudos.

---

## 1. Comandos básicos do Git

| Ação                  | Comando                          |
|-----------------------|----------------------------------|
| Inicializar repositório | `git init`                     |
| Clonar repositório    | `git clone URL`                  |
| Ver status            | `git status`                     |
| Adicionar arquivos    | `git add .`                      |
| Criar commit          | `git commit -m "mensagem"`       |
| Ver branches          | `git branch`                     |
| Criar nova branch     | `git checkout -b nome-branch`    |
| Trocar de branch      | `git checkout nome-branch`       |
| Enviar alterações     | `git push origin nome-branch`    |
| Atualizar local       | `git pull`                       |

---

## 2. Comandos básicos do GitHub CLI (`gh`)

| Ação                  | Comando                                      |
|-----------------------|----------------------------------------------|
| Criar repositório     | `gh repo create`                             |
| Clonar repositório    | `gh repo clone usuario/repo`                 |
| Ver detalhes repo     | `gh repo view usuario/repo`                  |
| Criar issue           | `gh issue create --title --body`             |
| Listar issues         | `gh issue list`                              |
| Ver issue             | `gh issue view 1`                            |
| Criar PR              | `gh pr create --title --body`                |
| Listar PRs            | `gh pr list`                                 |
| Ver PR                | `gh pr view 1`                               |
| Criar release         | `gh release create v1.0 --notes "descrição"` |
| Ver workflows         | `gh run list`                                |

---

## 3. Links úteis
- 📖 [Documentação oficial do Git](https://git-scm.com/doc)  
- 🐙 [Documentação oficial do GitHub](https://docs.github.com)  
- 💻 [Manual do GitHub CLI](https://cli.github.com/manual)  
- ✍️ [Guia de Markdown](https://www.markdownguide.org/)  

---

## Conclusão
Este capítulo funciona como um **resumo de bolso**: sempre que esquecer um comando, volte aqui e consulte.  
No próximo capítulo, vamos encerrar o manual com uma conclusão e próximos passos.  

---

✅ **Próximo passo**: avançar para o [Capítulo 16 – Conclusão](./16-conclusao.md).
