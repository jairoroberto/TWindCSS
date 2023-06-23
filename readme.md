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
- Crie uma pasta `src/` e arquivo `styles.css` nesta pasta.
- Insere este código da lib no `styles.css`:
```CSS
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
@tailwind base;
@tailwind components;
@tailwind utilities;


### Passo 06:
// Gerando o arquivo de saída: Este comando eu coloquei direto no `package.json`
```sh
npx tailwindcss build styles.css -o src/css/styles.css
```

### Passo Complementar:
##### Se você uso o `package.json` basta executar o comando:
// Gerando o arquivo de saída: 
```sh
npm run dev
```

### Passo Complementar:
##### Este é comando para gerar o arquivo de prod - mas não precisa usar por enquanto.
```sh
NODE_ENV=production npx tailwindcss-cli@latest build ./src/geral.scss -o ./src/styles.css
```
