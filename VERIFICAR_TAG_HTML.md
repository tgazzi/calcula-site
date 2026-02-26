# Verificar com Tag HTML (em vez do arquivo)

O método "Arquivo HTML" falhou porque o Google não encontrou o arquivo no endereço esperado. Use o método **Tag HTML**:

---

## Passos

1. No **Google Search Console**, na propriedade **https://tgazzi.github.io/calcula-site**, vá em **Configurações** (ícone de engrenagem) → **Verificação de propriedade** (ou abra de novo o fluxo de verificação).

2. Escolha o método **Tag HTML** (não "Arquivo HTML").

3. O Google vai mostrar uma tag assim:
   ```html
   <meta name="google-site-verification" content="XXXXXXXXXXXX" />
   ```
   Copie **só o valor de content** (a parte entre aspas), por exemplo: `XXXXXXXXXXXX`.

4. No projeto, abra **site-desenvolvedor/index.html**. Procure a linha:
   ```html
   <meta name="google-site-verification" content="COLE_SUA_TAG_AQUI" />
   ```
   Substitua **COLE_SUA_TAG_AQUI** pelo valor que você copiou (o content da tag do Google). Salve.

5. Envie para o GitHub:
   ```bash
   cd site-desenvolvedor
   git add index.html
   git commit -m "Tag verificação Search Console"
   git push
   ```

6. Espere 1–2 minutos e no Search Console clique em **Verificar**.

O Google vai olhar a página **https://tgazzi.github.io/calcula-site/** (a inicial) e procurar a tag no `<head>`. Se a tag estiver certa, a verificação passa.
