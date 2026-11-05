# Site do unidosccristo

Páginas estáticas para a homepage, a Política de Privacidade e os Termos de Uso
do aplicativo. Não há dependências, build ou JavaScript.

## Antes de publicar

1. Confira o e-mail de contato `unidosccristo@hotmail.com` nos três arquivos HTML.
2. Revise o nome do aplicativo `unidosccristo` e os textos.
3. Não copie `.env`, `client_secret*.json` ou qualquer credencial para este site.

## Publicar no GitHub Pages

O caminho mais simples é criar um repositório chamado `unidosccristo.github.io`.
Assim o site fica na raiz de `https://unidosccristo.github.io/`.

1. Crie o repositório público `unidosccristo.github.io`.
2. Envie o conteúdo desta pasta `site/` para a raiz do repositório.
3. No GitHub, abra **Settings > Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/(root)`. Salve.
6. Aguarde a publicação e abra `https://unidosccristo.github.io/`.

Também é possível usar um repositório comum, mas o site ficará em
`https://unidosccristo.github.io/NOME_DO_REPOSITORIO/`. Nesse caso, o domínio
autorizado continua sendo `unidosccristo.github.io`, sem caminho.

## Configurar no Google Cloud

Depois que o site estiver no ar:

1. Abra o projeto `unidosccristo` no Google Cloud.
2. Verifique `unidosccristo.github.io` no Google Search Console.
   - Para um site na raiz, use a verificação por arquivo HTML ou pelo método
     disponível para o domínio.
   - Para um site em subpasta, verifique a propriedade de prefixo de URL
     correspondente.
3. Em **Google Auth Platform > Branding**, preencha:
   - **Homepage:** `https://unidosccristo.github.io/`
   - **Privacy policy:** `https://unidosccristo.github.io/privacidade.html`
   - **Terms of service:** `https://unidosccristo.github.io/termos.html`
   - **Authorized domain:** `unidosccristo.github.io`
4. Salve e publique o app em **Audience > Publish app**.
5. Depois de publicar, adicione `YOUTUBE_APP_TESTING=0` ao `.env`, rode
   `uv run python scripts/autorizar_youtube.py` e reinicie a interface.

O domínio autorizado deve ser informado sem `https://`, sem barra e sem caminho.
Se o Google recusar `unidosccristo.github.io`, use um domínio próprio apontado para
o GitHub Pages e verifique esse domínio no Search Console.

## URLs esperadas

- `https://unidosccristo.github.io/`
- `https://unidosccristo.github.io/privacidade.html`
- `https://unidosccristo.github.io/termos.html`
