# Trabalho-de-Testes

Bem-vindo ao repositório do projeto. Este documento fornece as instruções necessárias para configurar o ambiente, executar a aplicação (Backend e Frontend) da DoaSô e rodar os testes automatizados.

# Como rodar a DoaSô:

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:

* [Node.js](https://nodejs.org/) (v14 ou superior)
* [MySQL](https://www.mysql.com/) (Banco de dados)
* [VS Code](https://code.visualstudio.com/) (Editor de código)
* Extensão **Live Server** para o VS Code (para rodar o frontend)

---

## 🚀 Instalação e Configuração

### 1. Clonar e Instalar Dependências
Abra o terminal na pasta raiz do projeto e execute o comando abaixo para instalar as bibliotecas necessárias (Express, Jest, Supertest, MySQL, etc.):

```bash
npm install
```

## 2. Configuração do Banco de Dados
Certifique-se de que o seu serviço MySQL está rodando.

Verifique o arquivo connection_mysql.js (ou similar) na raiz do projeto para confirmar se as credenciais (usuário, senha, host) correspondem à sua configuração local.

Execute o script SQL de criação do banco de dados (se houver) no seu gerenciador MySQL (Workbench, DBeaver, etc.) para criar as tabelas necessárias (Doador, Centro_de_doacao, Usuario, etc.).

## ▶️ Como Rodar o Projeto
O projeto é dividido em Backend (API) e Frontend (Telas). Siga a ordem abaixo:

Passo 1: Iniciar o Backend (API)
No terminal, dentro da pasta do back projeto, inicie o servidor Node:

```Bash
npm install
node index.js
```
Se tudo estiver correto, você verá a mensagem:

```Bash
Server is running on 3307
```
A API ficará disponível em: http://localhost:3307

## Passo 2: Iniciar o Frontend (Live Server)
Para visualizar as telas do projeto:

Abra o projeto no VS Code.

Navegue até a pasta onde estão os arquivos HTML (ex: src/front ou na raiz).

Clique com o botão direito no arquivo index.html (ou na tela de login/inicial).

Selecione a opção "Open with Live Server".

O navegador abrirá automaticamente exibindo a aplicação.

🧪 Testes Automatizados (Jest)
Este projeto utiliza Jest e Supertest para garantir que as rotas da API (GET, POST, PUT, DELETE) estejam funcionando corretamente.

Para rodar os testes:
Certifique-se de que o MySQL está rodando, pois os testes realizam conexões reais com o banco. Em seguida, no terminal, execute:

```Bash

npm test
```
O que esperar:
O terminal exibirá o resultado de cada suíte de testes (Doadores, Centros, Metas, Propostas), indicando quais passaram (PASS) e quais falharam (FAIL).

Exemplo de saída:

```Plaintext

 PASS  ./index.test.js
  Testes das Rotas de Doadores
    ✓ GET /api/doador - deve retornar lista de doadores (50ms)
    ✓ POST /api/doador - deve criar um novo doador (120ms)
```
🛠️ Tecnologias Utilizadas
Node.js & Express: Servidor Backend.

MySQL: Banco de dados relacional.

Jest & Supertest: Testes de integração.

HTML/CSS/JS: Frontend.