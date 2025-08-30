# Capítulo 02 – Conceitos

## Objetivo
Explicar os conceitos fundamentais do universo Git e GitHub, preparando o leitor para os capítulos práticos.

---

## Git
- **O que é:** um sistema de **controle de versões distribuído**.  
- **Para que serve:** acompanhar a evolução de arquivos, permitindo voltar a estados anteriores e trabalhar em paralelo sem perder histórico.  
- **Analogia:** como uma máquina do tempo para os arquivos do projeto.  

Exemplo de comando para verificar se o Git está instalado:
```bash
git --version
```

---

## GitHub
- O que é: uma plataforma online que hospeda projetos Git e facilita colaboração.
- Diferença importante:
  - Git → funciona localmente na sua máquina.
  - GitHub → funciona na nuvem, para compartilhar e colaborar.
- Exemplo prático: você pode usar Git sozinho, mas usar GitHub facilita mostrar e compartilhar seu trabalho.

---

## Visual Studio Code (VS Code)
- O que é: um editor de código moderno, gratuito e extensível.
- Por que usar: integração nativa com Git e GitHub, terminal integrado, suporte a extensões úteis.
- Exemplo: acompanhar mudanças no código (ícones de + e -), criar commits sem sair do editor.

---

## GitHub CLI (gh)
- O que é: a ferramenta oficial de linha de comando do GitHub.
- Vantagens: permite criar repositórios, issues, pull requests, releases e acompanhar workflows sem precisar abrir o navegador.
- Exemplo prático:
```bash
gh repo create meu-repo --public
```

---

## GitHub Login Integration (GLI)
- O que é: a integração de login único entre VS Code, Git, GitHub e CLI.
- Benefícios:
  - Menos senhas digitadas.
  - Mais segurança (integração com 2FA).
  - Produtividade (logar uma vez e usar em todos os lugares).

---

## Comparativo rápido

| Ferramenta     | Função principal                         | Onde atua           |
| -------------- | ---------------------------------------- | ------------------- |
| **Git**        | Controle de versões                      | Local (sua máquina) |
| **GitHub**     | Colaboração e hospedagem de repositórios | Nuvem               |
| **VS Code**    | Editor de código com integração GitHub   | Local               |
| **CLI (`gh`)** | Linha de comando para ações no GitHub    | Local ↔ Nuvem       |
| **GLI**        | Login único em todas as ferramentas      | Local ↔ Nuvem       |

---

## Conclusão

Agora que você conhece os principais conceitos, já pode avançar para a configuração do ambiente.
No próximo capítulo, veremos como instalar o VS Code, o Git (com Git Bash) e o GitHub CLI.

✅ **Próximo passo**: avançar para o [Capítulo 03 – Preparando o ambiente](./03-preparando-ambiente.md).
