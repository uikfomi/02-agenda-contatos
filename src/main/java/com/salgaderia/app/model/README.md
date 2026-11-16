[🏠 Início](../../../../../../../README.md) / [⬆️ app](../README.md) / 📂 model

# 🧱 Modelo de domínio

Agrupa entidades, tipos de domínio e comportamentos encapsulados do sistema.

Mantenha as responsabilidades desta camada separadas das demais e consulte os arquivos relacionados antes de alterações.

## Explore as subpastas e arquivos

| Caminho | Conteúdo e responsabilidade |
|---|---|
| [enums/](enums/) | Enumerações com comportamento e respectivos testes. |
| [Cliente.java](Cliente.java) | Contato especializado em cliente. |
| [Contato.java](Contato.java) | Abstração comum de contatos. |
| [Fornecedor.java](Fornecedor.java) | Contato especializado em fornecedor. |
| [README.md](README.md) | Guia de navegação e explicações desta pasta. |
| [Usuario.java](Usuario.java) | Abstração de usuário e permissões. |
| [UsuarioAdmin.java](UsuarioAdmin.java) | Usuário administrativo. |
| [UsuarioCliente.java](UsuarioCliente.java) | Usuário vinculado a um cliente. |
| [Validacao.java](Validacao.java) | Validações compartilhadas das entidades. |

## Árvore estrutural comentada

O ponto inicial é `src/main/java/com/salgaderia/app/model/`; cada comentário apresenta o caminho completo relativo à raiz do repositório.

```text
src/main/java/com/salgaderia/app/model/  # Agrupa entidades, tipos de domínio e comportamentos encapsulados do sistema.
├── enums/  # src/main/java/com/salgaderia/app/model/enums/ — Enumerações com comportamento e respectivos testes.
│   ├── CategoriaInsumo.java  # src/main/java/com/salgaderia/app/model/enums/CategoriaInsumo.java — Categorias de insumos de fornecedores.
│   └── PerfilUsuario.java  # src/main/java/com/salgaderia/app/model/enums/PerfilUsuario.java — Perfis de acesso do usuário.
├── Cliente.java  # src/main/java/com/salgaderia/app/model/Cliente.java — Contato especializado em cliente.
├── Contato.java  # src/main/java/com/salgaderia/app/model/Contato.java — Abstração comum de contatos.
├── Fornecedor.java  # src/main/java/com/salgaderia/app/model/Fornecedor.java — Contato especializado em fornecedor.
├── README.md  # src/main/java/com/salgaderia/app/model/README.md — Guia de navegação e explicações desta pasta.
├── Usuario.java  # src/main/java/com/salgaderia/app/model/Usuario.java — Abstração de usuário e permissões.
├── UsuarioAdmin.java  # src/main/java/com/salgaderia/app/model/UsuarioAdmin.java — Usuário administrativo.
├── UsuarioCliente.java  # src/main/java/com/salgaderia/app/model/UsuarioCliente.java — Usuário vinculado a um cliente.
└── Validacao.java  # src/main/java/com/salgaderia/app/model/Validacao.java — Validações compartilhadas das entidades.
```

[🏠 Voltar ao README principal](../../../../../../../README.md)
