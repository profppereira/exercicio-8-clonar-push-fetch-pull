# Exercício 8 - Clonar Push Fetch Pull

1. Crie um repositório no seu Github com o nome `exercicio-8-clonar-push-fetch-pull`.
2. Clone o recém criado repositório do Github para o seu computador.
3. Crie um novo arquivo chamado `index.html` (deixe-o vazio por enquanto).
4. Crie um novo arquivo chamado `script.js` (deixe-o vazio por enquanto).
5. Crie um novo arquivo chamado `style.css` (deixe-o vazio por enquanto).
6. Adicione e comite os arquivos vazios, com a mensagem "adicionar arquivos web vazios".
7. Imediatamente crie uma nova branch chamada `home-page` e outra branch chamada `about-me` (ambas baseadas na branch principal).
8. Ainda na branch main, faça um push dos commits para o seu Github, verifique no Github se o push enviou o commit com sucesso, observe também quantas branches têm no seu Github.
9. Mude para a branch `home-page` usando o comando "switch" para trocar de branch.
10. No arquivo `index.html`, adicione o seguinte:

```html
<!DOCTYPE html>
<html lang="pt-br">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Minha Página Inicial</title>
      <script src="script.js"></script>
      <link rel="stylesheet" href="style.css">
  </head>
  <body>
      <header>
          <h1>Minha Página Inicial</h1>
      </header>
      <div class="container">
          <h2>Bem-vindo à minha página inicial</h2>
          <p>Esta é minha home page.</p>
          <p>Exercícios de Git.</p>
          <button onclick="atualizarHora()">Mostrar Hora Atual</button>
          <p id="horaAtual"></p>
      </div>
  </body>
</html>

```

11. No arquivo `script.js`, adicione o seguinte:

```javascript
function atualizarHora() {
    var data = new Date();
    var hora = data.getHours();
    var minutos = data.getMinutes();
    var segundos = data.getSeconds();

    hora = hora < 10 ? '0' + hora : hora;
    minutos = minutos < 10 ? '0' + minutos : minutos;
    segundos = segundos < 10 ? '0' + segundos : segundos;

    document.getElementById('horaAtual').innerText = hora + ':' + minutos + ':' + segundos;
}

```

12. No arquivo `style.css`, adicione o seguinte:

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f2f2f2;
}
header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}
h1 {
    margin: 0;
}
.container {
    max-width: 800px;
    margin: auto;
    padding: 20px;
}
p {
    line-height: 1.6;
}

```

13. Adicione e comite as alterações, com a mensagem de commit "adicionar home page do meu website".
14. Ainda na branch `home-page`, faça um push dos commits para o seu Github, verifique no Github se o push enviou o commit com sucesso, observe também quantas branches têm no seu Github.
15. Mude para a branch `about-me` usando o comando "switch" para trocar de branch.
16. Crie um novo arquivo chamado `about.html`, e adicione exatamente o seguinte (não altere o texto da página):

```html
<!DOCTYPE html>
<html lang="pt-br">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Sobre Mim</title>
      <link rel="stylesheet" href="style.css">
  </head>
  <body>
      <header>
          <h1>Sobre Mim</h1>
      </header>
      <div class="container">
          <h2>Um pouco sobre mim</h2>
          <p>Meu nome é [Seu Nome]. Eu sou um [sua ocupação] interessado em [seus interesses].</p>
          <p>Eu gosto de [suas atividades favoritas] e estou interessado em aprender mais sobre [áreas de interesse].</p>
          <p>Sinta-se à vontade para entrar em contato comigo através do meu e-mail: [seu e-mail].</p>
      </div>
  </body>
</html>

```

17. Adicione e comite as alterações na branch `about-me` com a mensagem de commit "adicionar página sobre mim".
18. Ainda na branch `about-me`, faça um push dos commits para o seu Github, verifique no Github se o push enviou o commit com sucesso, observe também quantas branches têm no seu Github.
19. Pelo Github (use o navegador), na branch `about-me`, altere o arquivo `about.html`. Nesse arquivo, altere o texto da página substituindo tudo que estiver entre colchetes `[]`, por suas informações. Por exemplo, onde estiver `[Seu Nome]`, alterar pelo seu nome de fato, e assim sucessivamente. Commit pela interface do Github.
20. No terminal, faça um fetch para trazer as novas alterações do Github.
21. Olhe no git log em qual commit a referência para a branch remota `origin/about-me` está e a referência para a branch local `about-me` está.
22. Faça um merge entre a referência de branch remota `origin/about-me` com a branch `about-me`.
23. Pelo Github (use o navegador), na branch `home-page`, altere o arquivo `index.html`. Nesse arquivo, altere o texto `<h1>Minha Página Inicial</h1>` para seu nome. Por exemplo: `<h1>Maria Alice</h1>`. Commit pela interface do Github.
24. Mude para a branch `home-page` usando o comando "switch" para trocar de branch.
25. No terminal, faça um pull para trazer as novas alterações do Github.
26. Olhe no git log em qual commit a referência para a branch remota `origin/home-page` está e a referência para a branch local `home-page` está.
