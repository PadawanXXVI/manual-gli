# Capítulo 06 – Repositórios

## Objetivo
Explicar o que é um repositório no Git/GitHub, como criá-lo, clonar, inicializar e trabalhar com commits iniciais.

---

## 1. O que é um repositório?
- Um **repositório** é onde o Git armazena o histórico do seu projeto.  
- Pode ser **local** (na sua máquina) ou **remoto** (no GitHub).  
- Normalmente trabalhamos com os dois em conjunto.  

---

## 2. Criando um repositório local
1. Crie uma pasta para o projeto:
```bash
mkdir meu-projeto
cd meu-projeto
```

2. Inicialize o Git:
```bash
git init
```

3. Verifique se foi criado o repositório oculto:
```bash
ls -a
```

---

## 3. Criando um repositório remoto no GitHub
Com o GitHub CLI, você pode criar sem sair do terminal:

```bash
gh repo create meu-projeto --public --source=. --remote=origin --push
```

Explicação das opções:
- `--public` → repositório público.  
- `--source=.` → usa a pasta atual como origem.  
- `--remote=origin` → adiciona o remoto chamado `origin`.  
- `--push` → envia o commit inicial automaticamente.  

---

## 4. Clonando um repositório existente
Se o projeto já existe no GitHub, basta clonar:

```bash
gh repo clone usuario/repositorio
```

ou usando Git diretamente:
```bash
git clone https://github.com/usuario/repositorio.git
```

---

## 5. Verificando repositórios remotos
Para listar os remotos configurados:
```bash
git remote -v
```

Resultado esperado:
```
origin  https://github.com/usuario/repositorio.git (fetch)
origin  https://github.com/usuario/repositorio.git (push)
```

---

## 6. Commit inicial
1. Crie um arquivo simples:
```bash
echo "# Meu Projeto" > README.md
```

2. Adicione ao Git:
```bash
git add README.md
```

3. Crie o commit:
```bash
git commit -m "chore: commit inicial com README"
```

4. Envie para o remoto:
```bash
git push origin main
```

---

## Conclusão
Agora você já sabe como criar repositórios locais, remotos, clonar existentes e fazer seu primeiro commit.  
No próximo capítulo, vamos estudar o **Workflow (ciclo Git)** para entender como organizar melhor o fluxo de trabalho.

---

✅ **Próximo passo**: avançar para o [Capítulo 07 – Workflow (ciclo Git)](./07-workflow.md).
