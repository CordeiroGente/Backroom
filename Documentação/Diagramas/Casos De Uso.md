``mermaid
---
title: Diagrama de Casos de Uso - Plataforma Backroom
---
graph TD
    %% Atores
    Visitante
    Cliente
    Administrador

    %% Sistema e Casos de Uso
    subgraph "Sistema Backroom"
        UC1("Visualizar Landing Page")
        UC2("Consultar Serviços")
        UC3("Solicitar Contato via E-mail")
        UC4("Realizar Cadastro")
        UC5("Realizar Login")
        UC6("Gerenciar Projetos")
        UC7("Solicitar Orçamento")
        UC8("Acompanhar Status do Projeto")
        UC9("Analisar Solicitações")
        UC10("Gerar Orçamento")
    end

    %% Relacionamentos
    Visitante --- UC1
    Visitante --- UC2
    Visitante --- UC3
    Visitante --- UC4

    Cliente --- UC5
    Cliente --- UC6
    Cliente --- UC7
    Cliente --- UC8

    Administrador --- UC9
    Administrador --- UC10

    UC4 ..> UC5 : "<<include>>"
```
