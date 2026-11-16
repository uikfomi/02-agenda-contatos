[🏠 Início](../README.md) / 📂 database

# 🗄️ Banco de dados

Reúne o schema, as migrações e os modelos de dados que apoiam a persistência JDBC da Ui K'Fomi.

Aplique os scripts na ordem descrita no README principal, em um banco de desenvolvimento, e faça backup antes de alterações em dados existentes. Senhas de seed nunca são apropriadas para produção.

## Explore as subpastas e arquivos

| Caminho | Conteúdo e responsabilidade |
|---|---|
| [DER/](DER/) | Modelo entidade-relacionamento e seus materiais. |
| [DL/](DL/) | Modelo lógico das tabelas e relações. |
| [scripts/](scripts/) | Schema e migrações SQL ordenadas pela evolução do sistema. |
| [README.md](README.md) | Guia de navegação e explicações desta pasta. |

## Árvore estrutural comentada

O ponto inicial é `database/`; cada comentário apresenta o caminho completo relativo à raiz do repositório.

```text
database/  # Reúne o schema, as migrações e os modelos de dados que apoiam a persistência JDBC da Ui K'Fomi.
├── DER/  # database/DER/ — Modelo entidade-relacionamento e seus materiais.
│   └── .gitkeep  # database/DER/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
├── DL/  # database/DL/ — Modelo lógico das tabelas e relações.
│   └── .gitkeep  # database/DL/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
├── scripts/  # database/scripts/ — Schema e migrações SQL ordenadas pela evolução do sistema.
│   ├── .gitkeep  # database/scripts/.gitkeep — Marcador que mantém a pasta no controle de versão; não contém dados de aplicação.
│   └── schema.sql  # database/scripts/schema.sql — Schema inicial MySQL usado pelo respectivo repositório.
└── README.md  # database/README.md — Guia de navegação e explicações desta pasta.
```

## 📌 Status do Conteúdo

As pastas abaixo estão reservadas e aguardam materiais finais; os arquivos `.gitkeep` apenas preservam a estrutura:

- `database/DER/` — Modelo entidade-relacionamento e seus materiais.
- `database/DL/` — Modelo lógico das tabelas e relações.

[🏠 Voltar ao README principal](../README.md)
