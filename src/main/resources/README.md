[🏠 Início](../../../README.md) / [⬆️ main](../README.md) / 📂 resources

# 🎨 Recursos da aplicação

Agrupa telas FXML, estilos e configuração padrão consumidos pelo JavaFX e pela infraestrutura.

O arquivo database.local.properties é local e ignorado pelo Git; verifique se artefatos distribuídos não contêm credenciais.

## Explore as subpastas e arquivos

| Caminho | Conteúdo e responsabilidade |
|---|---|
| [css/](css/) | Folhas de estilo das telas JavaFX. |
| [fxml/](fxml/) | Descrições de interface JavaFX. |
| [database.properties](database.properties) | Template de configuração JDBC; não contém credenciais locais. |
| [README.md](README.md) | Guia de navegação e explicações desta pasta. |

## Árvore estrutural comentada

O ponto inicial é `src/main/resources/`.

```text
src/main/resources/  # Agrupa telas FXML, estilos e configuração padrão consumidos pelo JavaFX e pela infraestrutura.
├── css/  # Folhas de estilo das telas JavaFX.
│   ├── agenda.css  # Estilos da agenda.
│   └── global.css  # Estilos compartilhados da aplicação.
├── fxml/  # Descrições de interface JavaFX.
│   └── agenda-contatos.fxml  # Estrutura visual da agenda.
├── database.properties  # Template de configuração JDBC; não contém credenciais locais.
└── README.md  # Guia de navegação e explicações desta pasta.
```

[🏠 Voltar ao README principal](../../../README.md)
