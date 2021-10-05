# JavaScript
Javascript é como nós chamamos a linguagem (mas isso é o trademark da Oracle), o nome oficial da linguagem é ECMAScript (ES) é a abreviação.

## Tipos de Dados

### Primitive
- String: conjunto de caracteres
  - (" ") aspas duplas
  - (' ') aspas simples
  - (` `) template string

- Number: números
  - Int
  - Float
  - NaN: not a number
  - Infinity: infinito

- Boolean: true ou false

- Undefined: indefinido

- Symbol

- BigInt

### Structural
- Objeto: {propriedade: "valor"}
  - [Funções de Objetos]()

- Array: []
  - [Iterando Arrays]()

- [Functions](functions.md)

### Structural Root Primitive
- Null: nulo

## Variáveis
JS é fracamente tipada
- [Var](#var), [Let e const](#Let-e-Const)
- Destructuring
  - Arrays e Objetos
- [Rest e Spread Operator](rest-spread-operator.md)

### Statements do JavaScript
  - [Controle de Fluxo](control_flow.md)
    - If, Switch, Throw e try/catch
  - [Estruturas de Repetição](repeticao.md)
    - For, While, For of, For in
  - Array, Objeto
  - Métodos de array e objeto

### [Expressões e Operadores](expressions_operators.md)



### Promises
  - Fetch
  - Async/Await

## Scope
- Determina a visibilidade de alguma variável
```js
// escopo global
{
  //escopo local
  //block statement
}
```

### Hoisting
  - Içamento de funções e variáveis para o topo do código, isso declara as variáveis e funções em memória e permite que você use uma função/variável antes mesmo de declara-la.

```js
console.log(x);
// saída será undefined
{
  var x = 1;
}

//Por baixo dos panos, com hoisting
var x;
console.log(x);
{
  x = 1;
}
```

### Var
- Tem o escopo global

```js
(() => {
  console.log(`Valor dentro da função ${test}`);

  if(true){
    var test = 'example';
    console.log(`Valor dentro do if ${test}`);
  }

  console.log(`Valor após execução do if ${test}`);
})();
```

### Let e Const
- Escopo de bloco
- Sofrem hoisting para o topo do bloco que foram definidas
  - Diferente do var, ao ser chamada antes de sua criação, é apontado um erro
- Const não pode ter seu valor reatribuido, enquanto let pode

```js
// LET
(() => {
  let testLet = 'valor função'
  console.log(`Valor dentro da função ${testLet}`);

  if(true){
    let testLet = 'valor if';
    console.log(`Valor dentro do if ${testLet}`);
  }

  console.log(`Valor após execução do if ${testLet}`);
})();

// CONST
const name = 'Leandro'; //não pode alterar o nome

const user = {
  name: 'Leandro'
}

user.name = 'Outro Nome'; //se for objeto, pode alterar

const persons = ['Pessoa 1', 'Pessoa 2', 'Pessoa 3'];

persons[1] = 'Pessoa X'; // array também pode alterar
console.log(persons);
```


## DOM - Document Object Model
- É o HTML convertido em JS
  - JS usa a DOM para se conectar ao HTML
    - Com isso, é possível manipular o HTML através do JS
- Estrutura de dados do tipo árvore, criada pelo browser

- [Selecionar Elementos](dom.md/#Selecionando-Elementos)
- [Manipular Conteúdos](dom.md/#Manipulando-Conteúdos)