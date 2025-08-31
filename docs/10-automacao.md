# Capítulo 10 – Automação

## Objetivo
Ensinar como aumentar a produtividade usando o **GitHub CLI (`gh`)** com **aliases**, **extensões** e **scripts** para automatizar tarefas repetitivas.

---

## 1. Aliases (`gh alias`)
- Permitem criar **atalhos** para comandos longos.  
- Útil para simplificar comandos usados com frequência.  

Exemplo:
```bash
gh alias set co "pr checkout"
```
Agora, em vez de rodar `gh pr checkout 123`, basta usar:
```bash
gh co 123
```

📷 *Print sugerido:* terminal mostrando a criação e uso de alias `gh co`.  

---

## 2. Extensões (`gh extension`)
- O `gh` suporta extensões criadas pela comunidade.  
- Isso amplia os recursos além dos comandos oficiais.  

Instalar extensão:
```bash
gh extension install owner/gh-ext
```

Listar extensões instaladas:
```bash
gh extension list
```

📷 *Print sugerido:* saída de `gh extension list` mostrando uma extensão instalada.  

---

## 3. Automatizando tarefas repetitivas
Você pode criar scripts simples (em **Bash** ou **PowerShell**) que chamam o `gh` para automatizar o dia a dia.  

### Criar múltiplas issues de uma vez:
```bash
for i in {1..5}; do
  gh issue create --title "Tarefa $i" --body "Descrição da tarefa $i"
done
```

### Criar labels de forma automática:
```bash
gh label create "docs" --description "Documentação" --color 0366d6
gh label create "print-pendente" --description "Falta adicionar prints" --color ff0000
```

📷 *Print sugerido:* terminal executando script que cria várias issues de uma vez.  

---

## 4. Integração com VS Code
Alguns comandos podem abrir direto no navegador para facilitar:  

- Abrir issue:
```bash
gh issue view 1 --web
```

- Abrir PR:
```bash
gh pr view 5 --web
```

📷 *Print sugerido:* VS Code com terminal Git Bash e navegador abrindo issue/PR.  

---

## Conclusão
Com **aliases**, **extensões** e **scripts**, você pode transformar o `gh` em uma ferramenta muito mais poderosa e adaptada ao seu fluxo de trabalho.  

No próximo capítulo, vamos aprender a publicar o manual online usando **GitHub Pages**.  

---

✅ **Próximo passo**: avançar para o [Capítulo 11 – GitHub Pages](./11-pages.md).
