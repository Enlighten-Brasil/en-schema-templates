Aqui está uma versão aprimorada da documentação para o sistema de gerenciamento de hotel:

---

### Documentação do Sistema de Gerenciamento de Hotel

Este sistema de gerenciamento de hotel foi projetado para otimizar e automatizar as operações diárias de um hotel, abrangendo desde o gerenciamento de reservas até a administração de quartos e funcionários. O sistema é composto por várias entidades que interagem entre si para garantir um fluxo de trabalho eficiente e uma experiência aprimorada para hóspedes e funcionários. Abaixo, detalhamos as principais entidades do sistema e suas funcionalidades.

---

### **Diagrama ER**
![Diagrama ER](https://raw.githubusercontent.com/Enlighten-Brasil/en-schema-templates/main/templates/hotel_01/diagram.svg)

#### 1. **Reservas**
- **Descrição**: A entidade **Reservas** é responsável por gerenciar todas as reservas feitas pelos hóspedes. Inclui detalhes essenciais como as datas de check-in e check-out, o quarto reservado, e o status atual da reserva.
- **Campos Principais**:
  - **Hóspede** (`hospede`): Relação com a entidade *Hóspedes*, indicando quem realizou a reserva.
  - **Quarto** (`quarto`): Relação com a entidade *Quartos*, especificando o quarto reservado.
  - **Data de Check-In** (`data_checkin`): Data e hora previstas para a entrada do hóspede no hotel.
  - **Data de Check-Out** (`data_checkout`): Data e hora previstas para a saída do hóspede do hotel.
  - **Status da Reserva** (`status_reserva`): Estado atual da reserva, podendo ser "Confirmada", "Pendente" ou "Cancelada".
  - **Total do Pagamento** (`total_pagamento`): Valor total da reserva, incluindo todos os custos aplicáveis.

---

#### 2. **Hóspedes**
- **Descrição**: A entidade **Hóspedes** armazena informações detalhadas sobre os clientes do hotel, incluindo dados pessoais, informações de contato, e o histórico de todas as reservas feitas pelo hóspede.
- **Campos Principais**:
  - **Nome Completo** (`nome`): Nome completo do hóspede, necessário para identificação.
  - **E-mail** (`email`): Endereço de e-mail do hóspede, utilizado para comunicação e envio de confirmações de reserva.
  - **Telefone** (`telefone`): Número de telefone para contato direto com o hóspede.
  - **Documento de Identidade** (`documento`): Número do documento de identidade do hóspede, necessário para o registro oficial.
  - **Histórico de Reservas** (`historico_reservas`): Relação com a entidade *Reservas*, exibindo todas as reservas feitas pelo hóspede.

---

#### 3. **Quartos**
- **Descrição**: A entidade **Quartos** gerencia todos os quartos disponíveis no hotel, incluindo informações sobre o tipo de quarto, sua capacidade, disponibilidade, e o preço da diária.
- **Campos Principais**:
  - **Número do Quarto** (`numero_quarto`): Identificação única para cada quarto no hotel.
  - **Tipo de Quarto** (`tipo_quarto`): Categoria do quarto, como "Individual", "Duplo", ou "Suíte".
  - **Capacidade** (`capacidade`): Número máximo de hóspedes que o quarto pode acomodar.
  - **Preço da Diária** (`preco_diaria`): Valor cobrado por noite para estadia no quarto.
  - **Disponibilidade** (`disponibilidade`): Indica se o quarto está disponível para reserva.

---

#### 4. **Serviços Adicionais**
- **Descrição**: A entidade **Serviços Adicionais** cobre todos os serviços extras oferecidos pelo hotel, como serviço de quarto, lavanderia, e transporte. Esses serviços podem ser adicionados à conta do hóspede durante a estadia.
- **Campos Principais**:
  - **Nome do Serviço** (`nome_servico`): Identificação do serviço adicional oferecido pelo hotel.
  - **Descrição** (`descricao`): Explicação detalhada do serviço, incluindo o que ele cobre e suas vantagens.
  - **Preço** (`preco`): Custo do serviço adicional, que será adicionado à conta do hóspede.

---

#### 5. **Funcionários**
- **Descrição**: A entidade **Funcionários** gerencia os dados dos colaboradores do hotel, abrangendo informações sobre seus cargos, horários de trabalho, e meios de contato.
- **Campos Principais**:
  - **Nome Completo** (`nome`): Nome do funcionário, necessário para identificação.
  - **Cargo** (`cargo`): Posição do funcionário no hotel, como "Recepcionista", "Gerente", "Camareira", etc.
  - **Telefone** (`telefone`): Número de telefone para contato com o funcionário.
  - **E-mail** (`email`): Endereço de e-mail profissional do funcionário.
  - **Horários de Trabalho** (`horarios_trabalho`): Relação com a entidade *Horários de Trabalho*, detalhando os turnos atribuídos ao funcionário.

---

#### 6. **Horários de Trabalho**
- **Descrição**: A entidade **Horários de Trabalho** organiza os turnos e horários dos funcionários, garantindo que todas as funções essenciais do hotel sejam cobertas durante o expediente.
- **Campos Principais**:
  - **Dia da Semana** (`dia_semana`): Dia específico da semana em que o funcionário trabalha.
  - **Hora de Início** (`hora_inicio`): Hora exata de início do turno do funcionário.
  - **Hora de Término** (`hora_fim`): Hora exata de término do turno do funcionário.
  - **Funcionário** (`funcionario`): Relação com a entidade *Funcionários*, vinculando o horário ao colaborador responsável.

---

### Conclusão

Este sistema de gerenciamento de hotel foi elaborado para cobrir todas as necessidades operacionais de um hotel, desde a reserva de quartos até o gerenciamento dos funcionários e serviços adicionais. Com este sistema, o hotel pode assegurar que todas as informações sejam organizadas e facilmente acessíveis, melhorando a eficiência operacional e proporcionando uma experiência mais satisfatória para os hóspedes.
