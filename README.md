
![cover](https://i.ibb.co/0yPYBjy/preview.png)

## :rocket: Principais funções

- [x] Layout storages
- [x] Edição de textos
- [x] Edição de layouts
- [x] Edição de categorias
- [x] Edição de configurações

## ✨ Foi utilizado

- [x] Node.js (Runtime)
- [x] Fastify (Framework web super rapido)
- [x] Prisma (ORM moderno para bancos de dados)
- [x] Typescript (Traz segurança e clareza ao código, oferecendo tipagem estática e um desenvolvimento mais robusto)
- [x] JSON Web Token (Autenticação)
- [x] BCrypt (Um forte mecanismo de hash para proteger senhas e dados sensíveis)
- [x] Zod (Oferece validação de dados rápida e flexível em TypeScript)
- [x] ETA (Uma alternativa EJS mais rápida, leve e configurável)


### 1. Configuracoes Iniciais:

```bash
sudo apt update
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs

```

```bash
npm install -g prisma
```

```bash
git clone https://github.com/fleetvpngit/PAINEL_DTUNNEL_MOD.git
```

```bash
cd PAINEL_DTUNNEL_MOD
```

Crie seu arquivo de variável ambiente `.env` na pasta do projeto.
Exemplo:

```cl
PORT=                // 3000
NODE_ENV=            // "production"
DATABASE_URL=        // "file:./database.db"
CSRF_SECRET=         //
JWT_SECRET_KEY=      //
JWT_SECRET_REFRESH=  //
```

`CSRF_SECRET`, `JWT_SECRET_KEY`, `JWT_SECRET_REFRESH` são chaves secretas sensíveis, ninguém além de você deve ter acesso a elas, para garantir a segurança do painel recomendo que utilizem este comando para gerar chaves privadas:

```js
node -e "console.log(require('crypto').randomBytes(256).toString('base64'));"
```

### 1. Instale as dependências:

```bash
npm install
```

### 2. Gerar artefactos do prisma

```bash
npx prisma generate
```

### 3. Crie as migrations do banco de dados

```bash
npx prisma migrate deploy
```

### 4. Rodando o projeto

```bash

screen -S paineldtunnel
npm run start
```

<br />
