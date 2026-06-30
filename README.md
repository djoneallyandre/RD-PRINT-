# RD print — Site de Vendas

Landing page estática (HTML/CSS/JS puro, sem build). Sobe em segundos no Vercel.

## Estrutura
```
rd-site/
├── index.html      ← a página
└── img/
    ├── logo.png    ← logo principal
    ├── mono.png    ← monograma (favicon/avatar)
    └── portfolio-01.jpg ... portfolio-19.jpg   ← suas fotos
```

## 1) Trocar o número de WhatsApp (IMPORTANTE)
Abra `index.html`, procure a linha (lá embaixo, no `<script>`):
```js
var WHATSAPP = "5527000000000";
```
Troque pelo seu número novo no formato **55 + DDD + número, só dígitos**.
Ex.: `5527999998888`. Todos os botões da página passam a apontar pra ele automaticamente.

## 2) Trocar / acrescentar fotos do portfólio
- As fotos ficam em `img/` com os nomes `portfolio-01.jpg` até `portfolio-19.jpg`.
- Para trocar uma, salve a nova com o mesmo nome por cima.
- Para mudar a quantidade, ajuste o número no `index.html`:
  ```js
  for (var i=1; i<=19; i++){   // troque 19 pela quantidade de fotos
  ```
- Dica: mantenha cada foto com no máximo ~1400px de largura pra página carregar rápido.

## 3) Subir no Vercel (3 opções)

### A) Mais fácil — arrastar e soltar
1. Crie conta grátis em https://vercel.com (login com Google).
2. No painel, clique **Add New → Project → Deploy** (ou use https://vercel.com/new).
3. **Arraste a pasta `rd-site` inteira** para a área de upload.
4. Clique **Deploy**. Em ~20s seu site está no ar com um link `…vercel.app`.

### B) Pelo GitHub (recomendado pra atualizar fácil)
1. Suba a pasta `rd-site` num repositório no GitHub.
2. No Vercel: **Add New → Project → Import** o repositório.
3. Framework Preset: **Other**. Deixe tudo em branco e **Deploy**.
4. Toda vez que você editar e der push, o site atualiza sozinho.

### C) Pelo terminal (Vercel CLI)
```bash
npm i -g vercel
cd rd-site
vercel        # siga as perguntas, escolha "Other"
vercel --prod # publica em produção
```

## 4) Domínio próprio (opcional)
No projeto do Vercel → **Settings → Domains** → adicione seu domínio
(ex.: `rdprint.com.br`) e siga as instruções de DNS. Funciona com o link `.vercel.app` enquanto isso.

---
Cores da marca: azul `#1426B8` · laranja `#FF7A00` — Fontes: Sora + Inter
