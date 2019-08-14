# Iniciando aplicação NodeJS

**1.** Criar o arquivo package.json, através do seguinte comando:

`yarn init -y`

**2.** Adicionar o express:

`yarn add express`

- Criar dentro da pasta src, os arquivos [app.js](https://gist.github.com/lrohde/2c882edac662c2eb8ea64e4d3b0c8de1), [server.js](https://gist.github.com/lrohde/762551423217494c4c17142175270af4) e [routes.js](https://gist.github.com/lrohde/82fc2f7ac5b1e194e8be763a822adb46).

**3.** Adicionar o sucrase e o nodemon:

`yarn add sucrase nodemon -D`

- Criar o script dev e o arquivo [nodemon.json](https://gist.github.com/lrohde/fc02c20605728aca7a3889ffd030b560#file-nodemon-json).

## Ferramenta de Linting

**4.** Para padronização de código utiliza-se:

`yarn add eslint -D`<br />
`yarn eslint --init`

Selecionar as seguintes opções, respectivamente:

- To check sintax, find problems, ans enforce code style
- JavaScript module(import/export)
- None of these
- Node
- Use a popular style guide
- Airbnb
- JavaScript

**Obs:** Se o yarn estiver sendo utilizado, deve-se remover o package-lock.json e executar `yarn`novamente.

- O arquivo de configuração do vscode deve ter a extensão do eslint instalada e o arquivo de configuração deve seguir [este padrão](https://gist.github.com/lrohde/9c7b7a87f5a47972483f249f3f4e72fe).

**4.** É recomendado a utilização do prettier para autocorreção do código:

`yarn add prettier eslint-config-prettier eslint-plugin-prettier -D`

- Um arquivo [.eslintrc.js](https://gist.github.com/lrohde/abc4f6134229bbf4c6a9aaabe85285e1) será criado na raiz do projeto, algumas alterações serão necessárias. Elas podem ser encontradas [aqui](https://gist.github.com/lrohde/abc4f6134229bbf4c6a9aaabe85285e1). O arquivo [.prettierrc](https://gist.github.com/lrohde/c4f4d124a91550f196320a5463865363) também deve ser [criado](https://gist.github.com/lrohde/c4f4d124a91550f196320a5463865363).

**5.** Para finalizar as configurações de estilo, é necessário gerar o arquivo [.editorconfig](https://gist.github.com/lrohde/6ed14cd9447b1d0344e313819a754b8c).

## Adicionando ORM (Sequelize)

**6.** Para facilitar as operações de banco de dados utilizamos um ORM(Object-Relational Mapping):

- Para instalar com o módulo do MySQL e com a CLI:

  `yarn add sequelize mysql2`<br />
  `yarn add sequelize-cli -D`

- Deve-se criar os diretórios para migrations, seeds e models e então referenciá-los no arquivo [.sequelizerc](https://gist.github.com/lrohde/dd50303b8519e353599682985960ab44).

- É necessário também criar um loader para os models dentro da pasta database e importá-lo dentro app.js.

## Outras bibliotecas recomendadas

- Para autenticação JWT [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).
- Para criptografia de senha [bcryptjs](https://github.com/dcodeIO/bcrypt.js).
- Para manipulação de data [momentjs](https://github.com/moment/moment).
- Para requisições HTTP [axios](https://github.com/axios/axios).
- Para validação de dados [yup](https://github.com/jquense/yup).
