# Projeto - Microsserviços com Docker

Este repositório contém a estrutura de microsserviços utilizados na aplicação, com configuração de containers Docker para facilitar o ambiente de desenvolvimento e testes.

## 📁 Estrutura

```
/
├── docker/
│   └── docker-compose.yml  # Arquivo de configuração dos containers
├── ms-usuario/              # Microsserviço de usuários
├── ms-login/                # Microsserviço de login
├── ms-cardapio/             # Microsserviço de cardápio
└── README.md
```

## 🐳 Executando com Docker

Certifique-se de que o Docker esteja instalado e rodando na sua máquina.

Para subir todos os serviços definidos no `docker-compose`, execute o seguinte comando no terminal, a partir da raiz do projeto:

```bash
docker-compose -f docker/docker-compose.yml up --build
```

Para derrubar os containers:

```bash
docker-compose -f docker/docker-compose.yml down
```

## ⚙️ Serviços inclusos

- MySQL (como banco de dados compartilhado entre os microsserviços)
- Microsserviços: `ms-usuario`, `ms-login`, `ms-cardapio`

## 🧪 Testes

Os microsserviços possuem testes unitários e de integração. Recomendado utilizar Maven/Gradle para executar localmente:

```bash
# Exemplo com Maven
cd ms-usuario
./mvnw test
```

## 📦 Requisitos

- Docker e Docker Compose
- Java 17+ (para rodar localmente os serviços)
- Maven ou Gradle (opcional)

## ✍️ Autor

Este projeto é mantido por [Seu Nome Aqui].
