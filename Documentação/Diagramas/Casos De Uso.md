graph TD
    subgraph "Site & Plataforma Backroom"
        UC1(Visualizar Landing Page)
        UC2(Consultar Serviços)
        UC3(Solicitar Contato)
        UC4(Realizar Cadastro)
        UC5(Gerenciar Projetos)
        UC6(Solicitar Orçamento)
        UC7(Acompanhar Status do Projeto)
        UC8(Realizar Login)
        UC9(Analisar Solicitações)
        UC10(Gerar Orçamento)
    end

    Visitante --|> UC1
    Visitante --|> UC2
    Visitante --|> UC3
    Visitante --|> UC4

    UC4 -- include --> UC8

    Cliente --|> UC8
    Cliente --|> UC5
    Cliente --|> UC6
    Cliente --|> UC7

    Administrador --|> UC9
    Administrador --|> UC10
