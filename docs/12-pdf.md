# Capítulo 12 – PDF

## Objetivo
Ensinar como gerar uma versão **offline** do manual em formato **PDF**, a partir dos arquivos Markdown que estão no repositório.

---

## 1. Por que gerar um PDF?
- Permite **compartilhar offline**.  
- Útil em ambientes acadêmicos ou corporativos.  
- Facilita a **impressão** ou envio por e-mail.  

---

## 2. Ferramentas recomendadas

### Pandoc (recomendado)
Ferramenta poderosa para converter arquivos Markdown em PDF.  

Exemplo simples:
```bash
pandoc docs/*.md -o manual-gli.pdf
```

### Alternativas
- Extensões do VS Code, como **Markdown PDF**.  
- Serviços online de conversão (menos recomendados por dependerem de upload).  

📷 *Print sugerido:* terminal mostrando execução do Pandoc e geração do PDF.  

---

## 3. Preparando os arquivos
- Certifique-se de que todos os capítulos estão **numerados** (`01-`, `02-`, etc.).  
- Garanta que existe um `docs/index.md` servindo como capa/índice.  
- Use títulos hierárquicos (`#`, `##`, `###`) para permitir a geração de sumário automático.  

---

## 4. Personalização
O Pandoc permite adicionar capa, sumário e metadados.  

Exemplo:
```bash
pandoc docs/*.md -o manual-gli.pdf \
  --metadata title="Guia Prático do GLI" \
  --metadata author="Anderson de Matos Guimarães" \
  --metadata date="2025-08-30"
```

📷 *Print sugerido:* primeira página do PDF com capa gerada automaticamente.  

---

## 5. Automatizando a geração
Você pode criar um script simples para padronizar a geração do PDF:  

Arquivo `scripts/gerar-pdf.sh`:
```bash
#!/bin/bash
pandoc docs/*.md -o build/manual-gli.pdf --metadata title="Guia GLI"
```

📷 *Print sugerido:* pasta `build/` contendo o arquivo `manual-gli.pdf`.  

---

## 6. Integração com GitHub Actions (opcional)
Também é possível automatizar a geração de PDF a cada commit, usando workflows.  

Exemplo de workflow (`.github/workflows/pdf.yml`):
```yaml
name: Gerar PDF

on:
  push:
    branches: [ "main" ]

jobs:
  build-pdf:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Instalar Pandoc
        run: sudo apt-get install -y pandoc
      - name: Gerar PDF
        run: pandoc docs/*.md -o manual-gli.pdf
      - name: Upload do artefato
        uses: actions/upload-artifact@v4
        with:
          name: manual-gli
          path: manual-gli.pdf
```

📷 *Print sugerido:* aba *Actions* mostrando workflow de geração do PDF.  

---

## Conclusão
Agora você sabe como transformar o manual em um PDF completo, personalizável e até automatizado com GitHub Actions.  

---

✅ **Próximo passo**: avançar para o [Capítulo 13 – Times](./13-times.md).
