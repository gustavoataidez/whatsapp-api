# WhatsApp API Node.js

Esta API permite controlar funções do WhatsApp através de uma interface RESTful. Ela é baseada na biblioteca Baileys e pode ser usada para criar bots de atendimento, chats multiserviços ou qualquer outro sistema que utilize o WhatsApp.

---

## Pré-requisitos

- Docker
- Node.js (versão 20)
- PM2 (opcional, para gerenciamento de processos)

---

## Instalação

1. **Instale o Docker:**

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ${USER}
```

2. **Instale o Node.js usando NVM:**

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
nvm install 20
```

3. **Instale o PM2 globalmente:**

```bash
npm i -g pm2
```

4. **Clone o repositório e instale as dependências:**

```bash
git clone https://github.com/code-chat-br/whatsapp-api.git
cd whatsapp-api
npm install
```

5. **Configure as variáveis de ambiente:**
   
Copie o arquivo .env.dev para .env e ajuste as configurações necessárias:
```bash
cp .env.dev .env
```
   
7. **Configure o banco de dados:**

Execute o script para configurar o banco de dados com o Prisma ORM:
```
bash deploy_db.sh
```

## Executando a API

**Modo de desenvolvimento:**
```
npm run start:dev
```
**Modo de produção:**
```
npm run start:prod
```
**Usando PM2:**
```
pm2 start 'npm run start:prod' --name WhatsApp_API
```


## Docker 

**Se preferir, você pode rodar a API usando Docker:**
```
docker-compose up
```

## Documentação da API
```
[docker-compose up](http://localhost:8085/docs)
```

## Webhooks

A API suporta webhooks para notificações em tempo real sobre eventos como recebimento de mensagens, atualizações de status, etc. Consulte a documentação para mais detalhes.


## Nota 

Este projeto não é afiliado ao WhatsApp. Use por sua conta e risco. Não utilize para spam.
