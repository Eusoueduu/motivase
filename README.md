# Motive-se — landing page

Landing page institucional em HTML, CSS e JavaScript puros. Não exige instalação, compilação, CDN ou dependências de JavaScript. O logotipo está em `assets/logo-motive-se.jpeg`; a fonte Lexend está incluída em `assets/fonts/` com sua licença.

## Prévia local

Abra `index.html` no navegador. Se preferir um servidor local, execute `python3 -m http.server 8000` dentro desta pasta e acesse `http://localhost:8000`.

## Como colocar suas fotos

Os blocos com o texto “Troque este espaço por uma imagem sua” são áreas reservadas para fotos próprias. Em `index.html`, localize o espaço correspondente (hero, Carla França ou iniciativas), mantenha a tag externa `<figure class="photo-frame ...">` para preservar o recorte visual e substitua o conteúdo interno pelos elementos abaixo. Remova do `<figure>` o atributo `role="img"` e o `aria-label` do espaço reservado, pois agora o texto alternativo da foto será lido:

```html
<img class="photo-image" src="assets/aula-de-libras.jpg" alt="Descrição objetiva da foto" loading="lazy">
```

Coloque a foto em `assets/`, use uma descrição objetiva em `alt` e, para imagens de estudantes e participantes, confirme que elas podem ser publicadas. Se renomear a imagem, atualize o caminho no HTML. O logotipo pode ser substituído mantendo o nome `assets/logo-motive-se.jpeg`.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub. Para a página de usuário/organização, use o formato `usuario.github.io`; para um site de projeto, qualquer nome é aceito.
2. Envie para a raiz do repositório `index.html`, `style.css`, `script.js`, `manus-routes.json`, `README.md` e a pasta `assets/` com logotipo, fonte e fotos.
3. No GitHub, abra **Settings → Pages**. Em **Build and deployment**, selecione **Deploy from a branch**, escolha a branch `main` e a pasta `/(root)`; salve.
4. Aguarde a publicação e use o endereço que aparecer em **Settings → Pages**.

A página usa caminhos relativos (`style.css`, `script.js` e `assets/...`) e funciona tanto em domínio próprio quanto em URL de projeto do GitHub Pages. Não renomeie os arquivos sem atualizar os caminhos no `index.html`.
