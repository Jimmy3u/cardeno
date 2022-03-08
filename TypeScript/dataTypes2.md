## Union Type

---

No TypeScript podemos atribuir mais de um data type para uma função ou variavel, sendo esse o tipo **Union**. Por exemplo:

```ts
let union: string | number; 
let union: (string | number);  //Ambas sintaxes são validas
union = "Açucar"            //Valido
union = 12               //Valido
union = false;              //Vai retornar um erro
```

O tipo Union pode ser declarado tanto apenas separando os tipos com `|` ou envolvendo os tipos com parenteses. Podemos usar isso como parametros de função, por exemplo:

```ts
function qualTipo(input: string | number){
    if (typeof(input) === "string")
        console.log('Foi enserida uma string.')
    else if(typeof(input) === "number")
        console.log('Foi enserido um numero.')
}

qualTipo(123);         //Imprime 'Foi enserido um numero.'
qualTipo("Clovis");    //Imprime 'Foi enserida uma string.'
qualTipo(false);       //Dispara um erro, dizendo que boolean não é valido para o dado
```

## Tuple

---

**Tupla**  é um tipo de dado parecido com um array, em que podemos ter tipos diferentes de dados em cada indice. Por exemplo criaremos uma variavel `cachorro` em que recebera 2 string e 1 numero, representando seu nome, raça e idade:

```ts
let cachorro: [string, string, number];     //Declaramos a variavel
cachorro = ["Tobias", "Vira-lata", 12];     //Inicializamos a variavel
```
