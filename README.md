# infointra-docs

Documentação técnica multi-projeto (GitHub Pages).

> ⚠️ **Repositório de artefatos estáticos apenas — MIGRADO.** O conteúdo de documentação de todos os projetos foi consolidado no repositório central **`bbanho/axio-docs`**, publicado em **https://docs.axio.eng.br**.
>
> Este repositório está **sendo desativado** como site Pages. O custom domain `docs.axio.eng.br` pertence agora ao repo `axio-docs`. As fontes (`.md`) continuam vivendo nos repos privados de cada projeto, compiladas localmente antes do push para `axio-docs`.

## Publicar (a partir do repo privado do projeto)

Após a migração, o build de cada projeto deve ser copiado para o repositório central `axio-docs` (e não mais para cá):

```bash
# 1. Build com base /<projeto>/ (links internos apontam para /<projeto>/...)
cd ../amplainformatica-erp-integrado/wiki
npm run build -- --base /ampla/

# 2. Copiar o build para o repo central
cp -r .vitepress/dist/* ../../axio-docs/ampla/

# 3. Commit + push no repo central (GitHub Pages atualiza em ~1 min)
cd ../../axio-docs
git add -A && git commit -m "docs: atualiza wiki ampla (build)" && git push
```

## URL

- Produção (central): https://docs.axio.eng.br/ampla/
- Fallback (Pages): https://bbanho.github.io/axio-docs/ampla/
