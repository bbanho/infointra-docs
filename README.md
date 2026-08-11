# infointra-docs

Documentação técnica multi-projeto (GitHub Pages).

> ⚠️ **Repo de artefatos estáticos apenas.** Este repositório contém **somente builds compilados** (HTML/CSS/JS) — as fontes das documentações (`.md`, config) vivem nos repos privados de cada projeto e são compiladas localmente antes do push.

## Projetos publicados

| Projeto | URL | Fonte (privada) |
|---|---|---|
| Ampla Vendas ERP | https://docs.axio.eng.br/ampla/ | `amplainformatica-erp-integrado` (wiki/) |

## Publicar (a partir do repo privado do projeto)

```bash
# 1. Build com base /<projeto>/ (links internos apontam para /<projeto>/...)
cd ../amplainformatica-erp-integrado/wiki
npm run build -- --base /ampla/

# 2. Copiar o build para cá
cp -r .vitepress/dist/* ../../infointra-docs/ampla/

# 3. Commit + push (GitHub Pages atualiza sozinho ~1 min)
cd ../../infointra-docs
git add -A && git commit -m "docs: atualiza wiki ampla (build)" && git push
```

## URL

- Produção: https://docs.axio.eng.br/ampla/ (custom domain — requer TXT verificado)
- Fallback (Pages): https://bbanho.github.io/infointra-docs/ampla/
