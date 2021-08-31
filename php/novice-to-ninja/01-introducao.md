# PARTE I

## Introdução ao PHP

PHP é uma linguagem do tipo server-side e assim como o JavaScript, é possível utilizar em conjunto com o HTML com diferença de que no JavaScript o código é executado pelo próprio navegador, enquanto no PHP, o código é executado no servidor.

### Vantagens

* Não há riscos de incompatibilidade entre navegadores;

* Não permite o acesso de terceiros aos recursos do servidor;

* Reduz a carga do navegador, visto que os recursos são executados pelo servidor.

## Sintaxe e declarações

Um script em PHP é um conjunto de comandos que são executados em ordem e cada uma delas terminam em ponto e vírgula **(;)**.

```php
echo "This is a test!";
echo rand(1, 6);
```

### Variáveis

PHP é uma linguagem ‘loosely typed’, ou seja, uma variável que pode conter e armazenar qualquer tipo de dado sem a necessidade de uma declaração explícita.

Exemplo:

```php
$testVariable = 3;
$testVariable = 'three';
```

### Operadores

As atribuições dos operadores são usados para atribuir valores às variáveis sendo os mais comuns são os operadores aritméticos **(+, -, / e *)**.

Exemplo:

```php
$testVariable = 3 + 2; // o valor armazenado na variável é 5
$testVariable = 3 * 2; // o valor armazenado na variável é 6
```

### Comentários

Comentários permitem descrever o que o código faz. Quando iniciados com **‘//’** começam e terminam na mesma linha, enquanto ‘/\*’ e ‘\*/’ permitem comentários em blocos.

Exemplo:

```php
$testVariable = 'three' // isso é um comentário e é ignorado quando executado
```

## Estrutura de controle

Assim como outras linguagens de programação, o PHP possui recursos que permitem alterar o fluxo de controle.

### if

A mais comum das declarações e segue a seguinte estrutura:

```php
if (condição) {
    : código que será executado de a condição for verdadeira
}
```

Exemplo:

```php
$roll = rand(1, 6);
echo 'You rolled a ' . $roll;
if ($roll == 6) {
echo 'You win!';
}
```

### For Loops

Loops podem ser utilizados para repetir o mesmo trecho de código repetidas vezes e segue a seguinte estrutura:

```
for (contador; condição; incremento do contador) {
: código que será executado repetidamente enquanto a(s) condições forem verdadeiras
}
```

Exemplo:

```php
for ($count = 1; $count <= 10; $count++) {
    echo $count . ‘ ‘;
}
```

### While loops

Assim como as declarações do tipo **if … else** permitem escolher qual o conjunto de código que será executado, o **while** permite o uso da condição para determinar quantas vezes uma parte do código será executada:

```php
while (condição) {
: código que será executado repetidamente enquanto a(s) condições forem verdadeiras
}
```

Exemplo (contador até 10):

```php
for ($count <= 10) {
    echo $count . ‘ ‘;
    ++$count;
}
```

## Arrays

São variáveis que contém valores múltiplos. Para criar um array em PHP usa-se colchetes **"[ ]"** contendo os valores separados por vírgula:

```php
$myArray = [‘one’, 2, ‘3’]
```

Listas também podem ser criadas utilizando a variável de ambiente **array()**:

```php
$myArray = array(‘one’, 2, ‘3’)
```

Para saber qual item está armazenado na lista é preciso saber sua posição, geralmente as listas se iniciam por zero:

```php
$myArray = ['one', 2, '3'];

```

Neste caso, os itens de acordo com seus indexes são:

```php
echo $myArray[0];       // o item armazenado é 'one'
echo $myArray[1];       // o item armazenado é 2
echo $myArray[2];       // o item armazenado é '3'
```

Cada valor de uma lista é chamado de elemento e podem ser alterados ou adicionados da seguinte maneira:

```php
$myArray[1] = ‘two’
$myArray[1] = 4     // neste caso, o elemento na posição 1 foi alterado de 'two' para 4
$myArray[] = ‘five’ // neste caso, adiciona o elemento 'five' ao final da lista
```

## Interação e formulários

Atualmente, as páginas web, além de serem geradas automaticamente, precisam ser interativas. Porém, para criar interatividade em PHP é preciso entender como as informações podem ser enviadas no momento da solicitação de uma nova página e pode ser feito de duas maneiras:

* via links;
* via formulários.

### Enviando variáveis via links

```
http://www.google.com/search?h1=&q=ubuntu
```

\* No exemplo acima o termo de busca, indicado a partir do ponto de interrogação **(?)**, é enviado ao servidor junto com a requisição pela URL.

### Enviando variáveis via formulários

Frontend:

```html
<form action="name.php" method="post">
<label for="firstname">First name:</label>
<input type="text" name="firstname" id="firstname">
<label for="lastname">Last name:</label>
<input type="text" name="lastname" id="lastname">
<input type="submit" value="GO">
</form>
```

Backend:

```php
<?php
$firstname = $_POST['firstname'];
$lastname = $_POST['lastname'];
echo 'Welcome to our website, ' .
htmlspecialchars($firstname, ENT_QUOTES, 'UTF-8') . ' ' .
htmlspecialchars($lastname, ENT_QUOTES, 'UTF-8') . '!';
?>
```
