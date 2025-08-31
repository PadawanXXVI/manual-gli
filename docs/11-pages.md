# Capítulo 11 – GitHub Pages

## Objetivo
Ensinar como publicar este manual como **livro online** usando o GitHub Pages, tanto na forma mais simples quanto em uma opção avançada com GitHub Actions.

---

## 1. O que é o GitHub Pages
- Serviço gratuito do GitHub que permite hospedar **sites estáticos** diretamente a partir de um repositório.  
- Ideal para documentações, manuais, blogs ou portfólios.  

📷 *Print sugerido:* tela do GitHub Pages com a mensagem "Your site is published!".  

---

## 2. Opção simples: branch `main` + pasta `/docs`
1. Crie um arquivo `docs/index.md`.  
2. Vá em **Settings → Pages** no repositório.  
3. Configure a origem:  
   - **Branch:** `main`  
   - **Folder:** `/docs`  

O site ficará disponível em uma URL como:
```
https://usuario.github.io/nome-do-repositorio/
```

📷 *Print sugerido:* tela de configuração do Pages em *Settings*.  

---

## 3. Opção avançada: usando GitHub Actions
- Permite compilar o projeto antes de publicar.  
- Útil para frameworks de documentação como **MkDocs**, **Docusaurus**, ou **Jekyll**.  

Exemplo de workflow (`.github/workflows/pages.yml`):
```yaml
name: Deploy Manual

on:
  push:
    branches: [ "main" ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Configurar Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'

      - name: Build
        run: echo "Rodar script de build aqui"

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v4
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./docs
```

📷 *Print sugerido:* aba *Actions* mostrando workflow de deploy rodando com sucesso.  

---

## 4. Estrutura recomendada
- `docs/` → capítulos do manual em Markdown.  
- `docs/assets/` → imagens (prints).  
- `docs/index.md` → página inicial do manual.  

---

## 5. Testando o site
- Acesse a URL gerada.  
- Verifique se os links entre capítulos funcionam corretamente.  
- Caso a página não apareça de imediato, aguarde alguns minutos (build pode demorar).  

📷 *Print sugerido:* navegador mostrando a página inicial do manual publicada.  

---

## Conclusão
Com o GitHub Pages, você transforma seu repositório em um **site acessível online**, facilitando o compartilhamento do manual com colegas e a comunidade.  

---

✅ **Próximo passo**: avançar para o [Capítulo 12 – PDF](./12-pdf.md).
