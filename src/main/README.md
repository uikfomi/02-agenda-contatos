[🏠 Início](../../README.md) / [⬆️ src](../README.md) / 📂 main

# 🚀 Aplicação principal

Contém o código executável e os recursos necessários à aplicação JavaFX.

Os arquivos Java e os recursos FXML/CSS são compilados e copiados pelo Maven em etapas distintas.

## Explore as subpastas e arquivos

| Caminho | Conteúdo e responsabilidade |
|---|---|
| [java/](java/) | Pacotes de código Java. [Abrir guia](java/README.md). |
| [resources/](resources/) | Recursos institucionais ou recursos JavaFX, conforme a localização. [Abrir guia](resources/README.md). |
| [README.md](README.md) | Guia de navegação e explicações desta pasta. |

## Árvore estrutural comentada

O ponto inicial é `src/main/`.

```text
src/main/  # Contém o código executável e os recursos necessários à aplicação JavaFX.
├── java/  # Pacotes de código Java.
│   ├── com/  # Raiz de pacotes Java.
│   │   ├── salgaderia/  # Pacote da aplicação Salgaderia.
│   │   │   ├── app/  # Componentes da aplicação e suas camadas.
│   │   │   │   ├── controller/  # Controllers das telas e testes de interface, conforme a localização.
│   │   │   │   │   └── AgendaController.java  # Interface da agenda de clientes e fornecedores.
│   │   │   │   ├── dao/  # Contratos de acesso a dados ou testes JDBC.
│   │   │   │   │   ├── impl/  # Implementações JDBC dos contratos DAO, com comandos parametrizados.
│   │   │   │   │   │   └── ContatoDAOImpl.java  # Operações JDBC de contatos com filtros de clientes e fornecedores.
│   │   │   │   │   └── ContatoDAO.java  # Contrato para cadastro, edição, exclusão e busca filtrada de contatos.
│   │   │   │   ├── exception/  # Exceções personalizadas de domínio e persistência.
│   │   │   │   │   └── PersistenciaException.java  # Encapsula erro de persistência.
│   │   │   │   ├── model/  # Entidades de domínio ou testes dessas entidades.
│   │   │   │   │   ├── enums/  # Enumerações com comportamento e respectivos testes.
│   │   │   │   │   │   ├── CategoriaInsumo.java  # Categorias de insumos de fornecedores.
│   │   │   │   │   │   └── PerfilUsuario.java  # Perfis de acesso do usuário.
│   │   │   │   │   ├── Cliente.java  # Contato especializado em cliente.
│   │   │   │   │   ├── Contato.java  # Abstração comum de contatos.
│   │   │   │   │   ├── Fornecedor.java  # Contato especializado em fornecedor.
│   │   │   │   │   ├── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   │   ├── Usuario.java  # Abstração de usuário e permissões.
│   │   │   │   │   ├── UsuarioAdmin.java  # Usuário administrativo.
│   │   │   │   │   ├── UsuarioCliente.java  # Usuário vinculado a um cliente.
│   │   │   │   │   └── Validacao.java  # Validações compartilhadas das entidades.
│   │   │   │   ├── service/  # Contratos, regras de negócio e testes de serviços.
│   │   │   │   │   ├── impl/  # Implementações de regras e orquestração dos serviços.
│   │   │   │   │   │   └── AgendaServiceImpl.java  # Valida e coordena cadastro, busca e alterações de contatos pela camada DAO.
│   │   │   │   │   └── AgendaService.java  # Contrato de operações e busca da agenda de clientes e fornecedores.
│   │   │   │   ├── util/  # Conexão, autenticação auxiliar e navegação.
│   │   │   │   │   ├── ConnectionFactory.java  # Pool HikariCP e transações JDBC.
│   │   │   │   │   ├── Navegacao.java  # Navegação entre telas FXML.
│   │   │   │   │   ├── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   │   └── TelaAutenticada.java  # Contrato para telas com usuário autenticado.
│   │   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   └── README.md  # Guia de navegação e explicações desta pasta.
├── resources/  # Recursos institucionais ou recursos JavaFX, conforme a localização.
│   ├── css/  # Folhas de estilo das telas JavaFX.
│   │   ├── agenda.css  # Estilos da agenda.
│   │   └── global.css  # Estilos compartilhados da aplicação.
│   ├── fxml/  # Descrições de interface JavaFX.
│   │   └── agenda-contatos.fxml  # Estrutura visual da agenda.
│   ├── database.properties  # Template de configuração JDBC; não contém credenciais locais.
│   └── README.md  # Guia de navegação e explicações desta pasta.
└── README.md  # Guia de navegação e explicações desta pasta.
```

[🏠 Voltar ao README principal](../../README.md)
