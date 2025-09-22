---
title: Diagrama de Casos de Uso - Plataforma Backroom
---
graph TD
    subgraph " "
        direction LR
        subgraph "Atores"
            direction TB
            A1(Visitante)
            A2(Cliente)
            A3(Administrador)
        end
        subgraph "Sistema Backroom"
            direction TB
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
    end

    A1 --o UC1
    A1 --o UC2
    A1 --o UC3
    A1 --o UC4

    A2 --o UC5
    A2 --o UC6
    A2 --o UC7
    A2 --o UC8

    A3 --o UC9
    A3 --o UC10

    UC4 ..> UC5 : <<include>>
