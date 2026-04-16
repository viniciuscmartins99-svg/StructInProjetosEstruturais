# StructIn — Guia Completo para Colocar o Site no Ar

## Estrutura do Projeto

```
structin-site/
├── index.html          ← Página principal (todo o site)
└── images/
    ├── projeto_casa.png
    ├── interiores.png
    ├── planta_loja.png
    └── render_loja.png
```

---

## OPÇÃO 1 — Vercel (Recomendada, Grátis)

A forma mais rápida e profissional. O site fica online em menos de 5 minutos.

**Passo 1 — Criar conta no GitHub**
1. Acesse [github.com](https://github.com) e crie uma conta gratuita
2. Clique em **"New repository"** (botão verde)
3. Nome: `structin-site` → marque **Public** → Create

**Passo 2 — Enviar os arquivos**
1. No repositório criado, clique em **"uploading an existing file"**
2. Arraste a pasta inteira (`index.html` + pasta `images/`) para a área de upload
3. Clique **"Commit changes"**

**Passo 3 — Conectar à Vercel**
1. Acesse [vercel.com](https://vercel.com) e faça login com sua conta GitHub
2. Clique **"Add New Project"**
3. Selecione o repositório `structin-site`
4. Clique **"Deploy"** — pronto, o site estará no ar!

**Passo 4 — Domínio personalizado**
1. Compre um domínio (ex: `structin.com.br`) no Registro.br (~R$40/ano)
2. No painel da Vercel → Settings → Domains → adicione `structin.com.br`
3. A Vercel vai mostrar os registros DNS. No Registro.br, vá em DNS e adicione:
   - Tipo **A** → IP que a Vercel informar
   - Tipo **CNAME** → `cname.vercel-dns.com` (para www)
4. Aguarde até 24h para propagação

---

## OPÇÃO 2 — Netlify (Grátis, Drag & Drop)

Mais simples, sem precisar de GitHub.

1. Acesse [netlify.com](https://netlify.com) e crie uma conta
2. Na tela inicial, localize **"Deploy manually"**
3. Arraste a pasta `structin-site` inteira para a área indicada
4. Pronto! O site recebe uma URL tipo `structin-xyz.netlify.app`
5. Para domínio próprio: Domain settings → Add custom domain → siga os passos de DNS

---

## OPÇÃO 3 — GitHub Pages (Grátis)

1. Crie o repositório no GitHub (como na Opção 1)
2. Vá em **Settings** → **Pages**
3. Em "Source", selecione **main branch** e **/ (root)**
4. Clique **Save**
5. O site ficará disponível em `seuusuario.github.io/structin-site`

---

## Personalizações Necessárias

Antes de publicar, ajuste os seguintes itens no `index.html`:

### 1. Número do WhatsApp
Procure por `5561999999999` e substitua pelo número real (formato: 55 + DDD + número, sem espaços).

### 2. Fotos da equipe
No HTML, os cards de equipe usam ícones placeholder. Para colocar as fotos reais:
- Salve as fotos como `salmy.jpg` e `vinicius.jpg` na pasta `images/`
- No HTML, substitua o bloco `<div class="team-photo" style="background:...">...</div>` por:
```html
<img src="images/salmy.jpg" alt="Eng. Salmy Luz" class="team-photo">
```

### 3. Imagem do banner (hero)
O banner usa uma imagem do Unsplash como placeholder. Para usar uma foto própria:
- Salve a imagem na pasta `images/` como `hero.jpg`
- No CSS, encontre `.hero-bg` e troque a `url(...)` por `url('images/hero.jpg')`

### 4. Links de redes sociais
Procure os links de Instagram e LinkedIn no footer e substitua pelas URLs reais.

---

## Dicas de SEO e Performance

- **Otimize as imagens**: Use [tinypng.com](https://tinypng.com) para comprimir as imagens antes de subir
- **Favicon**: Adicione um favicon (ícone da aba) com a logo da StructIn
- **Google Analytics**: Crie uma conta no Google Analytics e adicione o script antes do `</head>`
- **Google Meu Negócio**: Cadastre a StructIn para aparecer nas buscas locais de Brasília
- **SSL**: Vercel e Netlify já fornecem HTTPS gratuito automaticamente

---

## Custo Total Estimado

| Item | Custo |
|------|-------|
| Hospedagem (Vercel/Netlify) | **Grátis** |
| Domínio .com.br (Registro.br) | ~R$ 40/ano |
| SSL (HTTPS) | **Grátis** (incluso) |
| **Total** | **~R$ 40/ano** |
