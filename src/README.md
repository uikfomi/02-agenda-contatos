[🏠 Início](../README.md) / 📂 src

# 💻 Código-fonte e testes

Reúne o código da aplicação, os recursos carregados pelo JavaFX e, quando presentes, os testes automatizados.

A implementação respeita a separação entre interface, serviços, modelos e acesso a dados; configurações locais não devem ser versionadas.

## Explore as subpastas e arquivos

| Caminho | Conteúdo e responsabilidade |
|---|---|
| [main/](main/) | Aplicação principal e seus recursos. [Abrir guia](main/README.md). |
| [.gitkeep](.gitkeep) | Marcador que mantém a pasta no controle de versão; não contém dados de aplicação. |
| [README.md](README.md) | Guia de navegação e explicações desta pasta. |

## Árvore estrutural comentada

O ponto inicial é `src/`; cada comentário apresenta o caminho completo relativo à raiz do repositório.

```text
src/  # Reúne o código da aplicação, os recursos carregados pelo JavaFX e, quando presentes, os testes automatizados.
├── main/  # src/main/ — Aplicação principal e seus recursos.
│   ├── java/  # src/main/java/ — Pacotes de código Java.
│   │   ├── com/  # src/main/java/com/ — Raiz de pacotes Java.
│   │   │   ├── salgaderia/  # src/main/java/com/salgaderia/ — Pacote da aplicação Salgaderia.
│   │   │   │   ├── app/  # src/main/java/com/salgaderia/app/ — Componentes da aplicação e suas camadas.
│   │   │   │   │   ├── controller/  # src/main/java/com/salgaderia/app/controller/ — Controllers das telas e testes de interface, conforme a localização.
│   │   │   │   │   │   └── AgendaController.java  # src/main/java/com/salgaderia/app/controller/AgendaController.java — Interface da agenda de clientes e fornecedores.
│   │   │   │   │   ├── dao/  # src/main/java/com/salgaderia/app/dao/ — Contratos de acesso a dados ou testes JDBC.
│   │   │   │   │   │   ├── impl/  # src/main/java/com/salgaderia/app/dao/impl/ — Implementações JDBC dos contratos DAO, com comandos parametrizados.
│   │   │   │   │   │   │   └── ContatoDAOImpl.java  # src/main/java/com/salgaderia/app/dao/impl/ContatoDAOImpl.java — Operações JDBC de contatos com filtros de clientes e fornecedores.
│   │   │   │   │   │   └── ContatoDAO.java  # src/main/java/com/salgaderia/app/dao/ContatoDAO.java — Contrato para cadastro, edição, exclusão e busca filtrada de contatos.
│   │   │   │   │   ├── exception/  # src/main/java/com/salgaderia/app/exception/ — Exceções personalizadas de domínio e persistência.
│   │   │   │   │   │   └── PersistenciaException.java  # src/main/java/com/salgaderia/app/exception/PersistenciaException.java — Encapsula erro de persistência.
│   │   │   │   │   ├── model/  # src/main/java/com/salgaderia/app/model/ — Entidades de domínio ou testes dessas entidades.
│   │   │   │   │   │   ├── enums/  # src/main/java/com/salgaderia/app/model/enums/ — Enumerações com comportamento e respectivos testes.
│   │   │   │   │   │   │   ├── CategoriaInsumo.java  # src/main/java/com/salgaderia/app/model/enums/CategoriaInsumo.java — Categorias de insumos de fornecedores.
│   │   │   │   │   │   │   └── PerfilUsuario.java  # src/main/java/com/salgaderia/app/model/enums/PerfilUsuario.java — Perfis de acesso do usuário.
│   │   │   │   │   │   ├── Cliente.java  # src/main/java/com/salgaderia/app/model/Cliente.java — Contato especializado em cliente.
│   │   │   │   │   │   ├── Contato.java  # src/main/java/com/salgaderia/app/model/Contato.java — Abstração comum de contatos.
│   │   │   │   │   │   ├── Fornecedor.java  # src/main/java/com/salgaderia/app/model/Fornecedor.java — Contato especializado em fornecedor.
│   │   │   │   │   │   ├── README.md  # src/main/java/com/salgaderia/app/model/README.md — Guia de navegação e explicações desta pasta.
│   │   │   │   │   │   ├── Usuario.java  # src/main/java/com/salgaderia/app/model/Usuario.java — Abstração de usuário e permissões.
│   │   │   │   │   │   ├── UsuarioAdmin.java  # src/main/java/com/salgaderia/app/model/UsuarioAdmin.java — Usuário administrativo.
│   │   │   │   │   │   ├── UsuarioCliente.java  # src/main/java/com/salgaderia/app/model/UsuarioCliente.java — Usuário vinculado a um cliente.
│   │   │   │   │   │   └── Validacao.java  # src/main/java/com/salgaderia/app/model/Validacao.java — Validações compartilhadas das entidades.
│   │   │   │   │   ├── service/  # src/main/java/com/salgaderia/app/service/ — Contratos, regras de negócio e testes de serviços.
│   │   │   │   │   │   ├── impl/  # src/main/java/com/salgaderia/app/service/impl/ — Implementações de regras e orquestração dos serviços.
│   │   │   │   │   │   │   └── AgendaServiceImpl.java  # src/main/java/com/salgaderia/app/service/impl/AgendaServiceImpl.java — Valida e coordena cadastro, busca e alterações de contatos pela camada DAO.
│   │   │   │   │   │   └── AgendaService.java  # src/main/java/com/salgaderia/app/service/AgendaService.java — Contrato de operações e busca da agenda de clientes e fornecedores.
│   │   │   │   │   ├── util/  # src/main/java/com/salgaderia/app/util/ — Conexão, autenticação auxiliar e navegação.
│   │   │   │   │   │   ├── ConnectionFactory.java  # src/main/java/com/salgaderia/app/util/ConnectionFactory.java — Pool HikariCP e transações JDBC.
│   │   │   │   │   │   ├── Navegacao.java  # src/main/java/com/salgaderia/app/util/Navegacao.java — Navegação entre telas FXML.
│   │   │   │   │   │   ├── README.md  # src/main/java/com/salgaderia/app/util/README.md — Guia de navegação e explicações desta pasta.
│   │   │   │   │   │   └── TelaAutenticada.java  # src/main/java/com/salgaderia/app/util/TelaAutenticada.java — Contrato para telas com usuário autenticado.
│   │   │   │   │   └── README.md  # src/main/java/com/salgaderia/app/README.md — Guia de navegação e explicações desta pasta.
│   │   │   │   └── README.md  # src/main/java/com/salgaderia/README.md — Guia de navegação e explicações desta pasta.
│   │   │   └── README.md  # src/main/java/com/README.md — Guia de navegação e explicações desta pasta.
│   │   └── README.md  # src/main/java/README.md — Guia de navegação e explicações desta pasta.
│   ├── resources/  # src/main/resources/ — Recursos institucionais ou recursos JavaFX, conforme a localização.
│   │   ├── css/  # src/main/resources/css/ — Folhas de estilo das telas JavaFX.
│   │   │   ├── agenda.css  # src/main/resources/css/agenda.css — Estilos da agenda.
│   │   │   └── global.css  # src/main/resources/css/global.css — Estilos compartilhados da aplicação.
│   │   ├── fxml/  # src/main/resources/fxml/ — Descrições de interface JavaFX.
│   │   │   └── agenda-contatos.fxml  # src/main/resources/fxml/agenda-contatos.fxml — Estrutura visual da agenda.
│   │   ├── database.properties  # src/main/resources/database.properties — Template de configuração JDBC; não contém credenciais locais.
│   │   └── README.md  # src/main/resources/README.md — Guia de navegação e explicações desta pasta.
│   └── README.md  # src/main/README.md — Guia de navegação e explicações desta pasta.
├── .gitkeep  # src/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
└── README.md  # src/README.md — Guia de navegação e explicações desta pasta.
```

[🏠 Voltar ao README principal](../README.md)
