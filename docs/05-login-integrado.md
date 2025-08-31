# Capítulo 05 – Login integrado (GLI)

## Objetivo
Configurar o **GitHub Login Integration (GLI)**, garantindo que Git, VS Code e GitHub CLI funcionem juntos sem precisar digitar senha a cada comando.

---

## 1. Configurando usuário no Git
Antes de tudo, configure seu nome e email no Git (esses dados aparecerão nos commits).

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```

Para verificar:
```bash
git config --list
```

📷 *Print sugerido:* tela do Git Bash mostrando a saída de `git config --list` com nome e email configurados.  

---

## 2. Autenticando no GitHub CLI (`gh`)
O `gh` facilita o login sem precisar criar manualmente tokens.

1. Rode o comando:
```bash
gh auth login
```
2. Escolha:
   - **GitHub.com**
   - **HTTPS**
   - **Login via navegador**
3. Confirme no navegador e volte ao terminal.

Para checar:
```bash
gh auth status
```

📷 *Print sugerido:* saída do comando `gh auth login` pedindo escolha do método de login.  
📷 *Print sugerido:* saída de `gh auth status` mostrando que está autenticado.  

---

## 3. Configurando credenciais no Git (Credential Manager)
Se o Git pedir usuário/senha a cada `push`, configure o **credential manager**:

```bash
git config --global credential.helper manager-core
```

📷 *Print sugerido:* tela do Windows Credential Manager mostrando credenciais salvas para GitHub.  

---

## 4. Integração com VS Code
O VS Code reconhece automaticamente sua autenticação via GLI.

- Abra o **Command Palette** (`Ctrl+Shift+P`).  
- Procure por **“GitHub: Sign in”**.  
- Clique e confirme o login pelo navegador.  

📷 *Print sugerido:* tela do VS Code mostrando o pop-up de login no GitHub.  

---

## 5. Testando tudo
1. Crie uma pasta de teste e entre nela:
```bash
mkdir projeto-teste
cd projeto-teste
```

2. Inicie o Git:
```bash
git init
```

3. Crie um repositório no GitHub direto pelo `gh`:
```bash
gh repo create projeto-teste --public --source=. --remote=origin --push
```

4. Verifique se o repositório foi criado online e sincronizado.

📷 *Print sugerido:* terminal mostrando a criação do repositório via `gh`.  
📷 *Print sugerido:* página do repositório recém-criado no GitHub.  

---

## Conclusão
Agora você já tem o login integrado funcionando no **Git**, **GitHub CLI** e **VS Code**.  
Isso garante que todos os próximos capítulos fluam sem bloqueios de autenticação.  

---

✅ **Próximo passo**: avançar para o [Capítulo 06 – Repositórios](./06-repositorios.md).
