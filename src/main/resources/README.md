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

O ponto inicial é `src/main/resources/`; cada comentário apresenta o caminho completo relativo à raiz do repositório.

```text
src/main/resources/  # Agrupa telas FXML, estilos e configuração padrão consumidos pelo JavaFX e pela infraestrutura.
├── css/  # src/main/resources/css/ — Folhas de estilo das telas JavaFX.
│   ├── agenda.css  # src/main/resources/css/agenda.css — Estilos da agenda.
│   └── global.css  # src/main/resources/css/global.css — Estilos compartilhados da aplicação.
├── fxml/  # src/main/resources/fxml/ — Descrições de interface JavaFX.
│   └── agenda-contatos.fxml  # src/main/resources/fxml/agenda-contatos.fxml — Estrutura visual da agenda.
├── database.properties  # src/main/resources/database.properties — Template de configuração JDBC; não contém credenciais locais.
└── README.md  # src/main/resources/README.md — Guia de navegação e explicações desta pasta.
```

[🏠 Voltar ao README principal](../../../README.md)
