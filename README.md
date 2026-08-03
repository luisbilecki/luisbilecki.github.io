# bilecki-landing-page

Portfólio Jekyll de Luís Felipe Bilecki, pronto pra GitHub Pages.

Home atual mostra apenas "Em Construção" (PT-BR / EN / ES). Páginas de
projetos, experiência e contato ficam prontas em placeholder pra quando
conteúdo real for adicionado.

## Preencher placeholders

Arquivos com conteúdo placeholder (marcados `<!-- PLACEHOLDER -->`):
- `projects.md` — lista de projetos reais
- `experience.md` — histórico profissional/formação
- `contact.md` — email (opcional)

## Rodar local

```bash
make install
make serve
```

ou direto:

```bash
bundle install
bundle exec jekyll serve
```

## Deploy no GitHub Pages

1. Renomear/criar repo remoto `luisbilecki.github.io` (ou outro nome + habilitar Pages nas settings)
2. `git remote add origin <url>` e `git push -u origin main`
3. Settings → Pages → Source: branch `main`

## Domínio custom

1. Criar arquivo `CNAME` na raiz com o domínio (ex: `seudominio.com`)
2. DNS no registrar:
   - Domínio raiz: A records apontando pros IPs do GitHub Pages
   - `www`: CNAME record apontando pra `luisbilecki.github.io`
3. Settings → Pages → habilitar "Enforce HTTPS" após DNS propagar
