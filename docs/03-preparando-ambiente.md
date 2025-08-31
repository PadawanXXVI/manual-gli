# Capítulo 03 – Preparando o ambiente

## Objetivo
Ensinar como instalar e configurar o ambiente necessário para seguir o manual:  
- **Visual Studio Code (VS Code)**  
- **Git** (com **Git Bash**)  
- **GitHub CLI (`gh`)**

---

## 1. Instalando o VS Code
- Acesse: <https://code.visualstudio.com/>  
- Baixe a versão para **Windows** e siga o instalador.  
- Durante a instalação, marque a opção **“Add to PATH”** para permitir abrir o VS Code pelo terminal.  

✅ Após instalado, abra o VS Code para verificar se está funcionando.  

📷 *Print sugerido:* tela do instalador do VS Code com a opção **Add to PATH** marcada.  

---

## 2. Instalando o Git (com Git Bash)
- Acesse: <https://git-scm.com/downloads>  
- Baixe o instalador para Windows.  
- **Durante a instalação**:  
  - Escolha **Git Bash** como terminal padrão.  
  - Marque a opção **Git Credential Manager** (necessário para login integrado).  

✅ Teste a instalação abrindo o **Git Bash** e rodando:
```bash
git --version
```

📷 *Print sugerido:* tela inicial do Git Bash mostrando a versão instalada.  

---

## 3. Instalando o GitHub CLI (`gh`)
- Acesse: <https://cli.github.com/>  
- Baixe e instale a versão para Windows.  

✅ Teste a instalação no **Git Bash**:
```bash
gh --version
```

📷 *Print sugerido:* saída do comando `gh --version`.  

---

## 4. Configurando o VS Code para usar o Git Bash
1. Abra o VS Code.  
2. Vá em **File → Preferences → Settings**.  
3. Procure por **Terminal › Integrated › Profiles**.  
4. Garanta que existe o perfil **Git Bash** (ou adicione manualmente no `settings.json`):  
```json
{
  "terminal.integrated.profiles.windows": {
    "Git Bash": {
      "path": "C:\\\\Program Files\\\\Git\\\\bin\\\\bash.exe"
    }
  },
  "terminal.integrated.defaultProfile.windows": "Git Bash"
}
```

Agora, ao abrir o terminal integrado do VS Code (`Ctrl` + `` ` ``), o **Git Bash** será usado por padrão. 🎉  

📷 *Print sugerido:* tela do VS Code mostrando o **Git Bash** aberto no terminal integrado.  

---

## 5. Testando tudo junto
No terminal integrado do VS Code (com Git Bash ativo), rode:
```bash
git --version
gh --version
code --version
```

Se todos responderem com suas versões, seu ambiente está pronto. ✅  

📷 *Print sugerido:* terminal integrado do VS Code exibindo as três versões corretamente.  

---

## Conclusão
Você já preparou todas as ferramentas necessárias!  
No próximo capítulo, vamos explorar os **terminais** no Windows e entender por que priorizamos o **Git Bash**.

---

✅ **Próximo passo**: avançar para o [Capítulo 04 – Terminais](./04-terminais.md).
