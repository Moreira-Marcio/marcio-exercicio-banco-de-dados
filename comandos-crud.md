## comandos curd exercicio

```sql
INSERT INTO cursos(nome_do_curso, carga_horaria)
VALUES(
    'Front-End', 
    40 


),
(
    'Back-End', 
    80


),

(
    'UX/UI Design', 
    30


),
(
    'Figma', 
     10


),

(
    'Redes de Computadores', 
     100


);
```
```sql

INSERT INTO professores(nome, area_de_atuacao,curso_id)
VALUES(
    'Jon Oliva',
     'infra',
     5

);
```
```sql

INSERT INTO professores(nome, area_de_atuacao,curso_id)
VALUES(
    'Lemmy Kilmister',
     'design',
     4

),
(
 'Ozzy Osbourne',
 'desenvolvimento',
 3   
),
(
 'Neil Peart',
 'design',
 4  
),
(
 'David Gilmour',
 'desenvolvimento',
 3   
);
```
```sql
UPDATE cursos SET professor_id = 5
WHERE  id = 1;
```
```sql
UPDATE cursos SET professor_id = 4
WHERE  id = 2;
```
```sql
UPDATE cursos SET professor_id = 3
WHERE  id = 3;
```
```sql
UPDATE cursos SET professor_id = 2
WHERE  id = 4;
```
```sql
UPDATE cursos SET professor_id = 1
WHERE  id = 5;
```
```sql
INSERT INTO alunos(nome, data_de_nascimento,primeira_nota,segunda_nota, curso_id)
VALUES(
    'jose',
    '2000-07-10',
    08.25,
    05.50,
    1
),
(
    'mario',
    '1985-09-07',
    10.00,
    06.00,
    2
),
(
    'lucas',
    '2003-08-20',
    08.25,
    05.50,
    5
),
(
    'jonas',
    '1993-10-02',
    0.00,
    10.00,
    4
),
(
    'fabio',
    '1998-07-10',
    07.25,
    06.50,
    3
);

```
```sql
SELECT nome, data_de_nascimento FROM alunos
WHERE data_de_nascimento < '2009-01-01';

```
```sql
INSERT INTO alunos(nome, data_de_nascimento,primeira_nota,segunda_nota, curso_id)
VALUES (
    'paula',
    '2012-07-10',
    07.25,
    06.50,
    3
);
```
```sql
   SELECT nome,SUM(primeira_nota + segunda_nota) AS soma_notas,
    AVG(primeira_nota + segunda_nota/2) AS media_notas
FROM
    alunos
GROUP BY
    alunos.id, nome;
```
```sql
SELECT curso.nome_do_curso, (curso.carga_horaria * 0.25) AS limite_faltas
FROM cursos AS curso
ORDER BY curso.nome_do_curso;
```
```sql
SELECT nome
FROM professores
WHERE area_de_atuacao = 'desenvolvimento';
```
```sql
SELECT area_de_atuacao, COUNT(*) AS quantidade_professores
FROM professores
WHERE area_de_atuacao IN ('design', 'infra', 'desenvolvimento')
GROUP BY area_de_atuacao;
```
```sql
SELECT
    a.nome AS aluno,
    c.nome_do_curso AS curso,
    c.carga_horaria
FROM
    alunos AS a
JOIN
    cursos AS c ON a.curso_id = c.id;
```
```sql
SELECT professores.nome AS professor,
    cursos.nome_do_curso AS curso
FROM professores
LEFT JOIN cursos ON professores.id = cursos.id_professor
ORDER BY professores.nome;
```
```sql
SELECT 
    alunos.nome AS Nome_Aluno, 
    cursos.nome_do_curso AS Curso, 
    professores.nome AS Professor
FROM alunos
JOIN cursos ON alunos.curso_id = cursos.id
JOIN professores ON cursos.professor_id = professores.id;

 ```  

 ```sql 
SELECT 
    cursos.nome_do_curso AS Curso, 
    COUNT(alunos.id) AS Quantidade_Alunos
FROM cursos
LEFT JOIN alunos ON cursos.id = alunos.curso_id
GROUP BY cursos.nome_do_curso
ORDER BY Quantidade_Alunos DESC;
  ``` 
 ```sql 
SELECT
    alunos.nome AS Nome_Aluno,
    alunos.primeira_nota + alunos.segunda_nota AS Soma_Notas,
    (alunos.primeira_nota + alunos.segunda_nota) / 2.0 AS Media,
    cursos.nome_do_curso AS Curso
FROM alunos
JOIN cursos ON alunos.curso_id = cursos.id
WHERE cursos.nome_do_curso IN ('Front-End', 'Back-End')
ORDER BY alunos.nome;
```


 ```sql
UPDATE cursos
SET nome_do_curso = 'Adobe XD', carga_horaria = 15
WHERE nome_do_curso = 'Figma';
 ```
 ```sql
 DELETE FROM alunos
WHERE curso_id = (SELECT id FROM cursos WHERE nome_do_curso = 'Redes de Computadores');

DELETE FROM alunos
WHERE curso_id = (SELECT id FROM cursos WHERE nome_do_curso = 'UX/UI');
```
```sql
SELECT 
    alunos.nome AS Nome_Aluno, 
    cursos.nome_do_curso AS Curso
FROM alunos
JOIN cursos ON alunos.curso_id = cursos.id
ORDER BY Nome_Aluno;
```
```sql
SELECT 
    nome AS Nome_Aluno, 
    TIMESTAMPDIFF(YEAR, data_de_nascimento, CURDATE()) AS Idade
FROM alunos;
```

```sql
SELECT 
    alunos.nome AS Nome_Aluno,
    alunos.primeira_nota + alunos.segunda_nota AS Soma_Notas,
    (alunos.primeira_nota + alunos.segunda_nota) / 2.0 AS Media
FROM alunos
JOIN cursos ON alunos.curso_id = cursos.id
GROUP BY alunos.id
HAVING Media >= 7;
```