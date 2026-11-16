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

O ponto inicial é `src/main/java/com/salgaderia/app/model/`.

```text
src/main/java/com/salgaderia/app/model/  # Agrupa entidades, tipos de domínio e comportamentos encapsulados do sistema.
├── enums/  # Enumerações com comportamento e respectivos testes.
│   ├── CategoriaInsumo.java  # Categorias de insumos de fornecedores.
│   └── PerfilUsuario.java  # Perfis de acesso do usuário.
├── Cliente.java  # Contato especializado em cliente.
├── Contato.java  # Abstração comum de contatos.
├── Fornecedor.java  # Contato especializado em fornecedor.
├── README.md  # Guia de navegação e explicações desta pasta.
├── Usuario.java  # Abstração de usuário e permissões.
├── UsuarioAdmin.java  # Usuário administrativo.
├── UsuarioCliente.java  # Usuário vinculado a um cliente.
└── Validacao.java  # Validações compartilhadas das entidades.
```

[🏠 Voltar ao README principal](../../../../../../../README.md)
