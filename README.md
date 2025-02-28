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


# Atividades de Banco de Dados - Etapa 2
## Modelagem Lógica
B. Modelagem Lógica
Usando o MySQL Workbench, faça a modelagem lógica a partir do que fez na modelagem conceitual, transformando as entidades em tabelas e seus atributos em colunas, além de definir os tipos de dados e relacionamentos.

🚨Fique atento(a) quanto ao nome das tabelas e das colunas. A sugestão segue sendo usar plural para tabelas e singular para colunas.

💡Sobre a entidade/tabela para Professores
Na modelagem conceitual da entidade PROFESSOR foi criado um atributo para a Área de atuação e indicado entre parênteses os valores design, desenvolvimento, infra.

Agora, na modelagem lógica, você deverá pesquisar qual tipo de dados permite indicar uma lista fixa de valores, aplicando ele na coluna da área de atuação.

Ao final, coloque o arquivo de modelagem lógica em seu repositório do exercício em versão original e também exportado em formato de imagem.
