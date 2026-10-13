# Portfólio — Kevin Souza

Site pessoal em **https://kevinsouza.ghostcodetech.com**: uma página só, em inglês e português (botão EN/PT), com apresentação, projeto em destaque (Reading Your Soul), experiência, skills e contato.

## Estrutura

```
public/
  index.html   página (HTML + CSS)
  app.js       troca de idioma e animações ao rolar
  _headers     headers de segurança (CSP, HSTS, bloqueio de iframe)
worker.js      redireciona http → https e serve os arquivos de public/
wrangler.jsonc configuração do Cloudflare Worker e do subdomínio
```

Sem build e sem dependências: é HTML, CSS e JavaScript puros.

## Editar textos

Cada texto existe nas duas línguas, lado a lado:

```html
<span data-l="en">Get in touch</span><span data-l="pt">Fale comigo</span>
```

Ao mudar um, mude o outro também.

## Ver localmente

```bash
wrangler dev
```

## Publicar

```bash
wrangler deploy
```

Rode dentro desta pasta. Publica direto em kevinsouza.ghostcodetech.com (Cloudflare, conta GhostCode).
