### Diagrama de Classes

```mermaid
classDiagram
    direction TB

    abstract class Usuario {
        # int id
        # String email
        # String nome
        # String senha
        + login()
        + logout()
    }

    class Cliente {
        - String empresa
        + solicitarOrcamento()
        + visualizarProjetos()
    }

    class Administrador {
        + analisarSolicitacoes()
        + gerarOrcamento()
    }

    class Projeto {
        - int id
        - String nome
        - String descricao
        - String status
        + atualizarStatus()
        + adicionarMensagem()
    }

    class Orcamento {
        - int id
        - String descricaoServicos
        - float valor
        - String status
        + aprovar()
        + rejeitar()
    }

    class Mensagem {
        - int id
        - String conteudo
        - DateTime dataEnvio
    }

    Usuario <|-- Cliente
    Usuario <|-- Administrador

    Cliente "1" -- "0..*" Projeto : possui
    Cliente "1" -- "1..*" Orcamento : solicita
    Administrador "1" -- "1..*" Orcamento : gera
    Orcamento "1" -- "1" Projeto : se transforma em
    Projeto "1" -- "0..*" Mensagem : contém
    Usuario "1" -- "1..*" Mensagem : é o autor
```
