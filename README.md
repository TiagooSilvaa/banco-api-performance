# Banco API - Testes de Performance com K6

## 📌 Introdução

Este repositório contém testes de performance desenvolvidos em **JavaScript** utilizando o **K6**, com o objetivo de avaliar o desempenho da API do projeto *Banco API*.

Os testes simulam cenários reais de uso, como autenticação e transferências, permitindo identificar gargalos, medir tempos de resposta e analisar a estabilidade da aplicação sob carga.

---

## 🛠️ Tecnologias Utilizadas

- **JavaScript (ES6+)**
- **K6** – ferramenta para testes de carga e performance
- **Node.js** (opcional, para suporte ao projeto)
- Variáveis de ambiente para configuração dinâmica (ex: `BASE_URL`)

---

## 📁 Estrutura do Repositório

banco-api-performance/
├── fixtures/             # Dados de entrada para testes (ex: usuário, payloads)
├── helpers/              # Funções auxiliares (ex: autenticação)
├── tests/                # Scripts de testes de performance
├── utils/                # Funções utilitárias reutilizáveis
├── config/               # Arquivos de configuração de variáreis de ambiente
├── package.json          # Dependências (opcional)
└── README.md             # Documentação do projeto

---

## 🎯 Objetivo de Cada Grupo de Arquivos

### fixtures/
Dados de entrada para testes (ex: usuário, payloads)

### helpers/
Funções auxiliares (ex: autenticação)

### tests/
Contém os cenários de teste:
- Execução de fluxos da API (login, transferências, etc.)
- Simulação de carga com múltiplos usuários (VUs)
- Validação das respostas da API

### utils/
Funções utilitárias reutilizáveis

### config/
Arquivos de configuração de variáreis de ambiente

### package.json
(Se utilizado)
- Gerenciamento de dependências
- Scripts auxiliares do projeto

---

## ⚙️ Instalação

### 1. Clonar o repositório

git clone https://github.com/TiagooSilvaa/banco-api-performance.git
cd banco-api-performance

---

### 2. Instalar o K6

Windows (via Chocolatey):
choco install k6

---

## ▶️ Execução do Projeto

### Variável de ambiente obrigatória

BASA_URL

Exemplo:
set BASE_URL=http://localhost:3000

---

### Execução básica

k6 run tests/login.test.js

---

### Execução com dashboard em tempo real + exportação

set K6_WEB_DASHBOARD=true&& set K6_WEB_DASHBOARD_EXPORT=html-report.html&& k6 run tests/login.test.js

---

## 👨‍💻 Autor

Tiago Silva Lima
https://github.com/TiagooSilvaa/banco-api-performance
