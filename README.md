# Ui K'fomi — 02-agenda-contatos

A **Ui K'fomi** é uma startup de Maranguape, Ceará, dedicada a soluções digitais para o setor de alimentação. Este módulo acadêmico de POO aborda agenda estratégica de clientes e fornecedores, com busca e gestão de contatos.

## Escopo

Extração do sistema integrado, com as dependências de domínio e persistência necessárias. Usa Java 17, JavaFX, MySQL com JDBC e HikariCP, seguindo MVC + Service + DAO. As pastas oficiais estão presentes na raiz; os recursos JavaFX ativos ficam em `src/main/resources`.

## Compilação e integração

Execute `mvn clean test-compile` na raiz. O arquivo `database/scripts/schema.sql` contém somente as tabelas necessárias para este recorte; configure credenciais locais em `src/main/resources/database.local.properties`, que não deve ser versionado. Este repositório é um **recorte para integração**, não um aplicativo independente completo: telas externas e navegação para outros módulos pertencem ao projeto integrado [`03-ui-kfomi`](https://github.com/uikfomi/03-ui-kfomi). Não há usuários de demonstração no script.

Licença MIT; consulte `LICENSE`.

## 📂 Organização do Projeto

A árvore mostra todos os arquivos versionados e os guias desta documentação. Credenciais locais, arquivos ignorados e artefatos de compilação não fazem parte do inventário.

### Guias navegáveis

| Diretório | Guia |
|---|---|
| `database/` | [Abrir README](database/README.md) |
| `docs/` | [Abrir README](docs/README.md) |
| `docs/ui-ux/` | [Abrir README](docs/ui-ux/README.md) |
| `resources/` | [Abrir README](resources/README.md) |
| `src/` | [Abrir README](src/README.md) |
| `src/main/` | [Abrir README](src/main/README.md) |
| `src/main/java/` | [Abrir README](src/main/java/README.md) |
| `src/main/java/com/` | [Abrir README](src/main/java/com/README.md) |
| `src/main/java/com/salgaderia/` | [Abrir README](src/main/java/com/salgaderia/README.md) |
| `src/main/java/com/salgaderia/app/` | [Abrir README](src/main/java/com/salgaderia/app/README.md) |
| `src/main/java/com/salgaderia/app/model/` | [Abrir README](src/main/java/com/salgaderia/app/model/README.md) |
| `src/main/java/com/salgaderia/app/util/` | [Abrir README](src/main/java/com/salgaderia/app/util/README.md) |
| `src/main/resources/` | [Abrir README](src/main/resources/README.md) |
| `support/` | [Abrir README](support/README.md) |

### Árvore completa comentada

Cada comentário indica o caminho completo relativo à raiz e a responsabilidade do item.

```text
02-agenda-contatos/  # Raiz do repositório Ui K'Fomi
├── database/  # database/ — Modelos, schema e migrações para o MySQL.
│   ├── DER/  # database/DER/ — Modelo entidade-relacionamento e seus materiais.
│   │   └── .gitkeep  # database/DER/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── DL/  # database/DL/ — Modelo lógico das tabelas e relações.
│   │   └── .gitkeep  # database/DL/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── scripts/  # database/scripts/ — Schema e migrações SQL ordenadas pela evolução do sistema.
│   │   ├── .gitkeep  # database/scripts/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   └── schema.sql  # database/scripts/schema.sql — Schema inicial MySQL usado pelo respectivo repositório.
│   └── README.md  # database/README.md — Guia de navegação e explicações desta pasta.
├── docs/  # docs/ — Documentação, diagramas, interfaces e apresentações.
│   ├── diagrams/  # docs/diagrams/ — Espaço para diagramas adicionais.
│   │   └── .gitkeep  # docs/diagrams/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── presentations/  # docs/presentations/ — Espaço reservado para slides e apresentações.
│   │   └── .gitkeep  # docs/presentations/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── ui-ux/  # docs/ui-ux/ — Artefatos de experiência do usuário.
│   │   ├── mockups/  # docs/ui-ux/mockups/ — Espaço reservado para mockups.
│   │   │   └── .gitkeep  # docs/ui-ux/mockups/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   ├── prototypes/  # docs/ui-ux/prototypes/ — Espaço reservado para protótipos.
│   │   │   └── .gitkeep  # docs/ui-ux/prototypes/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   ├── wireframes/  # docs/ui-ux/wireframes/ — Espaço reservado para wireframes.
│   │   │   └── .gitkeep  # docs/ui-ux/wireframes/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   └── README.md  # docs/ui-ux/README.md — Guia de navegação e explicações desta pasta.
│   ├── uml/  # docs/uml/ — Materiais para diagramas de classes e modelagem UML.
│   │   └── .gitkeep  # docs/uml/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # docs/README.md — Guia de navegação e explicações desta pasta.
├── resources/  # resources/ — Recursos institucionais ou recursos JavaFX, conforme a localização.
│   ├── .gitkeep  # resources/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # resources/README.md — Guia de navegação e explicações desta pasta.
├── src/  # src/ — Fontes, recursos de execução e testes do projeto.
│   ├── main/  # src/main/ — Aplicação principal e seus recursos.
│   │   ├── java/  # src/main/java/ — Pacotes de código Java.
│   │   │   ├── com/  # src/main/java/com/ — Raiz de pacotes Java.
│   │   │   │   ├── salgaderia/  # src/main/java/com/salgaderia/ — Pacote da aplicação Salgaderia.
│   │   │   │   │   ├── app/  # src/main/java/com/salgaderia/app/ — Componentes da aplicação e suas camadas.
│   │   │   │   │   │   ├── controller/  # src/main/java/com/salgaderia/app/controller/ — Controllers das telas e testes de interface, conforme a localização.
│   │   │   │   │   │   │   └── AgendaController.java  # src/main/java/com/salgaderia/app/controller/AgendaController.java — Interface da agenda de clientes e fornecedores.
│   │   │   │   │   │   ├── dao/  # src/main/java/com/salgaderia/app/dao/ — Contratos de acesso a dados ou testes JDBC.
│   │   │   │   │   │   │   ├── impl/  # src/main/java/com/salgaderia/app/dao/impl/ — Implementações JDBC dos contratos DAO, com comandos parametrizados.
│   │   │   │   │   │   │   │   └── ContatoDAOImpl.java  # src/main/java/com/salgaderia/app/dao/impl/ContatoDAOImpl.java — Operações JDBC de contatos com filtros de clientes e fornecedores.
│   │   │   │   │   │   │   └── ContatoDAO.java  # src/main/java/com/salgaderia/app/dao/ContatoDAO.java — Contrato para cadastro, edição, exclusão e busca filtrada de contatos.
│   │   │   │   │   │   ├── exception/  # src/main/java/com/salgaderia/app/exception/ — Exceções personalizadas de domínio e persistência.
│   │   │   │   │   │   │   └── PersistenciaException.java  # src/main/java/com/salgaderia/app/exception/PersistenciaException.java — Encapsula erro de persistência.
│   │   │   │   │   │   ├── model/  # src/main/java/com/salgaderia/app/model/ — Entidades de domínio ou testes dessas entidades.
│   │   │   │   │   │   │   ├── enums/  # src/main/java/com/salgaderia/app/model/enums/ — Enumerações com comportamento e respectivos testes.
│   │   │   │   │   │   │   │   ├── CategoriaInsumo.java  # src/main/java/com/salgaderia/app/model/enums/CategoriaInsumo.java — Categorias de insumos de fornecedores.
│   │   │   │   │   │   │   │   └── PerfilUsuario.java  # src/main/java/com/salgaderia/app/model/enums/PerfilUsuario.java — Perfis de acesso do usuário.
│   │   │   │   │   │   │   ├── Cliente.java  # src/main/java/com/salgaderia/app/model/Cliente.java — Contato especializado em cliente.
│   │   │   │   │   │   │   ├── Contato.java  # src/main/java/com/salgaderia/app/model/Contato.java — Abstração comum de contatos.
│   │   │   │   │   │   │   ├── Fornecedor.java  # src/main/java/com/salgaderia/app/model/Fornecedor.java — Contato especializado em fornecedor.
│   │   │   │   │   │   │   ├── README.md  # src/main/java/com/salgaderia/app/model/README.md — Guia de navegação e explicações desta pasta.
│   │   │   │   │   │   │   ├── Usuario.java  # src/main/java/com/salgaderia/app/model/Usuario.java — Abstração de usuário e permissões.
│   │   │   │   │   │   │   ├── UsuarioAdmin.java  # src/main/java/com/salgaderia/app/model/UsuarioAdmin.java — Usuário administrativo.
│   │   │   │   │   │   │   ├── UsuarioCliente.java  # src/main/java/com/salgaderia/app/model/UsuarioCliente.java — Usuário vinculado a um cliente.
│   │   │   │   │   │   │   └── Validacao.java  # src/main/java/com/salgaderia/app/model/Validacao.java — Validações compartilhadas das entidades.
│   │   │   │   │   │   ├── service/  # src/main/java/com/salgaderia/app/service/ — Contratos, regras de negócio e testes de serviços.
│   │   │   │   │   │   │   ├── impl/  # src/main/java/com/salgaderia/app/service/impl/ — Implementações de regras e orquestração dos serviços.
│   │   │   │   │   │   │   │   └── AgendaServiceImpl.java  # src/main/java/com/salgaderia/app/service/impl/AgendaServiceImpl.java — Valida e coordena cadastro, busca e alterações de contatos pela camada DAO.
│   │   │   │   │   │   │   └── AgendaService.java  # src/main/java/com/salgaderia/app/service/AgendaService.java — Contrato de operações e busca da agenda de clientes e fornecedores.
│   │   │   │   │   │   ├── util/  # src/main/java/com/salgaderia/app/util/ — Conexão, autenticação auxiliar e navegação.
│   │   │   │   │   │   │   ├── ConnectionFactory.java  # src/main/java/com/salgaderia/app/util/ConnectionFactory.java — Pool HikariCP e transações JDBC.
│   │   │   │   │   │   │   ├── Navegacao.java  # src/main/java/com/salgaderia/app/util/Navegacao.java — Navegação entre telas FXML.
│   │   │   │   │   │   │   ├── README.md  # src/main/java/com/salgaderia/app/util/README.md — Guia de navegação e explicações desta pasta.
│   │   │   │   │   │   │   └── TelaAutenticada.java  # src/main/java/com/salgaderia/app/util/TelaAutenticada.java — Contrato para telas com usuário autenticado.
│   │   │   │   │   │   └── README.md  # src/main/java/com/salgaderia/app/README.md — Guia de navegação e explicações desta pasta.
│   │   │   │   │   └── README.md  # src/main/java/com/salgaderia/README.md — Guia de navegação e explicações desta pasta.
│   │   │   │   └── README.md  # src/main/java/com/README.md — Guia de navegação e explicações desta pasta.
│   │   │   └── README.md  # src/main/java/README.md — Guia de navegação e explicações desta pasta.
│   │   ├── resources/  # src/main/resources/ — Recursos institucionais ou recursos JavaFX, conforme a localização.
│   │   │   ├── css/  # src/main/resources/css/ — Folhas de estilo das telas JavaFX.
│   │   │   │   ├── agenda.css  # src/main/resources/css/agenda.css — Estilos da agenda.
│   │   │   │   └── global.css  # src/main/resources/css/global.css — Estilos compartilhados da aplicação.
│   │   │   ├── fxml/  # src/main/resources/fxml/ — Descrições de interface JavaFX.
│   │   │   │   └── agenda-contatos.fxml  # src/main/resources/fxml/agenda-contatos.fxml — Estrutura visual da agenda.
│   │   │   ├── database.properties  # src/main/resources/database.properties — Template de configuração JDBC; não contém credenciais locais.
│   │   │   └── README.md  # src/main/resources/README.md — Guia de navegação e explicações desta pasta.
│   │   └── README.md  # src/main/README.md — Guia de navegação e explicações desta pasta.
│   ├── .gitkeep  # src/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # src/README.md — Guia de navegação e explicações desta pasta.
├── support/  # support/ — Documentação de apoio, referências e materiais complementares.
│   ├── .gitkeep  # support/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # support/README.md — Guia de navegação e explicações desta pasta.
├── .gitignore  # .gitignore — Regras para não versionar configurações locais e artefatos gerados.
├── LICENSE  # LICENSE — Texto da licença MIT.
├── pom.xml  # pom.xml — Configuração Maven, dependências e build do módulo.
└── README.md  # README.md — Guia de navegação e explicações desta pasta.
```
