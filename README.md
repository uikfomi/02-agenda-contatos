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

Os comentários descrevem a responsabilidade de cada item.

```text
02-agenda-contatos/  # Raiz do repositório Ui K'Fomi
├── database/  # Modelos, schema e migrações para o MySQL.
│   ├── DER/  # Modelo entidade-relacionamento e seus materiais.
│   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── DL/  # Modelo lógico das tabelas e relações.
│   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── scripts/  # Schema e migrações SQL ordenadas pela evolução do sistema.
│   │   ├── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   └── schema.sql  # Schema inicial MySQL usado pelo respectivo repositório.
│   └── README.md  # Guia de navegação e explicações desta pasta.
├── docs/  # Documentação, diagramas, interfaces e apresentações.
│   ├── diagrams/  # Espaço para diagramas adicionais.
│   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── presentations/  # Espaço reservado para slides e apresentações.
│   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   ├── ui-ux/  # Artefatos de experiência do usuário.
│   │   ├── mockups/  # Espaço reservado para mockups.
│   │   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   ├── prototypes/  # Espaço reservado para protótipos.
│   │   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   ├── wireframes/  # Espaço reservado para wireframes.
│   │   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   ├── uml/  # Materiais para diagramas de classes e modelagem UML.
│   │   └── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # Guia de navegação e explicações desta pasta.
├── resources/  # Recursos institucionais ou recursos JavaFX, conforme a localização.
│   ├── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # Guia de navegação e explicações desta pasta.
├── src/  # Fontes, recursos de execução e testes do projeto.
│   ├── main/  # Aplicação principal e seus recursos.
│   │   ├── java/  # Pacotes de código Java.
│   │   │   ├── com/  # Raiz de pacotes Java.
│   │   │   │   ├── salgaderia/  # Pacote da aplicação Salgaderia.
│   │   │   │   │   ├── app/  # Componentes da aplicação e suas camadas.
│   │   │   │   │   │   ├── controller/  # Controllers das telas e testes de interface, conforme a localização.
│   │   │   │   │   │   │   └── AgendaController.java  # Interface da agenda de clientes e fornecedores.
│   │   │   │   │   │   ├── dao/  # Contratos de acesso a dados ou testes JDBC.
│   │   │   │   │   │   │   ├── impl/  # Implementações JDBC dos contratos DAO, com comandos parametrizados.
│   │   │   │   │   │   │   │   └── ContatoDAOImpl.java  # Operações JDBC de contatos com filtros de clientes e fornecedores.
│   │   │   │   │   │   │   └── ContatoDAO.java  # Contrato para cadastro, edição, exclusão e busca filtrada de contatos.
│   │   │   │   │   │   ├── exception/  # Exceções personalizadas de domínio e persistência.
│   │   │   │   │   │   │   └── PersistenciaException.java  # Encapsula erro de persistência.
│   │   │   │   │   │   ├── model/  # Entidades de domínio ou testes dessas entidades.
│   │   │   │   │   │   │   ├── enums/  # Enumerações com comportamento e respectivos testes.
│   │   │   │   │   │   │   │   ├── CategoriaInsumo.java  # Categorias de insumos de fornecedores.
│   │   │   │   │   │   │   │   └── PerfilUsuario.java  # Perfis de acesso do usuário.
│   │   │   │   │   │   │   ├── Cliente.java  # Contato especializado em cliente.
│   │   │   │   │   │   │   ├── Contato.java  # Abstração comum de contatos.
│   │   │   │   │   │   │   ├── Fornecedor.java  # Contato especializado em fornecedor.
│   │   │   │   │   │   │   ├── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   │   │   │   ├── Usuario.java  # Abstração de usuário e permissões.
│   │   │   │   │   │   │   ├── UsuarioAdmin.java  # Usuário administrativo.
│   │   │   │   │   │   │   ├── UsuarioCliente.java  # Usuário vinculado a um cliente.
│   │   │   │   │   │   │   └── Validacao.java  # Validações compartilhadas das entidades.
│   │   │   │   │   │   ├── service/  # Contratos, regras de negócio e testes de serviços.
│   │   │   │   │   │   │   ├── impl/  # Implementações de regras e orquestração dos serviços.
│   │   │   │   │   │   │   │   └── AgendaServiceImpl.java  # Valida e coordena cadastro, busca e alterações de contatos pela camada DAO.
│   │   │   │   │   │   │   └── AgendaService.java  # Contrato de operações e busca da agenda de clientes e fornecedores.
│   │   │   │   │   │   ├── util/  # Conexão, autenticação auxiliar e navegação.
│   │   │   │   │   │   │   ├── ConnectionFactory.java  # Pool HikariCP e transações JDBC.
│   │   │   │   │   │   │   ├── Navegacao.java  # Navegação entre telas FXML.
│   │   │   │   │   │   │   ├── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   │   │   │   └── TelaAutenticada.java  # Contrato para telas com usuário autenticado.
│   │   │   │   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   ├── resources/  # Recursos institucionais ou recursos JavaFX, conforme a localização.
│   │   │   ├── css/  # Folhas de estilo das telas JavaFX.
│   │   │   │   ├── agenda.css  # Estilos da agenda.
│   │   │   │   └── global.css  # Estilos compartilhados da aplicação.
│   │   │   ├── fxml/  # Descrições de interface JavaFX.
│   │   │   │   └── agenda-contatos.fxml  # Estrutura visual da agenda.
│   │   │   ├── database.properties  # Template de configuração JDBC; não contém credenciais locais.
│   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   ├── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # Guia de navegação e explicações desta pasta.
├── support/  # Documentação de apoio, referências e materiais complementares.
│   ├── .gitkeep  # Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── README.md  # Guia de navegação e explicações desta pasta.
├── .gitignore  # Regras para não versionar configurações locais e artefatos gerados.
├── LICENSE  # Texto da licença MIT.
├── pom.xml  # Configuração Maven, dependências e build do módulo.
└── README.md  # Guia de navegação e explicações desta pasta.
```
