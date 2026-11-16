[🏠 Início](../../../../../../../README.md) / [⬆️ app](../README.md) / 📂 util

# 🔧 Infraestrutura

Concentra conexão, navegação, autenticação auxiliar e suporte às telas, quando presentes.

Mantenha as responsabilidades desta camada separadas das demais e consulte os arquivos relacionados antes de alterações.

## Explore as subpastas e arquivos

| Caminho | Conteúdo e responsabilidade |
|---|---|
| [ConnectionFactory.java](ConnectionFactory.java) | Pool HikariCP e transações JDBC. |
| [Navegacao.java](Navegacao.java) | Navegação entre telas FXML. |
| [README.md](README.md) | Guia de navegação e explicações desta pasta. |
| [TelaAutenticada.java](TelaAutenticada.java) | Contrato para telas com usuário autenticado. |

## Árvore estrutural comentada

O ponto inicial é `src/main/java/com/salgaderia/app/util/`.

```text
src/main/java/com/salgaderia/app/util/  # Concentra conexão, navegação, autenticação auxiliar e suporte às telas, quando presentes.
├── ConnectionFactory.java  # Pool HikariCP e transações JDBC.
├── Navegacao.java  # Navegação entre telas FXML.
├── README.md  # Guia de navegação e explicações desta pasta.
└── TelaAutenticada.java  # Contrato para telas com usuário autenticado.
```

[🏠 Voltar ao README principal](../../../../../../../README.md)
