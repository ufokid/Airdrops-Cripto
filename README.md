# Airdrops Cripto 🚀

Plataforma de gerenciamento de airdrops e distribuição de tokens de criptomoedas. Projeto construído com **Ruby on Rails** e inspirado na interface de **holder.io**.

## 📋 Sobre o Projeto

Airdrops Cripto é uma aplicação web moderna para gerenciar, acompanhar e distribuir airdrops de criptomoedas. Oferece uma interface intuitiva similar ao holder.io, com funcionalidades de blockchain integradas.

### Features Principais

- 🪙 Gerenciamento de airdrops e tokens
- 📊 Dashboard com métricas em tempo real
- 🔐 Autenticação segura com JWT
- ⛓️ Integração com blockchain (Ethereum, Bitcoin)
- 📱 Interface responsiva (React + Bootstrap)
- 🔄 Processamento assíncrono com Sidekiq
- 📈 Relatórios e análises
- 🌐 API RESTful

## 🛠️ Tecnologias

### Backend
- **Ruby on Rails 7.0**
- **PostgreSQL** - Banco de dados
- **Redis** - Cache e fila de jobs
- **Sidekiq** - Processamento assíncrono
- **JWT** - Autenticação
- **Web3.rb** - Integração com blockchain

### Frontend
- **React** - Interface de usuário
- **Webpacker** - Asset bundling
- **Bootstrap** - Framework CSS
- **Vite** - Build tool moderno

### Blockchain
- **Ethereum (ETH)** - Via Alchemy RPC
- **Bitcoin (BTC)** - Via GetBlock API
- **Web3.js** - Interação com smart contracts

## 🚀 Quick Start

### Com GitHub Codespaces (Recomendado)

1. Clique no botão **"Code"** no repositório
2. Selecione **"Codespaces"** → **"Create codespace on main"**
3. Aguarde o container ser criado (2-3 minutos)
4. O terminal automaticamente executará:
   ```bash
   bundle install
   rails db:create db:migrate
   ```

5. Inicie o servidor:
   ```bash
   rails server
   ```

6. Acesse em `http://localhost:3000`

### Localmente

#### Pré-requisitos
- Ruby 3.2.0+
- PostgreSQL 12+
- Redis 6+
- Node.js 18+

#### Instalação

```bash
# Clone o repositório
git clone https://github.com/ufokid/Airdrops-Cripto.git
cd Airdrops-Cripto

# Configure as variáveis de ambiente
cp .env.example .env
# Edite .env com suas chaves de API

# Instale dependências
bundle install

# Configure o banco de dados
rails db:create db:migrate

# Instale assets
rails webpacker:install

# Inicie o servidor
rails server
```

## 📝 Estrutura do Projeto

```
Airdrops-Cripto/
├── .devcontainer/           # Configuração do Codespace
│   └── devcontainer.json
├── app/
│   ├── controllers/        # Controladores Rails
│   ├── models/             # Modelos e lógica de negócio
│   ├── views/              # Templates ERB
│   ├── javascript/         # Componentes React
│   └── assets/
├── config/                 # Configurações da aplicação
├── db/
│   ├── migrate/            # Migrações do banco
│   └── schema.rb
├── lib/                    # Código reutilizável
├── spec/                   # Testes RSpec
├── Gemfile                 # Dependências Ruby
├── Gemfile.lock
├── .env.example            # Variáveis de ambiente exemplo
└── README.md               # Este arquivo
```

## 🔧 Configuração do Ambiente

### Variáveis de Ambiente Importantes

Copie `.env.example` para `.env` e configure:

```bash
# Blockchain RPC URLs
ETH_RPC_URL=https://eth-mainnet.g.alchemy.com/v2/YOUR_KEY
BTC_API_KEY=your_bitcoin_api_key

# Web3 Infura
WEB3_INFURA_PROJECT_ID=your_project_id

# AWS S3 (para uploads)
AWS_ACCESS_KEY_ID=your_key
AWS_SECRET_ACCESS_KEY=your_secret

# Sentry (monitoramento)
SENTRY_DSN=your_dsn
```

## 🗄️ Banco de Dados

### Executar migrações

```bash
# Criar banco
rails db:create

# Executar migrações
rails db:migrate

# Popular dados de teste (seed)
rails db:seed
```

### Resetar banco

```bash
rails db:reset  # Drop + Create + Migrate + Seed
```

## 🧪 Testes

```bash
# Executar todos os testes
rspec

# Testes específicos
rspec spec/models/
rspec spec/controllers/

# Com cobertura
rspec --coverage
```

## 📚 API Documentation

### Endpoints Principais

```
GET    /api/v1/airdrops          # Listar airdrops
POST   /api/v1/airdrops          # Criar airdrop
GET    /api/v1/airdrops/:id      # Detalhes do airdrop
PUT    /api/v1/airdrops/:id      # Atualizar airdrop
DELETE /api/v1/airdrops/:id      # Deletar airdrop

GET    /api/v1/tokens            # Listar tokens
POST   /api/v1/tokens            # Criar token
GET    /api/v1/tokens/:id        # Detalhes do token

POST   /api/v1/auth/login        # Login
POST   /api/v1/auth/logout       # Logout
```

## 🔐 Autenticação

A API usa **JWT tokens**. Incluir no header:

```bash
Authorization: Bearer YOUR_JWT_TOKEN
```

## 🚢 Deployment

### Deploy no Heroku

```bash
# Instalar Heroku CLI
heroku login

# Criar app
heroku create airdrops-cripto

# Configurar variáveis
heroku config:set RAILS_ENV=production
heroku config:set JWT_SECRET=your_secret

# Deploy
git push heroku main

# Migrations
heroku run rails db:migrate
```

## 📝 Logs e Debugging

```bash
# Logs em desenvolvimento
rails log:clear

# Console Rails
rails console

# Debugger
bundler exec pry  # ou byebug nos testes
```

## 🤝 Contribuindo

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está licenciado sob a MIT License - veja o arquivo LICENSE para detalhes.

## 💡 Ideias Futuras

- [ ] Suporte a mais blockchains (Solana, Polygon, etc)
- [ ] Dashboard mobile nativo
- [ ] Sistema de notificações (Push, Email)
- [ ] Análise avançada de dados
- [ ] Marketplace de airdrops
- [ ] Integração com DEX
- [ ] Smart contracts personalizados

## 📞 Contato

- GitHub: [@ufokid](https://github.com/ufokid)
- Issues: [Abra uma issue](https://github.com/ufokid/Airdrops-Cripto/issues)

---

⭐ Se você achou este projeto útil, considere dar uma estrela!
