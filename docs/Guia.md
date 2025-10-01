## 🚀 Como Rodar o Projeto

Siga os passos abaixo para configurar e rodar o projeto em ambiente de desenvolvimento.

### 1. Clone o Repositório

```bash
git clone [https://github.com/FR0M-ZER0/Nimbus.git](https://github.com/FR0M-ZER0/Nimbus.git)
cd nome-do-repositorio
```

### 2. Configurando o Backend

```bash
# Navegue para a pasta do backend
cd back

# Instale as dependências
npm install

# Crie uma cópia do arquivo de variáveis de ambiente
cp .env.example .env
```

Agora, abra o arquivo `.env` e preencha com as suas credenciais:

```env
# URL de conexão com o banco de dados
DATABASE_URL="postgresql://USUARIO:SENHA@HOST:PORTA/NOME_DO_BANCO"

# Porta em que o servidor irá rodar
PORT=3333

# Chave secreta para JWT
JWT_SECRET="SUA_CHAVE_SECRETA_AQUI"
```

Depois de configurar o `.env`, rode as migrações do banco de dados:

```bash
# Este comando irá criar as tabelas no seu banco
npx prisma migrate dev
```

Para iniciar o servidor backend:

```bash
npm run dev
```

### 3. Configurando o Frontend

```bash
# Volte para a raiz do projeto e navegue para a pasta do frontend
cd ../front

# Instale as dependências
npm install

# Crie uma cópia do arquivo de variáveis de ambiente
cp .env.example .env.local
```

Abra o arquivo `.env.local` e configure a URL da API:

```env
# URL base do seu backend
VITE_API_URL=http://localhost:3333
```

Para iniciar a aplicação frontend:

```bash
npm run dev
```

Pronto! Agora você pode acessar `http://localhost:5173` (ou a porta indicada pelo Vite) no seu navegador.
