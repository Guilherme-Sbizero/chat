# Projeto: Chat em Tempo Real

Um chat simples em tempo real, composto por um **backend WebSocket
(Node.js)** e um **frontend estático (HTML/CSS/JS)**.

## 📁 Estrutura do Projeto

    /
    ├── backend/        # Servidor WebSocket em Node.js
    └── frontend/       # Interface do usuário (HTML, CSS e JS)

## 🧩 Pré-requisitos

-   **Node.js** --- versão **14+** recomendada\
-   **npm** --- já incluso com o Node.js

## ⚙️ Instalação (Backend)

Abra um terminal e navegue até a pasta:

``` bash
cd backend
```

Instale as dependências:

``` bash
npm install
```

## 🔧 Variáveis de Ambiente

O backend usa a variável `PORTA_WS` para definir a porta do WebSocket.

Se não for configurada, o servidor usará **8080** por padrão.

Para alterar a porta:

Crie um arquivo `.env` dentro de **backend/**:

    PORTA_WS=3000

## ▶️ Executando o Backend

**Modo produção / simples:**

``` bash
npm start
```

**Modo desenvolvimento (auto-reload com `node --watch`):**

``` bash
npm run dev
```

O servidor WebSocket será iniciado na porta configurada\
(arquivo principal: `backend/src/server.js`).

## 💻 Executando o Frontend

O frontend é totalmente estático.

Você pode abrir o arquivo diretamente no navegador:

``` bash
Start-Process "frontend/index.html"
```

Ou usar extensões como **Live Server** (VS Code).

O frontend conecta em:

    ws://localhost:8080

Se mudar a porta do backend, atualize:

    frontend/js/script.js

ou configure `PORTA_WS=8080` no backend.

## 📝 Como Usar

1.  Inicie o backend\
2.  Abra `frontend/index.html` no navegador\
3.  Digite um nome e clique em **Entrar**\
4.  Envie mensagens --- elas serão distribuídas para todos os clientes
    conectados

## 📦 Dependências (Backend)

-   **ws** --- servidor WebSocket\
-   **dotenv** --- leitura de variáveis de ambiente `.env`

## 📂 Estrutura de Arquivos (Resumo)

    backend/
    │ package.json     # Scripts e dependências
    └ src/
      └ server.js      # Lógica do servidor WebSocket

    frontend/
    │ index.html       # Interface principal
    ├ css/styles.css   # Estilos do chat
    └ js/script.js     # Lógica do cliente + WebSocket

## 📄 Licença

`MIT LICENSE`.
