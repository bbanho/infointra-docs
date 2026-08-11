# infointra-docs

Wiki VitePress do **Ampla Vendas ERP** (PWA Offline-First de Força de Vendas).

> ⚠️ **Repo de artefatos estáticos apenas.** Este repositório contém **somente o build compilado** (HTML/CSS/JS) do VitePress — a fonte da documentação (`.md`, config) vive no repo privado `amplainformatica-erp-integrado` e é compilada localmente antes do push.

## Publicar (a partir do repo privado)

```bash
# 1. Build com base /docs/ (links internos apontam para /docs/...)
cd ../amplainformatica-erp-integrado/wiki
npm run build -- --base /docs/

# 2. Copiar o build para cá
cp -r .vitepress/dist/* ../../infointra-docs/docs/

# 3. Commit + push (GitHub Pages atualiza sozinho ~1 min)
cd ../../infointra-docs
git add -A && git commit -m "docs: atualiza wiki (build)" && git push
```

## URL

- Produção: https://infointra.axio.eng.br/docs/
- Fallback (Pages): https://bbanho.github.io/infointra-docs/docs/
