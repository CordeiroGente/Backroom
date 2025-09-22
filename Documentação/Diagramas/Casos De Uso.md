graph TD
    Visitante
    Cliente
    Administrador

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

        %% Links Invisíveis para forçar a verticalização
        UC5 ~~~ UC6
        UC6 ~~~ UC7
        UC7 ~~~ UC8

        UC9 ~~~ UC10
    end

    %% Relacionamentos Visíveis
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
    
    UC4 -.->|include| UC5
