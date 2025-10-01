## 🚀 Como Rodar a API

Siga os passos abaixo para clonar o repositório, inicializar os submódulos e configurar o ambiente de desenvolvimento da `Api`.

### 1. Clone o Repositório e os Submódulos

Use o comando a seguir com a flag `--recurse-submodules` para clonar o repositório principal e baixar o conteúdo de todos os submódulos (`Api`, `DataGetter`, etc.) de uma só vez.

```bash
git clone --recurse-submodules [https://github.com/FR0M-ZER0/Nimbus.git](https://github.com/FR0M-ZER0/Nimbus.git)
cd Nimbus
```

**Caso já tenha clonado o projeto sem a flag**, use os comandos abaixo para inicializar os submódulos:
```bash
git submodule init
git submodule update
```

### 2. Configurando a API (`/Api`)

Agora, vamos preparar e rodar o servidor backend.

```bash
# Navegue para a pasta do submódulo da API
cd Api

# Instale todas as dependências do backend
npm install

# Crie o arquivo de variáveis de ambiente a partir do exemplo
# (Se o seu arquivo de exemplo tiver outro nome, ajuste o comando)
cp .env.example .env
```

Abra o arquivo `.env` que você acabou de criar e preencha com as suas credenciais:

```env
# URL de conexão com o seu banco de dados
DATABASE_URL="postgresql://USUARIO:SENHA@HOST:PORTA/NOME_DO_BANCO"

# Porta onde o servidor irá rodar
PORT=3333

# Chave secreta para a geração de tokens de autenticação
JWT_SECRET="COLOQUE_UMA_CHAVE_SECRETA_BEM_FORTE_AQUI"
```

Com o `.env` configurado, aplique as migrações do Prisma para criar a estrutura no banco de dados:

```bash
npx prisma migrate dev
```

Finalmente, inicie o servidor da `Api` em modo de desenvolvimento:

```bash
# O nodemon irá reiniciar o servidor automaticamente a cada alteração
npm run dev
```
Pronto! O servidor da API estará rodando em `http://localhost:3333` (ou na porta que você definiu).
