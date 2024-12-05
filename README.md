Projeto Moderno com Webpack e Babel

Este projeto é uma estrutura básica para um aplicativo front-end moderno, utilizando ferramentas como Webpack, Babel, style-loader e css-loader. O objetivo é unificar todo o conhecimento adquirido em configuração de build e bundling.

Estrutura do Projeto 📁

.
├── dist/                # Arquivos de saída gerados pelo Webpack
├── src/                 # Código-fonte
│   ├── index.js         # Ponto de entrada principal do JavaScript
│   └── styles.css       # Arquivo de estilização
├── index.html           # Página HTML simples para teste
├── package.json         # Configurações do npm e scripts
├── webpack.config.js    # Configuração do Webpack
└── .babelrc             # Configuração do Babel

🚀 Funcionalidades

    Webpack para gerenciamento de módulos e criação de bundles.
    Babel para transpilar código ES6+ para compatibilidade com navegadores mais antigos.
    style-loader e css-loader para incorporar CSS ao JavaScript.
    Saída minificada no formato [name].min.js.

🛠️ Instalação

1. Clone o repositório:
    git clone https://github.com/devtauany-pereira/projeto-moderno.git
    cd projeto-moderno
2. Instale as dependências:
    npm install

📄 Configuração
Webpack (webpack.config.js)

//js
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: '[name].min.js',
    path: path.resolve(__dirname, 'dist'),
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: 'babel-loader',
      },
      {
        test: /\.css$/,
        use: ['style-loader', 'css-loader'],
      },
    ],
  },
  mode: 'production',
};

Babel (.babelrc)
//json
{
  "presets": ["@babel/preset-env"]
}

🔧 Scripts

No arquivo package.json, foi adicionado o script:

"scripts": {
  "build": "webpack"
}

Para compilar o projeto, execute:

npm run build

🌐 Testando o Projeto

Abra o arquivo index.html no navegador para visualizar a página e ver o JavaScript e CSS aplicados.
🛡️ Licença

Este projeto é licenciado sob a MIT License.
📫 Contato

Para dúvidas ou contribuições, entre em contato: [thauannymendes7@gmail.com]