# Diagrama de Classes (Entidades Principais)

```mermaid
classDiagram
    class User {
        +int UserId
        +string FullName
        +string Username
        +string Password
        +string Role
    }

    class Chamado {
        +int ChamadoId
        +string Titulo
        +string Descricao
        +string Status
        +DateTime DataAbertura
        +int AutorId
        +int TecnicoId
    }

    User "1" -- "1..*" Chamado : Autor (Abre)
    User "1" -- "0..*" Chamado : Técnico (Atende)
```

# Diagrama de Classes Desktop - Client-side

```mermaid
classDiagram
    class User {
        +int UserId
        +string FullName
        +string Username
        +string Password
        +string Role
    }

    class Chamado {
        +int ChamadoId
        +string Titulo
        +string Descricao
        +string Status
        +DateTime DataAbertura
        +int AutorId
        +int TecnicoId
    }

    User "1" -- "1..*" Chamado : Autor (Abre)
    User "1" -- "0..*" Chamado : Técnico (Atende)
```

# Diagrama de Classes (Implementação e Dependências)

```mermaid
classDiagram
    direction TB

    class LoginScreen {
        + exibirFormulario()
        + usarBiometria()
    }

    class ChamadoListScreen {
        + exibirListaChamados()
    }
    
    class PushNotificationHandler {
        + onReceive(notificacao)
        + exibirAlerta()
    }

    class ApiService {
        - apiToken: String
        + autenticar(user, pass)
        + buscarChamados()
        + aprovarSolicitacao(id)
        + marcarConcluido(id)
    }

    class ChamadoModel {
        <<Model>>
        - id: int
        - titulo: String
    }

    LoginScreen --> ApiService : usa
    ChamadoListScreen --> ApiService : usa
    PushNotificationHandler --> ApiService : usa
    ApiService ..> ChamadoModel : cria/popula
```
