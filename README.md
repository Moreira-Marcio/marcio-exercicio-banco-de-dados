# Atividades de Banco de Dados - Etapa 1

*Antes de começar, crie um novo repositório chamado `seunome_atividade-banco-de-dados` para colocar sua produção.*

## Modelagem Conceitual

### A. Modelagem Conceitual

Usando o **BrModelo**, faça a **modelagem conceitual** de três entidades: **CURSO**, **PROFESSOR** e **ALUNO**.

- A entidade **CURSO** deve conter os seguintes atributos:

    - Identificador, obrigatório
    - Título, obrigatório
    - Carga horária, obrigatório
    - Identificador do Professor, opcional

- A entidade **PROFESSOR** deve conter os seguintes atributos:    

    - Identificador, obrigatório
    - Nome, obrigatório
    - Área de atuação (coloque entre parênteses: *design*, *desenvolvimento*, *infra*), obrigatório
    - Identificador do Curso, obrigatório

- A entidade **ALUNO** deve conter os seguintes atributos:    

    - Identificador, obrigatório
    - Nome, obrigatório
    - Data de nascimento, obrigatório
    - Primeira nota, obrigatório
    - Segunda nota, obrigatório
    - Identificador do Curso, obrigatório


#### Crie os relacionamentos de acordo com a cardinalidade indicada a seguir:

- **1 curso tem vários alunos**, portanto será usada a cardinalidade **1:N**. 

- **1 professor leciona somente 1 curso**, portanto será usada a cardinalidade **1:1**. 

- **1 curso é lecionado somente por 1 professor**, portanto será usada a cardinalidade **1:1**. 



