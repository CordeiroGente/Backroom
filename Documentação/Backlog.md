
# [Backroom](https://github.com/CordeiroGente/Backroom/blob/main/README.md) - Product Backlog

> Sistema de gestão empresarial customizável com foco em front-end e suporte técnico contínuo

## 📋 Visão Geral

Este repositório contém o backlog de desenvolvimento dos produtos Backroom, organizados por prioridade e status de desenvolvimento. Nosso objetivo é entregar sistemas de gestão local altamente customizáveis com interfaces modernas e intuitivas.

## 💡 Problema

Empresas estão pagando o preço da desorganização digital
Você sabia que empresas perdem até 30% da produtividade por falta de gestão estruturada? Um exemplo sendo a necessidade de equipe de alterna entre diversos apps desconexos, como: Teams para organização de tarefas, Whatsapp para mensagens e Meet para videochamadas

Os números são gritantes, empresas tem um problema que ainda não tem solução

- 📊 44% das empresas relatam atrasos em projetos por falhas de comunicação
- 💰 18% perderam vendas devido à falta de alinhamento interno
- ⏰ 30% do tempo da equipe é desperdiçado com retrabalho e busca por informações

Assim nasceu a ideia da Backroom, pela necessidade. Nós oferecemos uma solução simples, desenvolvimento personalizado. Transforme as estatísticas apresentadas em coisas do passado.

# 📋 Product Backlog - Ecossistema Backroom

Este documento detalha o backlog priorizado para todos os produtos do ecossistema "Backroom". O backlog é dividido por produto e prioridade para guiar o desenvolvimento do PIM (Projeto Integrado Multidisciplinar).

**Prioridades:**
* **🔴 Must-Have (Obrigatório):** O MVP (Produto Mínimo Viável).
* **🟡 Should-Have (Deveria Ter):** Funcionalidades importantes que agregam valor.
* **🟢 Could-Have (Poderia Ter):** Melhorias que podem ser desenvolvidas após o MVP.

---

## 🚀 Produto 1: Plataforma Web "Backroom"
*Usuários: `Visitante`, `Cliente (Empresa)`, `Administrador (Backroom)`*

### 🔴 Must-Have (MVP)
-  **(Visitante):** Quero `ver a landing page` com os serviços, para `entender o que a Backroom faz`.
-  **(Visitante):** Quero `me cadastrar` como novo cliente, para `solicitar serviços`.
-  **(Cliente/Admin):** Quero `fazer login` no sistema, para `acessar meu painel`.
-  **(Cliente):** Quero `preencher um formulário de solicitação de orçamento`, para `iniciar um novo projeto`.
-  **(Admin Backroom):** Quero `receber e visualizar novas solicitações de orçamento`, para `analisá-las`.
-  **(Admin Backroom):** Quero `enviar um orçamento formal` ao cliente, para `aprovação`.
-  **(Cliente):** Quero `aprovar ou recusar um orçamento`, para `iniciar (ou não) o projeto`.

### 🟡 Should-Have
-  **(Cliente):** Quero `ver um dashboard` com meus projetos e seus status, para `acompanhar o progresso`.
-  **(Admin Backroom):** Quero `atualizar o status de um projeto`, para `informar o cliente`.
-  **(Cliente):** Quero `ter uma área para baixar os arquivos` do módulo concluído, para `integrá-lo`.

### 🟢 Could-Have
-  **(Cliente):** Quero `realizar o pagamento de uma fatura` pela plataforma, para `agilizar o financeiro`.
-  **(Admin Backroom):** Quero `ver um painel financeiro` com pagamentos, para `gerenciar o fluxo de caixa`.
-  **(Cliente):** Quero `ter um chat` no projeto, para `falar com o desenvolvedor`.

---

## 💻 Produto 2: App Desktop "Help Desk"
*Usuários: `Funcionário (Cliente)`, `Administrador (Cliente)`*

### 🔴 Must-Have (MVP)
-  **(Usuário):** Quero `fazer login` no app, para `acessar minhas funções`.
-  **(Funcionário):** Quero `solicitar a abertura de um chamado` (Estado: `Solicitado`), para `reportar um problema`.
-  **(Funcionário):** Quero `visualizar a lista dos meus chamados` e seus status, para `acompanhar`.
-  **(Admin):** Quero `visualizar a lista de solicitações pendentes`, para `gerenciá-las`.
-  **(Admin):** Quero `aceitar ou recusar uma solicitação` (Estados: `Solicitado` -> `Aberto` / `Fechado`), para `iniciar o trabalho`.
-  **(Admin):** Quero `visualizar todos os chamados abertos` em um painel.
-  **(Funcionário):** Quero `adicionar um comentário` a um chamado meu, para `fornecer mais informações`.
-  **(Admin):** Quero `adicionar um comentário` a um chamado, para `responder ou pedir informações`.
-  **(Admin):** Quero `marcar um chamado como "Resolvido"` (Estado: `Aberto` -> `Resolvido`), para `indicar a solução`.
-  **(Funcionário):** Quero `receber uma notificação` no app quando meu chamado for atualizado.

### 🟡 Should-Have
-  **(Funcionário):** Quero `confirmar a solução` e fechar o chamado (Estado: `Resolvido` -> `Fechado`).
-  **(Funcionário):** Quero `reabrir um chamado "Resolvido"` se a solução não funcionar (Estado: `Resolvido` -> `Aberto`).
-  **(Admin):** Quero `criar um chamado diretamente` (Estado: `[*]` -> `Aberto`), para `registrar problemas que identifiquei`.
-  **(Admin):** Quero `marcar um chamado como "Pendente"` (Estado: `Aberto` -> `Pendente`), para `sinalizar que aguardo resposta`.
-  **(Admin):** Quero `excluir ou cancelar um chamado` irrelevante.

### 🟢 Could-Have
-  **(Admin):** Quero `atribuir um chamado` a um técnico ou departamento.
-  **(Admin):** Quero `definir uma prioridade` (Baixa, Média, Alta) para um chamado.
-  **(Admin):** Quero `ver um dashboard com relatórios` (tempo médio de resolução, etc.), para `medir performance`.

---

## 📱 Produto 3: App Mobile "Help Desk"
*Usuário: `Administrador (Cliente)`*

### 🔴 Must-Have (MVP)
-  **(Admin):** Quero `fazer login seguro` (biometria/PIN), para `proteger os dados`.
-  **(Admin):** Quero `receber notificações push` quando um chamado for atualizado, para `ser informado em tempo real`.
-  **(Admin):** Quero `visualizar a lista de todos os chamados` e seus status.
-  **(Admin):** Quero `visualizar os detalhes` de um chamado específico.
-  **(Admin):** Quero `aceitar ou recusar uma nova solicitação` pelo celular, para `dar uma resposta rápida`.
-  **(Admin):** Quero `marcar um chamado como "Resolvido"` pelo celular, para `concluir tarefas de qualquer lugar`.

### 🟡 Should-Have
-  **(Admin):** Quero `adicionar um comentário` a um chamado pelo celular, para `responder rapidamente`.
-  **(Admin):** Quero `marcar um chamado como "Pendente"` pelo celular.

### 🟢 Could-Have
-  **(Admin):** Quero `criar um novo chamado` pelo app, para `registrar problemas "em campo"`.
-  **(Admin):** Quero `visualizar relatórios simples` (chamados abertos vs. fechados hoje).

*Última atualização: 27/10/2025*
*Versão do documento: 1.0*
