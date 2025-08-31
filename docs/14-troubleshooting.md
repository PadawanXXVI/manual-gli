# Capítulo 14 – Troubleshooting

## Objetivo
Apresentar os problemas mais comuns enfrentados ao usar Git, GitHub, VS Code e GitHub CLI, além de mostrar soluções práticas.

---

## 1. Push pedindo senha repetidamente
- **Causa:** o Git não está salvando as credenciais.  
- **Solução:** configure o Credential Manager.  
```bash
git config --global credential.helper manager-core
```

📷 *Print sugerido:* terminal mostrando push pedindo senha várias vezes.  

---

## 2. Erro de autenticação no GitHub CLI
- **Causa:** login não realizado ou token inválido.  
- **Solução:**  
```bash
gh auth login
gh auth status
```

📷 *Print sugerido:* saída do `gh auth status` mostrando "not logged in".  

---

## 3. Conflito de múltiplas contas (pessoal vs trabalho)
- **Sintoma:** commits enviados com o email errado.  
- **Solução:** configure email específico por repositório:  
```bash
git config user.email "meuemail@empresa.com"
```

📷 *Print sugerido:* commit no histórico aparecendo com email incorreto.  

---

## 4. Proxy ou firewall corporativo
- **Problema:** conexões externas para GitHub bloqueadas.  
- **Solução:** configurar proxy no Git e no `gh`.  
```bash
git config --global http.proxy http://usuario:senha@proxy:porta
```

📷 *Print sugerido:* mensagem de erro "Could not resolve host: github.com".  

---

## 5. Erro ao clonar repositório
- **Causa:** URL incorreta ou falta de permissão.  
- **Solução:**  
  - Conferir se o repositório é público/privado.  
  - Verificar se você está logado com a conta correta.  
```bash
gh repo clone usuario/repositorio
```

📷 *Print sugerido:* terminal mostrando erro de permissão ao clonar.  

---

## 6. Conflitos de merge
- **Sintoma:** Git mostra `CONFLICT` ao tentar merge.  
- **Solução:**
  1. Abra os arquivos conflitantes.  
  2. Resolva os trechos entre `<<<<<<<` e `>>>>>>>`.  
  3. Depois:  
  ```bash
  git add arquivo
  git commit
  ```

📷 *Print sugerido:* editor mostrando marcações de conflito `<<<<<<< HEAD`.  

---

## Checklist rápido
Se algo não funcionar, verifique:  
- Está logado no GitHub (`gh auth status`)?  
- O repositório remoto existe e está correto (`git remote -v`)?  
- Está na branch certa (`git branch`)?  
- Seu VS Code está conectado à conta GitHub?  

---

## Conclusão
Problemas são comuns, mas quase sempre têm soluções simples.  
Com esse guia, você terá segurança para resolver as principais situações do dia a dia.  

---

✅ **Próximo passo**: avançar para o [Capítulo 15 – Cheat-Sheet](./15-cheatsheet.md).
