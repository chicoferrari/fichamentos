# PADRONIZANDO AS NOMENCLATURAS

## Colunas

Colunas com nomes únicos e seguindo certos padrões ajudam na manutenção e na integridade dos dados, além de melhorar a forma como as tabelas se relacionam e também a aumentar a habilidade de busca de informações contidas no banco de dados. Pois nomes ambíguos, vagos ou genéricos demonstram que a estrutura da tabela não foi bem desenhada e pode causar muitos problemas.

### Boas práticas ao nomear colunas

* os nomes das colunas tem que fazer sentido para todos da organização, ou seja,deve-se evitar nomes que possam ter significados diferentes para grupos distintos;

* os nomes das colunas tem que ser claros - ‘telefone’, por exemplo, é um nome muito genérico que pode criar questionamentos como qual tipo de telefone a coluna representa, ou seja, usar nomes mais objetivos como ‘TelefoneResidencial’ evita questionamentos desse tipo;

* não usar acrônimos ou abreviações - acrônimos e abreviações podem não fazer sentido aos demais membros de uma organização;

* não usar nomes que implicam mais de uma característica;

* nomes das colunas tem que ser no singular, pois representam uma característica que precisa ser única do sujeito (ou evento) representado;

* cada coluna tem que manter um valor único, por exemplo, ao preencher o campo na coluna ‘TelefoneResidencial’ com o ‘ddd+numero_do_telefone’, dentre outras coisas, dificultaria filtrar os dados por ‘ddd’;

* colunas não podem armazenar um resultado de um cálculo ou concatenação, pois ao contrário do excel, a tabela em si, não será atualizada automaticamente;

* os nomes das colunas não devem se repetir em outras tabelas, assegurar nomes únicos para cada coluna evita, dentre outras coisas, a redundância, inconstância e erros ao visualizar os dados.

## Colunas com múltiplas partes e colunas com vários valores

São tipos de colunas que compromete a integridade dos dados, além de criar dificuldade de filtrar as informações nelas contidas:

* colunas com múltiplas partes, são colunas que possuem mais de uma característica armazenada, exemplos comuns são colunas com números de telefones com o ddd incluso, ou até mesmo endereços completos;

* colunas com vários valores são colunas que contém mais de um valor, geralmente separados por vírgulas.

## Tabelas

Tabelas bem desenhadas garante a integridade dos dados, se tornam simples de manipular e fácil de buscar alguma informação nelas contida. Enquanto as colunas representam as características de um objeto, as tabelas representam o objeto em si, se por algum motivo uma tabela representa mais do que um objeto, ela precisa ser dividida em tabelas menores.

### Boas práticas para nomear uma tabela

* seu nome tem que ser único e compreensível à toda organização;

* seu nome tem que ser claro e sem ambiguidades;

* seu nome não pode convergir com características físicas (arquivo, tabela, data, etc);

* não usar acrônimos e nem abreviações;

* não usar nomes que implicam em mais de um objeto;

* nomes das tabelas no plural (pois representam um conjunto de objetos).
Estrutura das tabelas:

* tabelas tem que representar um sujeito único - tal prática reduz o risco de problemas na integridade dos dados;

* certifique-se a tabela possua uma chave primária - pois elas identifica unicamente cada fileira da tabela e também é utilizada para relacionar com outras tabelas;

* certifique-se que a tabela não possua colunas duplicadas.

## Keys

A chave-primária possui a função de identificar unicamente cada fileira contida na tabela, assim como estabelece o relacionamento entre duas tabelas e cada tabela deve conter ao menos uma delas.

### Critérios para escolher a coluna para a chave-primária

* a coluna deve identificar unicamente cada fileira da tabela;

* a coluna deve conter apenas valores que não se repetem;

* a coluna não pode conter valores desconhecidos;

* valores de preenchimento opcional não são permitidos;

* os valores da coluna não podem ser modificados.

## Estabelecendo Relações Sólidas

Relacionamentos entre tabelas ocorrem quando as fileiras de uma tabela se associa com as fileiras de uma segunda tabela e podem ocorrer das seguintes formas:

* one-to-one;

* one-to-many;

* many-to-many.

Importante ressaltar que a coluna usada para vincular as tabelas precisam ser do mesmo tipo, por exemplo, se a chave primária for do tipo ‘inteiro’ a coluna com a chave estrangeira da segunda tabela também precisa ser do tipo ‘inteiro’.

## Regras de Exclusão

A regra de exclusão dita o que ocorrerá quando um usuário solicita a exclusão de uma fileira na tabela primária e divide-se em duas categorias:

### Restrito

Não permite a exclusão da fileira enquanto ela estiver vinculada à outra tabela, sendo necessário primeiro a exclusão das fileiras vinculadas para então excluir a fileira requisitada.

### Cascata

Exclui tanto a fileira da tabela primária quanto a fileira equivalente na tabela subordinada.

## Tipos de participação

Ao estabelecer uma relação entre duas tabelas, cada uma delas terá uma função diferente.

### Imprescindível

Pelo menos uma fileira tem que existir na tabela primária antes de inserir uma fileira na tabela subordinada.

### Opcional

Quando nenhum requisito é necessário.

## Nível de Participação

É possível limitar a quantidade de fileiras que podem ser vinculadas entre a tabela primária e a tabela subordinada em uma relação one-to-many.
