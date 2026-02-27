## 🏙️ Bot Comunidade SP - Watson & Node-RED

Este repositório contém a solução completa de um assistente virtual inteligente voltado para serviços públicos da cidade de São Paulo. A arquitetura combina o poder de processamento de linguagem natural (NLP) do **IBM Watson** com a flexibilidade de integração do **Node-RED**.

---

## 🏗️ Arquitetura da Solução

O projeto é dividido em dois componentes principais:

1.  **Skill de IA (Watson Assistant):** O arquivo JSON da Skill contém o treinamento de intenções (#), entidades (@) e a árvore de diálogo que define a "personalidade" e o conhecimento do bot.
2.  **Fluxo de Integração (Node-RED):** O arquivo JSON do fluxo atua como o middleware, conectando a API do **Telegram** ao motor de IA da IBM Cloud.

---

## 🚀 Funcionalidades

O assistente está pronto para fornecer informações sobre:
* **Mobilidade:** Status em tempo real de Metrô e CPTM.
* **Saúde:** Cronogramas de vacinação e busca por UBS.
* **Social:** Localização de Centros de Acolhida e Bibliotecas.
* **Clima:** Previsão do tempo para a capital paulista.
* **Trânsito:** Situação das principais vias (Marginais, Av. Paulista, etc).

---

## 🛠️ Como Instalar

### 1. Inteligência (IBM Watson)
* Crie uma instância do **Watson Assistant** na IBM Cloud.
* Importe o arquivo da Skill (`skill-comunidade-sp.json`).
* Copie a **API Key** e o **Assistant ID** na aba "Settings".

### 2. Conectividade (Node-RED)
* Importe o arquivo de fluxo (`flow-nodered.json`).
* Instale as dependências via "Manage Palette":
    * `node-red-contrib-telegrambot`
    * `node-red-node-watson`
* Configure o nó do Telegram com seu **Token** (obtido via @BotFather).
* Configure o nó do Watson com suas credenciais da IBM Cloud.

---

## 📋 Resumo Técnico
> Sistema de chatbot integrado para serviços públicos de São Paulo. Utiliza **IBM Watson** para processamento de linguagem natural e **Node-RED** como middleware para integração com **Telegram**. Automatiza consultas sobre transporte, saúde (vacinas/UBS) e trânsito, utilizando lógica de entidades e fluxos dinâmicos de resposta.

---

## 🔗 Fluxo de Dados
`Usuário (Telegram)` ➔ `Node-RED` ➔ `IBM Watson NLP` ➔ `Node-RED` ➔ `Resposta (Telegram)`

---
**Desenvolvido para fins educacionais.** ☕🏙️
