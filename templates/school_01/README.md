### **Documentação**

Sistema de gerenciamento de escola, abrangendo as principais funcionalidades necessárias para administrar alunos, turmas, professores, disciplinas, horários, e notas.


### **Diagrama ER**
![Diagrama ER](https://raw.githubusercontent.com/Enlighten-Brasil/en-schema-templates/main/templates/school_01/diagram.svg)


1. **Alunos**
   - **Descrição**: A entidade "Alunos" é responsável por armazenar e gerenciar todas as informações dos alunos matriculados na escola. Isso inclui dados pessoais, matrícula, informações de contato, e notas obtidas nas disciplinas.
   - **Campos principais**:
     - **Matrícula**: Número de matrícula único do aluno, utilizado para identificá-lo no sistema.
     - **Nome do Aluno**: Nome completo do aluno.
     - **Data de Nascimento**: Data de nascimento do aluno.
     - **Endereço**: Endereço residencial do aluno.
     - **Turma**: Turma atual em que o aluno está matriculado.
     - **Notas**: Notas do aluno em diversas disciplinas.
     - **Contato do Responsável**: Informações de contato do responsável pelo aluno.

2. **Professores**
   - **Descrição**: A entidade "Professores" gerencia todas as informações relacionadas aos professores da escola. Isso inclui dados pessoais, disciplinas que lecionam e as turmas atribuídas.
   - **Campos principais**:
     - **Nome do Professor**: Nome completo do professor.
     - **CPF**: CPF único do professor.
     - **E-mail**: Endereço de e-mail do professor.
     - **Telefone**: Número de telefone de contato do professor.
     - **Disciplinas**: Disciplinas que o professor leciona.
     - **Turmas**: Turmas pelas quais o professor é responsável.

3. **Turmas**
   - **Descrição**: A entidade "Turmas" gerencia a estrutura das turmas da escola, incluindo o professor responsável, os alunos matriculados e as disciplinas associadas.
   - **Campos principais**:
     - **Código da Turma**: Código único que identifica a turma.
     - **Nome da Turma**: Nome que identifica a turma (ex: 3º Ano A).
     - **Ano Letivo**: Ano letivo da turma.
     - **Professor Responsável**: Professor responsável pela turma.
     - **Alunos**: Lista de alunos matriculados na turma.
     - **Disciplinas**: Disciplinas associadas à turma.

4. **Disciplinas**
   - **Descrição**: A entidade "Disciplinas" gerencia as matérias oferecidas pela escola. Inclui informações como nome da disciplina, carga horária e professores responsáveis.
   - **Campos principais**:
     - **Código da Disciplina**: Código único que identifica a disciplina.
     - **Nome da Disciplina**: Nome completo da disciplina.
     - **Carga Horária**: Carga horária total da disciplina em horas.
     - **Turmas**: Turmas em que a disciplina é lecionada.
     - **Professores**: Professores que lecionam a disciplina.

5. **Horários**
   - **Descrição**: A entidade "Horários" gerencia a distribuição das aulas ao longo da semana para cada turma e disciplina.
   - **Campos principais**:
     - **Turma**: Turma para a qual o horário é definido.
     - **Disciplina**: Disciplina que será lecionada no horário definido.
     - **Professor**: Professor responsável por lecionar a disciplina.
     - **Dia da Semana**: Dia da semana em que a aula ocorre.
     - **Hora de Início**: Hora de início da aula.
     - **Hora de Término**: Hora de término da aula.

6. **Notas**
   - **Descrição**: A entidade "Notas" gerencia o registro das notas atribuídas aos alunos em cada disciplina.
   - **Campos principais**:
     - **Aluno**: Aluno que recebeu a nota.
     - **Disciplina**: Disciplina para a qual a nota foi atribuída.
     - **Nota**: Nota obtida pelo aluno na disciplina.
     - **Data da Avaliação**: Data em que a avaliação foi realizada.
     - **Observação**: Observações adicionais sobre a avaliação ou nota.

---

Esse esquema e documentação fornecem uma visão detalhada e estruturada para um sistema de gerenciamento escolar, cobrindo os aspectos mais essenciais para a administração eficiente da escola. Se precisar de mais informações ou ajustes, estou à disposição.
