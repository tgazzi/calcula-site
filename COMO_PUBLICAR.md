# Como publicar este site (para AdMob + Play Store)

Este site tem só uma página e o arquivo **app-ads.txt**, para você cumprir o que o AdMob e a Play Store pedem (site do desenvolvedor + app-ads.txt).

---

## Opção 1: GitHub Pages (recomendado, grátis)

### 1. Criar um repositório no GitHub

1. Acesse [github.com](https://github.com) e faça login.
2. Clique em **+** → **New repository**.
3. Nome sugerido: **calcula-ai** ou **calculaai-site**.
4. Deixe **Public**, não marque "Add a README".
5. Clique em **Create repository**.

### 2. Subir os arquivos

Na pasta do projeto você tem a pasta **site-desenvolvedor** com:

- `index.html`
- `app-ads.txt`

**No terminal** (na pasta do seu projeto CalculaAI):

```bash
cd site-desenvolvedor
git init
git add index.html app-ads.txt
git commit -m "Site desenvolvedor + app-ads.txt"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/calcula-ai.git
git push -u origin main
```

(Substitua **SEU_USUARIO** pelo seu usuário do GitHub e **calcula-ai** pelo nome do repositório que você criou.)

Se preferir, pode criar o repositório no GitHub, clicar em "uploading an existing file" e arrastar só os arquivos **index.html** e **app-ads.txt** (não precisa da pasta).

### 3. Ativar o GitHub Pages

1. No repositório no GitHub, vá em **Settings** → **Pages** (menu lateral).
2. Em **Source**, escolha **Deploy from a branch**.
3. Em **Branch**, selecione **main** e a pasta **/ (root)**.
4. Salve (**Save**).

Em 1–2 minutos o site fica no ar em:

**https://SEU_USUARIO.github.io/calcula-ai/**

O **app-ads.txt** estará em:

**https://SEU_USUARIO.github.io/calcula-ai/app-ads.txt**

### 4. Usar no Play Console e no AdMob

1. **Play Console** → seu app → **Presença na loja** → **Principais detalhes do app** → em **Site do desenvolvedor** coloque:
   - `https://SEU_USUARIO.github.io/calcula-ai`
   (com o seu usuário e nome do repo.)
2. Salve e publique se precisar.
3. No **AdMob**, rode de novo a verificação do app. O AdMob vai procurar o app-ads.txt nesse endereço.

---

## Opção 2: Netlify (também grátis)

1. Acesse [netlify.com](https://www.netlify.com) e crie uma conta (pode ser com GitHub).
2. Arraste a pasta **site-desenvolvedor** (com index.html e app-ads.txt dentro) para a área "Drag and drop your site output folder here" no Netlify.
3. O Netlify vai dar uma URL tipo **algo-aleatorio.netlify.app**.
4. Use essa URL no Play Console em **Site do desenvolvedor**.
5. O app-ads.txt estará em **https://algo-aleatorio.netlify.app/app-ads.txt**.

---

## Resumo

| Onde              | O que colocar |
|-------------------|----------------|
| **Play Console**  | URL do site (ex.: `https://SEU_USUARIO.github.io/calcula-ai`) |
| **Seu site**      | Já tem `index.html` e `app-ads.txt` na pasta **site-desenvolvedor** |

Depois de publicar, espere alguns minutos e tente verificar o app de novo no AdMob.
