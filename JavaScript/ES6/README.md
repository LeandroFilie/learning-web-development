# JavaScript ES6

### [Debugging](15-console.md)

### [Functions e Arrow Functions](01-functions.md)
- O contexto do this é a principal diferença
  - Uma function tem seu próprio this, enquanto a arrow function tem o this do escopo em que foi criada

### Operators
  - [Destructuring](02-destructuring.md)
  - [Rest e Spread](03-rest-spread.md)
  - [Binário](10-binario.md)

### JavaScript Assíncrono
Por padrão, o JavaScript é síncrono, ou seja, tarefas que executam após a tarefa anterior terminar<br />
Assíncrono: tarefas serem executadas de maneira independente de uma da outra

- [Promises](05-promises.md)

- [Async/Await](12-Async-Await.md)
- Promises (.then e .catch) vs Async/Await
  - Quando usamos o .then, o código não fica travado
  - No async/await o código só continua se a linha que tiver await terminar de ser executada

#### Consumir APIs
- [Fetch](14-fetch.md)
- [Axios](axios.md)

#### [Callbacks](11-callback.md)

### [Helpers](08-helpers.md)

### [High Order Functions](09-hof.md)

### [ES Modules](07-Modules)
Por padrão, o node não aceita, apenas com Babel (transpilador de código)
- Para corrigir, temos duas Opções
#### [Mudança de extensão do arquivo](07-Modules/Tipo1)
- Mudar a extensão dos arquivos .js para .mjs
- E também, no momento do import, passar também a extensão do arquivo

#### [Criando arquivo package.json](07-Modules/Tipo2)
- Criar a tag type e setala como module
```JSON
{
  "type": "module"
}
```