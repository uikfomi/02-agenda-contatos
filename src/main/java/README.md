[🏠 Início](../../../README.md) / [⬆️ main](../README.md) / 📂 java

# ☕ Código Java

Organiza os pacotes Java desta parte do projeto.

Mantenha as responsabilidades desta camada separadas das demais e consulte os arquivos relacionados antes de alterações.

## Explore as subpastas e arquivos

| Caminho | Conteúdo e responsabilidade |
|---|---|
| [com/](com/) | Raiz de pacotes Java. [Abrir guia](com/README.md). |
| [README.md](README.md) | Guia de navegação e explicações desta pasta. |

## Árvore estrutural comentada

O ponto inicial é `src/main/java/`.

```text
src/main/java/  # Organiza os pacotes Java desta parte do projeto.
├── com/  # Raiz de pacotes Java.
│   ├── salgaderia/  # Pacote da aplicação Salgaderia.
│   │   ├── app/  # Componentes da aplicação e suas camadas.
│   │   │   ├── controller/  # Controllers das telas e testes de interface, conforme a localização.
│   │   │   │   └── AgendaController.java  # Interface da agenda de clientes e fornecedores.
│   │   │   ├── dao/  # Contratos de acesso a dados ou testes JDBC.
│   │   │   │   ├── impl/  # Implementações JDBC dos contratos DAO, com comandos parametrizados.
│   │   │   │   │   └── ContatoDAOImpl.java  # Operações JDBC de contatos com filtros de clientes e fornecedores.
│   │   │   │   └── ContatoDAO.java  # Contrato para cadastro, edição, exclusão e busca filtrada de contatos.
│   │   │   ├── exception/  # Exceções personalizadas de domínio e persistência.
│   │   │   │   └── PersistenciaException.java  # Encapsula erro de persistência.
│   │   │   ├── model/  # Entidades de domínio ou testes dessas entidades.
│   │   │   │   ├── enums/  # Enumerações com comportamento e respectivos testes.
│   │   │   │   │   ├── CategoriaInsumo.java  # Categorias de insumos de fornecedores.
│   │   │   │   │   └── PerfilUsuario.java  # Perfis de acesso do usuário.
│   │   │   │   ├── Cliente.java  # Contato especializado em cliente.
│   │   │   │   ├── Contato.java  # Abstração comum de contatos.
│   │   │   │   ├── Fornecedor.java  # Contato especializado em fornecedor.
│   │   │   │   ├── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   ├── Usuario.java  # Abstração de usuário e permissões.
│   │   │   │   ├── UsuarioAdmin.java  # Usuário administrativo.
│   │   │   │   ├── UsuarioCliente.java  # Usuário vinculado a um cliente.
│   │   │   │   └── Validacao.java  # Validações compartilhadas das entidades.
│   │   │   ├── service/  # Contratos, regras de negócio e testes de serviços.
│   │   │   │   ├── impl/  # Implementações de regras e orquestração dos serviços.
│   │   │   │   │   └── AgendaServiceImpl.java  # Valida e coordena cadastro, busca e alterações de contatos pela camada DAO.
│   │   │   │   └── AgendaService.java  # Contrato de operações e busca da agenda de clientes e fornecedores.
│   │   │   ├── util/  # Conexão, autenticação auxiliar e navegação.
│   │   │   │   ├── ConnectionFactory.java  # Pool HikariCP e transações JDBC.
│   │   │   │   ├── Navegacao.java  # Navegação entre telas FXML.
│   │   │   │   ├── README.md  # Guia de navegação e explicações desta pasta.
│   │   │   │   └── TelaAutenticada.java  # Contrato para telas com usuário autenticado.
│   │   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   │   └── README.md  # Guia de navegação e explicações desta pasta.
│   └── README.md  # Guia de navegação e explicações desta pasta.
└── README.md  # Guia de navegação e explicações desta pasta.
```

[🏠 Voltar ao README principal](../../../README.md)
