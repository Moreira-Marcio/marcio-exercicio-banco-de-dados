## Comandos SQL

```sql
CREATE DATABASE tecinternet_escola_marcio CHARACTER SET utf8mb4;
```

```sql
CREATE TABLE professores(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    area-de-atuacao ENUM('design','desenvolvimento','infra'),
    curso_id INT NOT NULL --chave estrangeira--
);

```
```sql
CREATE TABLE cursos(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome_do_curso VARCHAR(50) NOT NULL,
    carga_horaria VARCHAR(45) NOT NULL,
    professor_id INT NULL --chave estrangeira--
);
```
```sql

