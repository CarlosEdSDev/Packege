# Sistema de Gestão de Alunos, Disciplinas e Professores

## Estrutura do Banco de Dados

O sistema utiliza um banco de dados estruturado com as seguintes tabelas principais:

- **ALUNO**: Armazena os dados cadastrais dos alunos.
- **DISCIPLINA**: Contém informações sobre as disciplinas oferecidas pela instituição.
- **MATRICULA**: Relaciona os alunos às disciplinas em que estão matriculados.
- **PROFESSOR**: Registra as informações dos professores.
- **TURMA**: Vincula os professores às disciplinas que lecionam.

Além disso, o código implementa pacotes PL/SQL para agrupar funções e procedimentos que facilitam o gerenciamento dos dados.

## Passos para Executar os Scripts no Oracle

1. **Configuração Inicial**:
   - Abra o Oracle SQL Developer ou qualquer outro cliente compatível.
   - Conecte-se ao banco de dados utilizando suas credenciais.

2. **Criação das Tabelas**:
   - Execute o script que define as tabelas `ALUNO`, `DISCIPLINA`, `MATRICULA`, `PROFESSOR` e `TURMA`. Isso estabelecerá a estrutura básica do banco.

3. **Implementação dos Pacotes PL/SQL**:
   - Execute os scripts que criam os pacotes `PKG_ALUNO`, `PKG_DISCIPLINA` e `PKG_PROFESSOR`. Esses pacotes contêm procedures e funções para o gerenciamento eficiente de dados.

4. **Validação e Testes**:
   - Insira dados de teste e execute as procedures e funções disponibilizadas. Realize operações como o cadastro de alunos, matrículas e disciplinas, além de consultas como listagem de alunos maiores de 18 anos ou a quantidade de turmas de cada professor.

## Descrição dos Pacotes

### PKG_ALUNO

- **Exclusão de Aluno**: Remove um aluno e todas as suas matrículas associadas.
- **Listagem de Alunos Maiores de 18 Anos**: Retorna a lista de alunos com mais de 18 anos.
- **Listagem de Alunos por Curso**: Exibe os alunos matriculados em um curso específico.

### PKG_DISCIPLINA

- **Cadastro de Disciplina**: Adiciona uma nova disciplina ao sistema.
- **Total de Alunos por Disciplina**: Exibe o número de alunos matriculados por disciplina, limitando-se às disciplinas com mais de 10 alunos.
- **Média de Idade por Disciplina**: Calcula a idade média dos alunos matriculados em uma disciplina.
- **Listagem de Alunos por Disciplina**: Apresenta os alunos matriculados em uma disciplina específica.

### PKG_PROFESSOR

- **Total de Turmas por Professor**: Lista os professores e a quantidade de turmas que lecionam, considerando apenas aqueles com mais de uma turma.
- **Total de Turmas de um Professor**: Retorna a quantidade de turmas atribuídas a um professor específico, com base no seu ID.
- **Professor de uma Disciplina**: Informa o nome do professor responsável por determinada disciplina.

