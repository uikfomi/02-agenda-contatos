# Ui K'fomi — 02-agenda-contatos

A **Ui K'fomi** é uma startup de Maranguape, Ceará, dedicada a soluções digitais para o setor de alimentação. Este módulo acadêmico de POO aborda agenda estratégica de clientes e fornecedores, com busca e gestão de contatos.

## Escopo

Extração do sistema integrado, com as dependências de domínio e persistência necessárias. Usa Java 17, JavaFX, MySQL com JDBC e HikariCP, seguindo MVC + Service + DAO. As pastas oficiais estão presentes na raiz; os recursos JavaFX ativos ficam em `src/main/resources`.

## Compilação e integração

Execute `mvn clean test-compile` na raiz. O arquivo `database/scripts/schema.sql` contém somente as tabelas necessárias para este recorte; configure credenciais locais em `src/main/resources/database.local.properties`, que não deve ser versionado. Este repositório é um **recorte para integração**, não um aplicativo independente completo: telas externas e navegação para outros módulos pertencem ao projeto integrado `03-projeto-livre`. Não há usuários de demonstração no script.

Licença MIT; consulte `LICENSE`.
