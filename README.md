# Laboratório_Docker-Portainer - criado por Araken Neto

# 🚀 Projeto Docker + Docker Compose

Este projeto demonstra como configurar e executar uma aplicação com múltiplos serviços usando Docker e Docker Compose. Ele inclui:

- 📦 API simulada com `json-server`
- 💻 Frontend em React
- 🛠️ Interface de gerenciamento com Portainer

---

## 📁 Estrutura do Projeto

├── api-alurabooks/ # API fake com json-server 

├── curso-react-alurabooks/ # Frontend React 

├── COMPOSES/ │ 
  └── docker-compose.yml # Arquivo principal do Docker Compose 
  
└── README.md


---

## 🐳 Pré-requisitos

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- Git (opcional, para clonar o projeto)

---

## ⚙️ Etapas para executar o projeto

### 1. Clonar o repositório

```bash
git clone git@github.com:Araken13/Projeto_Docker-Pontainer.git
cd Projeto_Docker-Pontainer

# 2. Subir os containers com Docker Compose

docker compose -f COMPOSES/docker-compose.yml up --build -d

# Isso irá:

Construir as imagens da API e do frontend

Subir os serviços em segundo plano

Expor as portas 8000 (API), 3000 (Frontend), 9000/9443 (Portainer)

🔍 Acessos
API: http://localhost:8000/public/registrar

Frontend: http://localhost:3000

Portainer: http://localhost:9000

🧹 Limpeza do ambiente (opcional)
Para remover containers, imagens e volumes não utilizados:

bash
docker system prune -a --volumes

🛠️ Comandos úteis
Parar os serviços:

bash
docker compose down
Reconstruir tudo:

bash
docker compose up --build -d

#Ver logs:

bash
docker compose logs api
docker compose logs frontend

📦 Volumes e persistência
O volume portainer_data é usado para manter os dados do Portainer.

Os diretórios api-alurabooks e curso-react-alurabooks são montados como volumes para facilitar o desenvolvimento.

🤝 Contribuições
Sinta-se à vontade para abrir issues ou pull requests. Sugestões são bem-vindas!

📄 Licença
Este projeto está sob a licença ISC.

