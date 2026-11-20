# KEFA Engenharia | Site institucional

Site estático (HTML e CSS puro, sem build). Fica hospedado na Vercel e o código vive no GitHub.

## Arquivos

| Arquivo | Função |
|---|---|
| `index.html` | Página principal (home completa, pronta para celular) |
| `politica-de-privacidade.html` | Política de privacidade (LGPD), abre em `/politica-de-privacidade` |
| `404.html` | Página de erro para endereços inexistentes |
| `favicon.svg` | Ícone da aba do navegador |
| `apple-touch-icon.png` | Ícone ao salvar o site na tela do celular |
| `og-image.png` | Imagem de prévia ao compartilhar o link (WhatsApp, LinkedIn) |
| `robots.txt` e `sitemap.xml` | Orientações para o Google |
| `vercel.json` | Configuração da Vercel (URLs limpas, segurança, cache) |

## Passo 1 | Criar o repositório no GitHub

1. Entre em https://github.com e clique em **New repository**.
2. Nome sugerido: `kefa-site`. Pode ser **Private**. Não marque a opção de criar README.
3. Clique em **Create repository**.
4. Na tela seguinte, clique em **uploading an existing file**.
5. Descompacte o zip e arraste **todos os arquivos de dentro da pasta** (não a pasta em si). O `.gitignore` pode ficar oculto no computador; se não aparecer, tudo bem.
6. Clique em **Commit changes**.

Pelo terminal, se preferir:

```bash
cd kefa-site
git init
git add .
git commit -m "Site KEFA | versão inicial"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/kefa-site.git
git push -u origin main
```

## Passo 2 | Publicar na Vercel

1. Entre em https://vercel.com e faça login com a conta do GitHub.
2. Clique em **Add New... > Project** e escolha o repositório `kefa-site` (se não aparecer, clique em **Adjust GitHub App Permissions** e libere o repositório).
3. Em **Framework Preset**, escolha **Other**. Não preencha Build Command nem Output Directory.
4. Clique em **Deploy**. Em cerca de 30 segundos o site fica no ar em um endereço como `kefa-site.vercel.app`.

A partir daí, qualquer alteração enviada ao GitHub é publicada automaticamente.

## Passo 3 | Quando comprar o domínio

1. Na Vercel: projeto > **Settings > Domains** > adicione `www.seudominio.com.br` e `seudominio.com.br`.
2. A Vercel mostra os registros DNS (A e CNAME). Cadastre esses registros no painel onde o domínio foi comprado (Registro.br, por exemplo). O HTTPS é ativado sozinho.
3. Substitua os marcadores nos arquivos (busca e troca):

| Procurar | Trocar por | Arquivos |
|---|---|---|
| `SEUDOMINIO` | o domínio real | `index.html`, `robots.txt`, `sitemap.xml`, `politica-de-privacidade.html` |
| `[seudominio]` | o domínio real | `index.html` |
| `[CNPJ]` | CNPJ da empresa | `index.html` |
| `[RAZÃO SOCIAL]` e `[00.000.000/0000-00]` | razão social e CNPJ | `politica-de-privacidade.html` |
| `[data da publicação]` | data de publicação | `politica-de-privacidade.html` |

## Formulário de contato

O formulário não precisa de servidor: ao clicar em **Enviar pelo WhatsApp**, ele monta a mensagem com os dados preenchidos e abre o WhatsApp no número +55 31 99848-2077. Para trocar o número, procure `5531998482077` no `index.html`.

## Pendências antes da divulgação

- Razão social e CNPJ no rodapé e na política de privacidade.
- Domínio e e-mail comercial.
- Logos dos clientes (hoje os nomes aparecem em texto) e autorização de uso.
- Revisão jurídica da política de privacidade.
