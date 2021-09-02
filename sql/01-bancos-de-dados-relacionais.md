# BANCO DE DADOS RELACIONAIS

## Definição

Banco de dados é uma coleção organizada de dados.

## Tipos de bancos de dados

Operacional

* amplamente utilizada pelas organizações, tem a função de coletar, modificar e manter os dados;
* é do tipo dinâmico, ou seja, está sempre mudando e reflete a informação em tempo real.

Analítico

* armazena e rastreia o histórico e dados no decorrer do tempo;
* utilizado para visualizar o fluxo de dados em determinados períodos ou elaborar estratégias e projeções sobre um determinado negócio;
* é do tipo estático, visto que raramente seus dados são alterados.

## Sistemas de Bancos de Dados Relacionais

Um sistema de gerenciamento de banco de dados relacionais (RDBMS) é uma aplicação usada para criar, manter, modificar e manipular um banco de dados.

## Anatomia de um Banco de Dados Relacional

No modelo relacional os dados são armazenados em relações, que são visualizadas pelos usuários como tabelas.

Cada relação é composta por tuplas (gravações ou fileiras) e atributos (campos ou colunas).

### Tabelas

* principal estrutura do banco de dados;

* cada tabela representa um único e específico objeto;

* o sujeito que a tabela representa pode ser um objeto ou um evento.

Objetos - a tabela representa algo tangível.

Eventos - a tabela representa algo que ocorreu em um determinado ponto em uma linha do tempo.

### Colunas

É a menor estrutura da tabela e representa as características do objeto ao qual pertence.

### Fileiras

* uma fileira representa o objeto da tabela;

* é composto pela sequência de colunas da tabela indiferente se tem algum valor atribuído ou não;

* devido a estrutura da tabela, cada fileira é identificada pelo banco de dados por um valor único.

### Keys

* são colunas especiais que executam uma função específica na tabela;

* o tipo de chave determina seu propósito e as mais utilizadas são as chaves-primária e chaves-estrangeira.

chave-primária - atribui um valor único à coluna que identifica cada fileira de uma tabela.

chave-estrangeira - é utilizada para relacionar duas tabelas distintas. São importantes pois asseguram a integridade das relações entre as tabelas.

### Visualizações

* permite a visualização de uma tabela virtual composta por colunas de uma ou mais tabelas do banco de dados;

* permite a visualização do banco de dados através de várias perspectivas provendo flexibilidade para trabalhar com os dados.

## Tipos de Relações

Se as fileiras de uma tabela podem ser associadas de alguma maneira às fileiras de outra tabela, pode se dizer que há uma relação entre elas. E a maneira que elas se relacionam podem ser divididas em três:

### One-to-one

Relações one-to-one são estabelecidas quando uma única fileira da tabela primária está atrelada a uma única fileira da tabela subordinada e vice-versa (seu uso não é muito comum e geralmente é utilizada quando uma tabela é dividida em duas parte, para assim, manter a confidencialidade de parte dos dados).

### One-to-many

Relações one-to-many são estabelecidas quando uma única fileira da tabela primária pode ser atrelada a várias fileiras da tabela subordinada. Porém, uma fileira da tabela subordinada só pode ser atrelada a uma única fileira da tabela primária.

### Many-to-many

Relações many-to-many são estabelecidas quando uma fileira da tabela primária se relaciona com várias fileiras da segunda subordinada e vice-versa (também chamada de linking table).
