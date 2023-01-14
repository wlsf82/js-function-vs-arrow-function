# JavaScript - function versus arrow function

**_Este texto foi produzido pelo [ChatGPT](https://chat.openai.com/) com co-autoria de [Walmyr Lima e Silva Filho](https://github.com/wlsf82)._**


___

> **Walmyr**: Qual a diferença entre functions  e arrow functions em JavaScript?

> **ChatGPT**: A principal diferença entre functions e arrow functions em JavaScript é a maneira como elas lidam com o escopo do "this". Em uma function tradicional, o "this" se refere ao objeto que chamou a função. Já em uma arrow function, o "this" se refere ao escopo léxico, ou seja, o objeto no qual a função foi criada. Além disso, arrow functions são mais curtas e concisas, já que não precisam ser declaradas com a palavra-chave "function".

> **Walmyr**: Fale também sobre arrow functions serem puras enquanto functions tradicionais não serem puras, no contexto de programação funcional.

> **ChatGPT**: Em programação funcional, uma função pura é aquela que retorna sempre o mesmo resultado quando recebe os mesmos parâmetros, e não tem efeitos colaterais. Em outras palavras, ela não modifica o estado externo do sistema, e não depende de nenhum estado externo para funcionar.
>
> As arrow functions são puras por natureza, pois elas não possuem acesso ao objeto "this" e, portanto, não podem modificar o estado externo. Além disso, elas também não possuem acesso ao objeto "arguments" e, portanto, são limitadas aos argumentos passados explicitamente.
>
> Já as functions tradicionais em javascript não são puras pois elas possuem acesso ao objeto "this" e "arguments" e, portanto, podem modificar o estado externo e depender de estado externo para funcionar. Além disso, elas também podem acessar variáveis globais e modifica-las.
>
> Em resumo, as arrow functions são mais fáceis de serem trabalhadas com programação funcional pois são puras e previsíveis enquanto as functions tradicionais não são.

> **Walmyr**: Fale sobre diferentes formas de passar argumentos (com e sem parênteses) para arrow functions e retorno implícito.

> **ChatGPT**: Em JavaScript, existem diferentes formas de passar argumentos para arrow functions.
>
> 1- Com argumento(s): Se uma arrow function tem um único argumento, os parênteses podem ser omitidos. Caso contrário, eles devem ser incluídos.
>
> Exemplo:

```js
// com um único argumento
const double = x => x * 2;

// com vários argumentos
const add = (x, y) => x + y;

```

> 2- Sem argumentos: Se uma arrow function não possui argumentos, os parênteses são obrigatórios.
>
> Exemplo:

```js
const sayHello = () => console.log('Hello');

```

> Retorno implícito: Se uma arrow function possui apenas uma linha de código, o retorno pode ser implícito. Isso significa que não é necessário incluir a palavra-chave "return" na frente do resultado.
>
> Exemplo:

```js
const double = x => x * 2;

```

> **Walmyr**: Fale também da omissão das chaves no retorno implícito.

> **ChatGPT**: Quando o retorno implícito é usado em uma arrow function, é possível omitir as chaves que normalmente são usadas para indicar o corpo da função. Isso significa que, se a função tem apenas uma linha de código e esse código é um retorno, é possível escrever a função sem as chaves.
>
> Exemplo:

```js
// Com retorno implícito e sem chaves
const double = x => x * 2;

```

> Esse recurso é útil para deixar o código mais conciso e fácil de ler, especialmente em casos em que a função é curta e faz apenas uma tarefa simples. No entanto, é importante notar que, quando a função tem mais de uma linha de código, ou quando o retorno é uma expressão complexa, é recomendado usar chaves e "return" para garantir que a função esteja fazendo o que se espera e para melhorar a legibilidade do código.

> **Walmyr**: Pode dar um exemplo do uso de chaves e a palavra return.

> **ChatGPT**: Claro, aqui está um exemplo de uma arrow function que usa chaves e a palavra "return" para retornar o resultado da função:

```js
const add = (x, y) => {
  return x + y;
}

```

> Neste exemplo, a função "add" tem duas variáveis de entrada, x e y, que são adicionadas juntas e retornadas com o uso da palavra-chave "return".
