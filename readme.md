# TailwinCSS
[![N|Solid](https://www.devonblog.com/wp-content/uploads/2022/06/tailwind-thumb.jpg)](https://tailwindcss.com/docs/installation)
### Dependencias Iniciais
@tailwind base
@tailwind components;
@tailwind utilities


### Passo 01:
// Crie o arquivo package.json
```sh
npm init -y
```

### Passo 02:
// Instalando o TailwindCSS
```sh
npm install tailwindcss
```

### Passo 03:
// Autoprefixer is a PostCSS plugin which parses your CSS and adds vendor prefixes
```sh
npm install autoprefixer
```

### Passo 04:
// Criando o tailwind.config.js, obs.: npx=package runner, o npm=package instaler
```sh
npx tailwindcss init
```

### Passo 05:
##### Antes de geração do arquivo no passo 06, crie o styles.css (Source) dentro do VSCode 
- Crie uma pasta `src/` e depois crie um arquivo `styles.css` dentro.
- Insere este código da lib no `styles.css`:
```CSS
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Passo 06:
// Gerando o arquivo de saída: Este comando eu coloquei direto no `package.json`
```sh
npx tailwindcss build styles.css -o src/css/styles.css
```

### Passo Complementar:
##### Se você colocou os prompts de comando na parte de scripts do `package.json` basta executar o comando:

//Exemplo do package.json
```Javascript
{
  "name": "tw",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "npx tailwindcss build ./src/styles.css -o css/styles.css --watch"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "autoprefixer": "^10.4.14",
    "tailwindcss": "^3.3.2"
  }
}
```
// Gerando o arquivo de saída: 
```sh
npm run dev
```

### Passo Complementar:
##### Este é comando para gerar o arquivo de prod minificando ainda mais o arquivo de css
// Importante: Antes de executar o comando abaixo, você precisa fazer uma mudança no arquivo de config do Tailwind chamado `tailwind.config.js`
colocando o `purge: ["index.html"]` para gerar para produção olhando o(s) arquivo que será assistido. Veja o exemplo deste config:

- Obs: Algumas mudanças ocorreram, pode haver ajuste neste passo para geração de prod, qualquer dúvida acessar documentação do TailWind ...
```Javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  purge: ["index.html"],
  content: [
    '*.html',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
```sh
NODE_ENV=production npx tailwindcss-cli@latest build ./src/styles.css -o ./css/styles.min.css --minify
```
