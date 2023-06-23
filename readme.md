# TailwinCSS
[![N|Solid](https://www.devonblog.com/wp-content/uploads/2022/06/tailwind-thumb.jpg)](https://tailwindcss.com/docs/installation)
### Dependencias Iniciais
@tailwind base
@tailwind components;
@tailwind utilities

### Passo 01:
```sh
// Crie o arquivo package.json
npm init -y
```

### Passo 02:
```sh
// Instalando o TailwindCSS
npm install tailwindcss
```

### Passo 03:
```sh
// Autoprefixer is a PostCSS plugin which parses your CSS and adds vendor prefixes
npm install autoprefixer
```

### Passo 04:
```sh
// Criando o tailwind.config.js, obs.: npx=package runner, o npm=package instaler
npx tailwindcss init
```

### Passo 05:
##### Antes de gerar o arquivo no passo 06, crie ele dentro do VSCode 
- Crie uma pasta `src/` e arquivo `styles.css` nesta pasta.
- Insere este código da lib no `styles.css`:
`
@tailwind base;\n
@tailwind components;
@tailwind utilities;
`



### Passo 06:
```sh
// Gerando o arquivo de saída: Este comando eu coloquei direto no `package.json`
npx tailwindcss build styles.css -o src/css/styles.css
```


### Passo Complementar:
##### Se você uso o `package.json` basta executar o comando:
```sh
// Gerando o arquivo de saída: 
npm run start
```

### Passo Complementar:
##### Este é comando para gerar o arquivo de prod - mas não precisa usar por enquanto.
`NODE_ENV=production npx tailwindcss-cli@latest build ./src/geral.scss -o ./src/styles.css`

