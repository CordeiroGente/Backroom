# Diagrama de Caso de Uso Web - Padrão

- A seguir um diagrama que demonstra como um visitante, um cliente/usuário e como um administrador interagem com o sistema web de assistência.

### Atores
- **Visitante**: Um não cliente interessado nos serviços da Backroom
- **Cliente/Usuário**: Alguém com cadastro no sistema 
- **Administrador**: Resposta de dúvidas sobre os serviços

```mermaid
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
```

# Diagrama de Casos de Uso Desktop - Exemplo

- A seguir um Diagrama que demonstra como Funcionário e Administrador iriam reagir em um sistema modular backroom criado para a resolução de chamados da empresa cliente.

### Atores
- **Funcionários**: Respondem a chamados e solicitam novos
- **Administradores**: Manejam o sistema.

```mermaid
graph TD
    %% Atores
    Funcionario("Funcionário")
    Administrador("Administrador")

    %% Sistema e Casos de Uso
    subgraph "Sistema de Chamados (Desktop)"
        direction TB
        
        %% UCs Gerais
        UC_Login("Realizar Login")

        %% UCs do Funcionário
        UC_F1("Solicitar Abertura de Chamado")
        UC_F2("Visualizar Chamado")
        UC_F3("Resolver Chamados")
        
        %% UCs do Administrador
        UC_A1("Aceitar Solicitação de Chamado")
        UC_A2("Criar Chamado Diretamente")
        UC_A3("Marcar Chamado como Concluído")
        UC_A4("Excluir Chamado")
        UC_A5("Resolver Chamados")
        UC_A6("Manejamento de Contas")

        %% Links Invisíveis para forçar a verticalização
        UC_F1 ~~~ UC_F2
        UC_F2 ~~~ UC_F3
        
        UC_A1 ~~~ UC_A2
        UC_A2 ~~~ UC_A3
        UC_A3 ~~~ UC_A4
        UC_A4 ~~~ UC_A5
    end

    %% Relacionamentos Atores -> Casos de Uso
    Funcionario --- UC_Login
    Funcionario --- UC_F1
    Funcionario --- UC_F2
    Funcionario --- UC_F3
    
    Administrador --- UC_Login
    Administrador --- UC_A1
    Administrador --- UC_A2
    Administrador --- UC_A3
    Administrador --- UC_A4
    Administrador --- UC_A5
    Administrador --- UC_A6
    
    %% Relações |include| (de UCs para Login)
    UC_F1 -.->|include| UC_Login
    UC_F2 -.->|include| UC_Login
    UC_F3 -.->|include| UC_Login
    UC_A1 -.->|include| UC_Login
    UC_A2 -.->|include| UC_Login
    UC_A3 -.->|include| UC_Login
    UC_A4 -.->|include| UC_Login
    UC_A5 -.->|include| UC_Login
    UC_A6 -.->|include| UC_Login

```

# Diagrama de Casos de Uso Mobile - Gerenciamento

- A seguir um Diagrama que demonstra como O Administrador iria ter acesso ao sistema desktop pelo celular, garantindo mobilidade caso ele seja um gestor de diversas empresas.

### Atores
- **Administrador**: O app mobile, sendo exclusivo para administradores garante Gerenciamento à distância


```mermaid
graph TD
    %% Ator
    Administrador("Administrador")

    %% Sistema e Casos de Uso
    subgraph "Sistema de Chamados"
        direction TB
        
        %% UCs Gerais
        UC_Login_Mob("Realizar Login Seguro")
        UC_Notif("Receber Notificações Push")

        %% UCs de Gerenciamento
        UC_Mob1("Visualizar Todos Chamados")
        UC_Mob2("Aceitar Solicitação de Chamado")
        UC_Mob3("Criar Chamado Diretamente")
        UC_Mob4("Marcar Chamado como Concluído")
        UC_Mob5("Excluir Chamado")
        

        %% Links Invisíveis para forçar a verticalização
        UC_Notif ~~~ UC_Mob1
        UC_Mob1 ~~~ UC_Mob2
        UC_Mob2 ~~~ UC_Mob3
        UC_Mob3 ~~~ UC_Mob4
        UC_Mob4 ~~~ UC_Mob5
    end

    %% Relacionamentos Ator -> Casos de Uso
    Administrador --- UC_Login_Mob
    Administrador --- UC_Notif
    Administrador --- UC_Mob1
    Administrador --- UC_Mob2
    Administrador --- UC_Mob3
    Administrador --- UC_Mob4
    Administrador --- UC_Mob5
    
    
    %% Relações |include| (de UCs para Login)
    UC_Notif -.->|include| UC_Login_Mob
    UC_Mob1 -.->|include| UC_Login_Mob
    UC_Mob2 -.->|include| UC_Login_Mob
    UC_Mob3 -.->|include| UC_Login_Mob
    UC_Mob4 -.->|include| UC_Login_Mob
    UC_Mob5 -.->|include| UC_Login_Mob
```
