# en-schema-templates
Repositorio para templates de modelos do Enspace


### **Documentação para Orientação de Preenchimento e Entendimento do Schema de Models do Enspace**

---

#### **Introdução**

Este documento tem como objetivo orientar os usuários na compreensão e correto preenchimento do schema JSON utilizado para gerenciar diversas entidades dentro de um sistema de gestão jurídica. As entidades descritas neste schema abrangem desde processos judiciais até a gestão de clientes, juízes, partes envolvidas, e documentação associada.

---

### **Estrutura Geral do Schema**

O schema JSON é composto por diferentes entidades, cada uma representada como um objeto com os seguintes componentes principais:

- **`name`**: Nome técnico da entidade, usado internamente no sistema.
- **`info`**: Metadados da entidade, incluindo nomes de exibição, descrição, e ícone associado.
- **`attributes`**: Conjunto de atributos que definem os campos disponíveis dentro de cada entidade. Esses atributos podem incluir tipos de dados, validações, e relações com outras entidades.

---

### **Componentes do Schema**

#### **1. `name`**

- **Descrição:** O campo `name` identifica de forma única a entidade dentro do sistema. Ele é utilizado como uma referência técnica e não deve ser alterado sem a devida compreensão dos impactos no sistema.

- **Exemplo:** `"name": "processos"`

#### **2. `info`**

- **Descrição:** O campo `info` fornece informações descritivas sobre a entidade, que são utilizadas para exibição na interface do usuário.

- **Subcampos:**
  - **`displayName`**: Nome da entidade que será exibido ao usuário.
  - **`singularName`**: Nome singular da entidade.
  - **`pluralName`**: Nome plural da entidade.
  - **`description`**: Descrição da finalidade da entidade.
  - **`icon`**: Ícone associado à entidade, utilizado na interface para facilitar a identificação visual.

- **Exemplo:**
  ```json
  "info": {
    "displayName": "Processos",
    "singularName": "Processo",
    "pluralName": "Processos",
    "description": "Processos gerenciados pela empresa",
    "icon": "file"
  }
  ```

#### **3. `attributes`**

- **Descrição:** O campo `attributes` define os diversos campos que compõem a entidade. Cada campo tem propriedades específicas que determinam seu comportamento e validação.

- **Subcampos Comuns:**
  - **`label`**: Nome do campo exibido ao usuário.
  - **`type`**: Tipo de dado que o campo aceita (e.g., texto, dropdown, data).
  - **`validation`**: Regras de validação aplicadas ao campo (e.g., obrigatório, valor único).
  - **`options`**: Lista de opções disponíveis para campos do tipo dropdown.
  - **`section`**: Seção do formulário onde o campo será exibido.
  - **`width`**: Largura do campo no layout do formulário, definida em frações (e.g., "2/12").

- **Exemplo:**
  ```json
  "attributes": {
    "tipo": {
      "label": "Tipo",
      "type": "EnlDropdown",
      "options": ["Judicial", "Extrajudicial"],
      "section": "Principal",
      "width": "2/12"
    },
    "titulo": {
      "label": "Título",
      "type": "inputText",
      "validation": "required",
      "section": "Principal",
      "width": "5/12"
    }
  }
  ```

---

### **Guia de Preenchimento de Atributos**

#### **1. Campos de Texto (`inputText`)**

- **Uso:** Utilizado para entradas de texto livre.
- **Validações Comuns:**
  - **`required`**: O campo é obrigatório.
  - **`uniqueValue`**: O valor deve ser único no contexto da entidade.

- **Exemplo de Preenchimento:**
  ```json
  "titulo": {
    "label": "Título",
    "type": "inputText",
    "validation": "required",
    "section": "Principal",
    "width": "5/12"
  }
  ```

#### **2. Dropdowns (`EnlDropdown`)**

- **Uso:** Permite ao usuário selecionar uma opção de uma lista pré-definida.
- **Atributos Importantes:**
  - **`options`**: Lista de opções disponíveis para seleção.
  - **`validation`**: Pode incluir a regra `required` para tornar o campo obrigatório.

- **Exemplo de Preenchimento:**
  ```json
  "tipo": {
    "label": "Tipo",
    "type": "EnlDropdown",
    "options": ["Judicial", "Extrajudicial"],
    "section": "Principal",
    "width": "2/12"
  }
  ```

#### **3. Campos de Data (`EnlCalendar`)**

- **Uso:** Utilizado para selecionar datas em um calendário.
- **Validações Comuns:**
  - **`required`**: O campo é obrigatório.

- **Exemplo de Preenchimento:**
  ```json
  "data": {
    "label": "Data",
    "type": "EnlCalendar",
    "validation": "required"
  }
  ```

#### **4. Relacionamentos (`EnRel` e `EnRelMulti`)**

- **Uso:** Define relações entre entidades, como `oneToOne` (um para um) ou `oneToMany` (um para muitos).
- **Atributos Importantes:**
  - **`relation`**: Tipo de relacionamento (e.g., `oneToOne`, `oneToMany`).
  - **`target`**: Entidade alvo do relacionamento.

- **Exemplo de Preenchimento:**
  ```json
  "cliente": {
    "label": "Cliente",
    "type": "EnRel",
    "relation": "oneToOne",
    "target": "models:clientes",
    "section": "Principal",
    "width": "4/12"
  }
  ```

#### **5. Máscaras de Entrada (`masks`)**

- **Uso:** Define formatos de entrada para campos de texto que requerem uma estrutura específica (e.g., CPF, CNPJ).
- **Exemplo de Preenchimento:**
  ```json
  "cpf_cnpj": {
    "label": "CPF / CNPJ",
    "type": "inputText",
    "validation": "required",
    "masks": ["###.###.###-##", "##.###.###/####-##"]
  }
  ```

---

### **Seções e Layout**

- **Seções (`section`)**: Os campos são agrupados em seções para facilitar a organização visual e o preenchimento do formulário. Exemplos incluem `Principal`, `Partes`, `Andamentos`, etc.
  
- **Layout e Distribuição de Campos (`width`)**: Define a largura de cada campo no formulário, utilizando frações de 12 como padrão (e.g., "2/12" para ocupar 2 de 12 colunas).

---

### **Boas Práticas e Considerações**

- **Validação e Consistência:** Assegure-se de que todos os campos obrigatórios estejam preenchidos e que os dados estejam formatados corretamente, conforme as regras de validação especificadas.
- **Uso de Relacionamentos:** Quando um campo estiver relacionado a outra entidade, verifique a consistência dos dados e as relações existentes para evitar conflitos ou duplicações.
- **Testes e Verificação:** Antes de implementar ou alterar o schema, realize testes para garantir que as modificações atendam às necessidades do sistema sem comprometer a integridade dos dados.

---

### **Conclusão**

Este guia fornece uma visão detalhada do preenchimento e entendimento do schema JSON utilizado no sistema de gestão jurídica. Seguindo essas orientações, os usuários poderão configurar e utilizar as entidades e seus atributos de forma eficiente, garantindo um fluxo de trabalho organizado e consistente.
