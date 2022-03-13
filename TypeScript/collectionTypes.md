### Collection types

## Arrays

No TypeScript existem duas formas de declaramos arrays, sendo declarando tipo seguido por colchetes [] 

```ts
let array: number[] = [1,2,3,4,5];
```

Ou declarando o tipo como array generico com a sintaxe: `Array<tipo>`

```ts
let array: Array<number> = [1,2,3,4,5];
```

Ambas sintaxes são validas e não tem diferença alguma entre si, podendo se usar aqui achar melhor.

## Tuple

**Tupla** é um tipo de dado parecido com um array, em que podemos ter tipos diferentes de dados em cada indice. Por exemplo criaremos uma variavel `cachorro` em que recebera 2 string e 1 numero, representando seu nome, raça e idade:

```ts
let cachorro: [string, string, number];     //Declaramos a variavel
cachorro = ["Tobias", "Vira-lata", 12];     //Inicializamos a variavel
```

Para acessarmos um valor da variavel usamos a mesma sintaxe de um **array** por exemplo:

```ts
console.log(cachorro[0]);             //Retornara a string "Tobias"
cachorro[0] = 1  //TS avisara que não é possivel atribuir um numero a uma string
cachorro[1] = "Labrador"              //Ok, altera a string "Vira-lata" 
```
