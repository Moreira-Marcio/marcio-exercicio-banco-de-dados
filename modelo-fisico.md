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
CREATE TABLE alunos(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(50) NOT NULL,
    data_de_nascimento DATE NOT NULL,
    primeira_nota DECIMAL(4,2) NOT NULL,
    segunda_nota DECIMAL(4,2) NOT NULL,
    curso_id INT NOT NULL--chave estrangeira--
);
```
```sql
ALTER TABLE professores
    
    ADD CONSTRAINT fk_professor_curso
      FOREIGN KEY (curso_id) REFERENCES cursos(id);
```
```sql
ALTER TABLE professores ADD curso_id INT NULL;
```
```sql
ALTER TABLE cursos ADD professor_id INT NULL;
```

```sql
ALTER TABLE cursos
    
    ADD CONSTRAINT fk_curso_professor1
      FOREIGN KEY (professor_id) REFERENCES professores(id);
```
```sql
ALTER TABLE alunos ADD curso_id INT NOT NULL;
```
```sql
ALTER TABLE alunos
    
    ADD CONSTRAINT fk_aluno_curso
      FOREIGN KEY (curso_id) REFERENCES cursos(id);
```
