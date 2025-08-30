# Capítulo 04 – Terminais

## Objetivo
Explicar os principais terminais disponíveis no Windows, destacar as diferenças entre eles e justificar a escolha do **Git Bash** como terminal padrão para o manual.

---

## 1. O que é um terminal?
O terminal é a interface onde você digita comandos para o sistema ou ferramentas como Git.  
No Windows, existem vários terminais que podem ser usados com Git e GitHub.

📷 *Print sugerido:* tela mostrando o VS Code com a lista de terminais disponíveis (CMD, PowerShell, Git Bash).  

---

## 2. Principais terminais

### CMD (Prompt de Comando)
- Terminal clássico do Windows.  
- Suporte limitado a comandos Unix/Linux.  
- Útil apenas em casos muito específicos ou scripts antigos.  

Exemplo:
```cmd
dir
```

📷 *Print sugerido:* janela do CMD com o comando `dir` sendo executado.  

---

### PowerShell
- Terminal moderno do Windows.  
- Suporta automação com **scripts PowerShell**.  
- Integração maior com o sistema operacional.  
- Pode rodar Git, mas alguns comandos diferem de Unix/Linux.  

Exemplo:
```powershell
Get-ChildItem
```

📷 *Print sugerido:* janela do PowerShell mostrando `Get-ChildItem`.  

---

### Git Bash
- Terminal baseado em Unix, instalado junto com o Git.  
- Traz comandos Linux para dentro do Windows.  
- Compatível com praticamente todos os exemplos de documentação Git.  
- É o terminal **recomendado neste manual**.  

Exemplo:
```bash
ls -la
```

📷 *Print sugerido:* Git Bash mostrando `ls -la` na pasta do repositório.  

---

## 3. Comparativo rápido

| Terminal   | Vantagens | Desvantagens | Indicado para |
|------------|-----------|--------------|---------------|
| **CMD**    | Simples, sempre disponível | Muito limitado | Scripts legados |
| **PowerShell** | Moderno, integração com Windows | Sintaxe diferente do Unix | Usuários avançados Windows |
| **Git Bash** | Suporte a comandos Unix, compatível com documentação Git | Precisa ser instalado | Git, GitHub e desenvolvimento |

📷 *Print sugerido:* tabela ou tela lado a lado dos três terminais abertos.  

---

## 4. Justificativa da escolha
No manual, vamos priorizar o **Git Bash** porque:
- É o mais próximo da documentação oficial do Git.  
- Facilita entender onde você está (branch, diretório etc.).  
- Exemplos prontos funcionam tanto no Windows quanto no Linux/Mac.  

> Obs.: Sempre que houver diferença entre os terminais, vamos trazer a versão **Git Bash** primeiro e, logo abaixo, a variação em PowerShell ou CMD.

---

## Conclusão
Agora você já conhece os terminais e entende por que usaremos o **Git Bash** como padrão.  
No próximo capítulo, veremos como configurar o **login integrado (GLI)** para conectar Git, GitHub, VS Code e GitHub CLI.

---

✅ **Próximo passo**: avançar para o [Capítulo 05 – Login integrado](./05-login-integrado.md).

