# Verificar o site no Google Search Console (para o AdMob aceitar)

O AdMob pede que o site esteja verificado no **Google Search Console**. Siga estes passos.

---

## 1. Abrir o Search Console

1. Acesse: **https://search.google.com/search-console**
2. Faça login com a **mesma conta Google** que usa no AdMob e no Play Console.

---

## 2. Adicionar a propriedade (o site)

1. Clique em **Adicionar propriedade** (ou "Add property").
2. Escolha **Prefixo do URL**.
3. No campo, digite **exatamente**:
   ```
   https://tgazzi.github.io/calcula-site
   ```
4. Clique em **Continuar**.

---

## 3. Verificar a propriedade (método por tag HTML)

1. O Search Console vai mostrar várias opções de verificação. Escolha **Tag HTML** (ou "HTML tag").
2. Copie a tag que aparecer, algo como:
   ```html
   <meta name="google-site-verification" content="ABC123xyz..." />
   ```
3. No projeto, abra o arquivo **`site-desenvolvedor/index.html`**.
4. Dentro de `<head>`, **logo após** a linha `<meta name="viewport" ...>`, **cole** essa tag (a que você copiou). Exemplo:
   ```html
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1">
     <meta name="google-site-verification" content="COLE_AQUI_O_CONTEUDO_QUE_O_GOOGLE_DEU" />
     <title>Calcula.ai – App de calculadoras</title>
   ```
5. Salve o arquivo, faça commit e envie para o GitHub (push). Exemplo:
   ```bash
   cd site-desenvolvedor
   git add index.html
   git commit -m "Adiciona verificação Google Search Console"
   git push
   ```
6. Espere 1–2 minutos (para o GitHub Pages atualizar).
7. No Search Console, clique em **Verificar**.

Quando a verificação for concluída, o site passa a aparecer como “seu” no Google. Aí você pode tentar de novo a verificação do app no AdMob.

---

## Se preferir verificar por arquivo HTML

1. No Search Console, escolha **Arquivo HTML** em vez de tag.
2. O Google vai dar um nome de arquivo (ex.: `google123abc.html`) e o conteúdo.
3. Crie um arquivo com esse nome na pasta **site-desenvolvedor**, com o conteúdo exato que o Google mostrar.
4. Faça commit, push para o GitHub, espere 1–2 min e clique em **Verificar** no Search Console.

---

## Resumo

| Onde | O que fazer |
|------|-------------|
| **Search Console** | Adicionar propriedade `https://tgazzi.github.io/calcula-site` e verificar (tag HTML ou arquivo). |
| **index.html** | Colar a tag `<meta name="google-site-verification" content="..." />` dentro do `<head>`. |
| **GitHub** | Dar push para o repositório `calcula-site`. |
| **AdMob** | Depois de verificado, tentar de novo a verificação do app. |
