### Documentação do Esquema de Gerenciamento de Livraria/Biblioteca

Este documento apresenta a descrição do esquema criado para o gerenciamento de uma livraria ou biblioteca. O esquema é composto por cinco entidades principais: **Livros**, **Membros**, **Empréstimos**, **Categorias**, e **Fornecedores**. Cada entidade possui um conjunto de atributos que descrevem suas características e funcionalidades. A seguir, são apresentadas as descrições de cada entidade e seus respectivos usos.

---

#### 1. **Entidade: Livros**

**Descrição**: A entidade "Livros" é responsável por armazenar e gerenciar todas as informações sobre os livros disponíveis na livraria ou biblioteca. Isso inclui detalhes essenciais como o título, autor, categoria, ISBN, e disponibilidade. Esta entidade é fundamental para manter um registro preciso do acervo literário.

**Principais Atributos**:
- **Título**: Nome do livro.
- **Autor**: Nome do autor do livro.
- **Categoria**: Categoria à qual o livro pertence (ex: Ficção, Não Ficção, Técnico, etc.).
- **ISBN**: Número ISBN do livro, utilizado para identificar de forma única cada título.
- **Editora**: Nome da editora que publicou o livro.
- **Ano de Publicação**: Ano em que o livro foi publicado.
- **Disponível**: Indica se o livro está disponível para empréstimo ou venda.
- **Localização**: Informação sobre onde o livro está localizado dentro da livraria ou biblioteca (ex: seção, prateleira).

**Uso**: Esta entidade é utilizada para gerenciar o acervo de livros, permitindo a fácil identificação e localização de cada título, bem como a verificação de sua disponibilidade para empréstimo ou venda.

---

#### 2. **Entidade: Membros**

**Descrição**: A entidade "Membros" é responsável pelo gerenciamento dos clientes ou usuários da livraria ou biblioteca. Esta entidade armazena informações pessoais e de contato dos membros, permitindo a gestão de suas interações, como empréstimos de livros.

**Principais Atributos**:
- **Nome**: Nome completo do membro.
- **CPF**: Número do CPF do membro, utilizado para identificação única.
- **E-mail**: Endereço de e-mail para contato.
- **Telefone**: Número de telefone para contato.
- **Endereço**: Endereço residencial do membro.
- **Data de Cadastro**: Data em que o membro foi registrado na livraria ou biblioteca.
- **Status**: Status do membro, indicando se está ativo ou inativo.

**Uso**: Esta entidade permite à livraria ou biblioteca gerenciar os seus clientes, rastrear seus empréstimos e manter suas informações de contato atualizadas.

---

#### 3. **Entidade: Empréstimos**

**Descrição**: A entidade "Empréstimos" gerencia o processo de empréstimo de livros dentro da livraria ou biblioteca. Esta entidade rastreia quais livros foram emprestados, para quais membros, e as datas de empréstimo e devolução.

**Principais Atributos**:
- **Livro**: O livro que está sendo emprestado.
- **Membro**: O membro que está realizando o empréstimo.
- **Data de Empréstimo**: Data em que o livro foi emprestado.
- **Data de Devolução Prevista**: Data prevista para a devolução do livro.
- **Data de Devolução Real**: Data em que o livro foi realmente devolvido.
- **Status**: Status do empréstimo (ex: Em andamento, Devolvido, Atrasado).

**Uso**: Esta entidade é usada para controlar e registrar o processo de empréstimo de livros, garantindo que os livros sejam devolvidos no prazo e permitindo o acompanhamento de eventuais atrasos.

---

#### 4. **Entidade: Categorias**

**Descrição**: A entidade "Categorias" organiza os livros em diferentes categorias, permitindo uma estrutura clara e eficiente para a catalogação e busca de títulos. Esta entidade facilita a navegação pelos livros disponíveis.

**Principais Atributos**:
- **Nome**: Nome da categoria (ex: Ficção, Não Ficção, Técnico, etc.).
- **Descrição**: Descrição breve sobre a categoria.

**Uso**: As categorias ajudam na organização dos livros, permitindo que clientes e membros encontrem mais facilmente os títulos de seu interesse.

---

#### 5. **Entidade: Fornecedores**

**Descrição**: A entidade "Fornecedores" gerencia as informações sobre os fornecedores de livros e outros materiais para a livraria ou biblioteca. Ela inclui detalhes como o nome do fornecedor, CNPJ, e informações de contato.

**Principais Atributos**:
- **Nome**: Nome do fornecedor.
- **CNPJ**: Número do CNPJ do fornecedor, utilizado para identificação.
- **Telefone**: Número de telefone para contato com o fornecedor.
- **E-mail**: Endereço de e-mail para contato.
- **Endereço**: Endereço completo do fornecedor.
- **Descrição**: Informações adicionais ou observações sobre o fornecedor.

**Uso**: Esta entidade é utilizada para manter um registro detalhado dos fornecedores, facilitando o gerenciamento de compras, recebimentos, e relacionamento com os fornecedores de materiais e livros.

---

### Conclusão

Este esquema foi projetado para fornecer uma solução abrangente para o gerenciamento de uma livraria ou biblioteca. Com as entidades **Livros**, **Membros**, **Empréstimos**, **Categorias**, e **Fornecedores**, o sistema cobre os principais aspectos necessários para manter o controle eficiente do acervo, dos clientes, e das operações diárias. As descrições e atributos de cada entidade foram cuidadosamente definidos para garantir clareza e funcionalidade na aplicação prática do sistema.
