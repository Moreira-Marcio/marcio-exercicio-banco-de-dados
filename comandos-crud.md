## comandos curd exercicio

```sql
INSERT INTO cursos(nome_do_curso, carga_horaria)
VALUES(
    'Front-End', 
    '40 horas'


),
(
    'Back-End', 
    '80 horas'


),

(
    'UX/UI Design', 
    '30 horas'


),
(
    'Figma', 
    '10 horas'


),

(
    'Redes de Computadores', 
    '100 horas'


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

