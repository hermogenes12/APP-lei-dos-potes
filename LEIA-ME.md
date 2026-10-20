# Lei dos Potes - gerar o APK

Este pacote compila o app em APK usando o GitHub (gratuito). Voce nao precisa instalar nada no computador.

## Passo a passo

1. Crie uma conta em https://github.com (se ainda nao tiver).
2. Clique em **New repository**, de um nome (ex.: `lei-dos-potes`), deixe **Public** ou **Private** e crie.
3. No repositorio vazio, clique em **uploading an existing file**.
4. Extraia este ZIP e arraste TODO o conteudo da pasta para a pagina
   (incluindo a pasta `www`, o `package.json`, o `capacitor.config.json`, o `.gitignore` e a pasta `.github`).
   Atencao: a pasta `.github` e oculta em alguns sistemas. No Windows, ative "Itens ocultos" no Explorador de Arquivos.
   Se a pasta `.github` nao subir, crie o arquivo manualmente: **Add file > Create new file**, digite
   `.github/workflows/build-apk.yml` como nome e cole o conteudo do arquivo.
5. Clique em **Commit changes**.
6. Va na aba **Actions**. O fluxo "Gerar APK" comeca sozinho (leva uns 5 minutos).
   Se nao comecar, clique em "Gerar APK" > **Run workflow**.
7. Quando aparecer o check verde, abra a execucao e, no fim da pagina, em **Artifacts**,
   baixe `lei-dos-potes-apk` (vem em ZIP com o arquivo `app-debug.apk`).
8. Envie o APK para o celular, abra e instale. O Android vai pedir para permitir
   instalar de fontes desconhecidas: autorize para o app que voce usou para abrir o arquivo.

## Observacoes

- O APK gerado e do tipo "debug": instala normalmente, mas nao serve para publicar na Play Store.
- O app usa o icone padrao do Capacitor. Da para trocar depois.
- Os dados (salario e potes) ficam salvos no proprio aparelho.
- Para alterar o app, edite `www/index.html` no GitHub e salve: um novo APK sera gerado.
