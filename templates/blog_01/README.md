
### Gerenciamento de Postagens em um Blog

Este sistema foi projetado para gerenciar as postagens de um blog, permitindo a criação, edição, categorização e publicação de conteúdo, além de gerenciar os autores e os comentários dos leitores. O sistema é composto por quatro entidades principais: **Postagens**, **Autores**, **Categorias**, e **Comentários**.

---

### **Diagrama ER**
![Diagrama ER](https://raw.githubusercontent.com/Enlighten-Brasil/en-schema-templates/main/templates/blog_01/diagram.svg)

#### 1. **Entidade: Postagens**

**Descrição**: A entidade "Postagens" é o núcleo do sistema, armazenando todas as informações sobre as postagens do blog. Isso inclui o título da postagem, o conteúdo, o autor, a data de publicação, o status da postagem e as categorias às quais pertence.

**Uso**: Essa entidade é utilizada para criar e gerenciar as postagens no blog, controlando desde a criação do conteúdo até a sua publicação e categorização.

**Atributos Principais**:
- **Título**: Nome da postagem.
- **Conteúdo**: O texto completo da postagem.
- **Autor**: O autor responsável pela criação da postagem.
- **Data de Publicação**: A data em que a postagem foi ou será publicada.
- **Status**: O estado atual da postagem, indicando se está em rascunho, publicada ou arquivada.
- **Categorias**: As categorias às quais a postagem pertence.
- **Comentários**: Os comentários feitos por leitores sobre a postagem.

---

#### 2. **Entidade: Autores**

**Descrição**: A entidade "Autores" gerencia as informações sobre os autores que contribuem com postagens no blog. Ela armazena dados como nome, biografia, e informações de contato dos autores.

**Uso**: Essa entidade permite gerenciar quem pode criar postagens no blog, mantendo um registro dos autores e suas respectivas contribuições.

**Atributos Principais**:
- **Nome**: Nome completo do autor.
- **Bio**: Uma breve biografia do autor.
- **E-mail**: Endereço de e-mail do autor para contato.
- **Avatar**: Imagem de perfil do autor.
- **Postagens**: As postagens que foram escritas pelo autor.

---

#### 3. **Entidade: Categorias**

**Descrição**: A entidade "Categorias" organiza as postagens do blog em diferentes temas ou assuntos, facilitando a navegação e a busca por conteúdo específico.

**Uso**: As categorias são usadas para classificar as postagens, permitindo aos leitores filtrar o conteúdo de acordo com seus interesses.

**Atributos Principais**:
- **Nome**: Nome da categoria.
- **Descrição**: Uma breve descrição sobre a categoria.
- **Postagens**: As postagens que pertencem a essa categoria.

---

#### 4. **Entidade: Comentários**

**

Descrição**: A entidade "Comentários" gerencia as interações dos leitores com as postagens, permitindo que deixem opiniões, feedbacks ou perguntas.

**Uso**: Essa entidade é utilizada para armazenar e moderar os comentários feitos pelos leitores nas postagens do blog, garantindo que o conteúdo gerado pelos usuários seja administrado de forma adequada.

**Atributos Principais**:
- **Autor**: Nome do autor do comentário.
- **E-mail**: Endereço de e-mail do autor do comentário.
- **Conteúdo**: O texto do comentário.
- **Data do Comentário**: A data em que o comentário foi feito.
- **Postagem**: A postagem à qual o comentário está relacionado.
- **Status**: O status do comentário, indicando se está aguardando moderação, foi aprovado ou rejeitado.

---

### Conclusão

Este sistema de gerenciamento de postagens em um blog foi desenhado para fornecer uma solução completa para a administração do conteúdo, autores, categorias e interações com leitores. As entidades descritas proporcionam uma estrutura robusta para manter um blog organizado e eficiente, facilitando tanto a criação quanto a navegação pelo conteúdo publicado.
