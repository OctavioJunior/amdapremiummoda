# AMDA Premium Moda — Site Oficial

Site elegante e leve para a loja **AMDA Premium Moda**, com foco em conversão via WhatsApp.

---

## ⚙️ Stack

- **Framework:** Astro (geração estática)
- **CMS:** Decap CMS (gerenciamento via painel visual)
- **Deploy:** Netlify (gratuito)
- **Vendas:** WhatsApp (link direto)

---

## 🚀 Deploy no Netlify

### 1. Suba o projeto no GitHub

```bash
git init
git add .
git commit -m "feat: projeto inicial AMDA Premium Moda"
git remote add origin https://github.com/SEU_USUARIO/amda-premium-moda.git
git push -u origin main
```

### 2. Conecte ao Netlify

1. Acesse [netlify.com](https://netlify.com) e faça login
2. Clique em **"Add new site" → "Import an existing project"**
3. Conecte ao GitHub e selecione o repositório
4. Confirme as configurações de build:
   - **Build command:** `npm run build`
   - **Publish directory:** `dist`
5. Clique em **"Deploy site"**

### 3. Ative Netlify Identity + Git Gateway

1. No painel do Netlify, vá em **Site settings → Identity**
2. Clique em **"Enable Identity"**
3. Em **Services → Git Gateway**, clique em **"Enable Git Gateway"**
4. Em **Registration**, selecione **"Invite only"**

### 4. Crie o usuário administrador

1. Vá em **Identity → Invite users**
2. Insira o e-mail do administrador
3. O usuário receberá um e-mail para criar a senha

---

## 🛠️ Desenvolvimento local

```bash
npm install
npm run dev
```

Acesse: http://localhost:4321

---

## 📝 Gerenciar Produtos

### Via painel CMS (recomendado)

1. Acesse `https://SEU-SITE.netlify.app/admin`
2. Faça login com o e-mail e senha criados
3. Clique em **"Produtos"**
4. Adicione, edite ou remova produtos
5. Clique em **"Publicar"** — as mudanças vão automaticamente para o site

### Manualmente (arquivo JSON)

Edite o arquivo `src/data/produtos.json`:

```json
{
  "items": [
    {
      "nome": "Nome do Produto",
      "preco": 199.90,
      "imagem": "/uploads/nome-da-imagem.jpg"
    }
  ]
}
```

---

## 📱 Configurar WhatsApp

Atualize o número de WhatsApp nos arquivos abaixo.  
Substitua `5551984229690` pelo número real (DDI + DDD + número, sem espaços ou símbolos):

- `src/layouts/BaseLayout.astro` (rodapé)
- `src/pages/index.astro` (CTA banner e bottom section)
- `src/pages/produtos.astro` (bottom CTA)
- `src/components/WhatsButton.astro` (prop padrão `telefone`)

---

## 📁 Estrutura

```
/public
  /admin
    index.html       ← Painel Decap CMS
    config.yml       ← Configuração do CMS
  /uploads           ← Imagens dos produtos
  placeholder.svg    ← Imagem padrão

/src
  /components
    ProductCard.astro
    WhatsButton.astro
  /layouts
    BaseLayout.astro
  /pages
    index.astro      ← Página inicial
    produtos.astro   ← Catálogo de produtos
  /data
    produtos.json    ← Dados dos produtos
```

---

## 🎨 Identidade Visual

| Variável CSS      | Cor        | Uso                    |
|-------------------|------------|------------------------|
| `--rose`          | `#C58A7A`  | Destaque, acentos      |
| `--rose-dark`     | `#8C5A52`  | Títulos, botões        |
| `--rose-light`    | `#E8D0CB`  | Fundos suaves          |
| `--bg`            | `#F8F6F5`  | Fundo principal        |
| `--text`          | `#2B2B2B`  | Texto geral            |

---

## 🔮 Próximos passos sugeridos

- [ ] Adicionar categorias (roupas / acessórios)
- [ ] Página individual de produto
- [ ] Integração com Mercado Pago
- [ ] SEO: meta tags por produto
