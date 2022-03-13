## Union Type

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
        console.log('Foi inserido  uma string.')
    else if(typeof(input) === "number")
        console.log('Foi inserido um numero.')
}

qualTipo(123);         //Imprime 'Foi inserido um numero.'
qualTipo("Clovis");    //Imprime 'Foi enserida uma string.'
qualTipo(false);       //Dispara um erro, dizendo que boolean não é valido para o dado
```

## Intersection Type

Muito parecido com o Union, o tipo Intersection é utilizado para criação de novos tipos geralmente combinando uma ou mais **Interface** para criar um novo tipo com todas as suas propriedades por exemplo:

```ts
interface Pessoa {
    nome: string;
    idade: number;
    cpf: string;
}
interface Aluno {
    matricula: number;
}
interface Funcionario {
    salario: number;
}

type pessoaAluno = Pessoa & Aluno;
type pessoaFuncionario = Pessoa & funcionario

let novoAluno: pessoaAluno {
    nome: "Claudisnei Silva";
    idade: 12;
    cpf: "231.123.654-23";
    matricula: 20220225;
}

let novoFuncionario: pessoaFuncionario {
    nome: "Sheila Silva";
    idade: 32;
    cpf: "131.123.654-69";
    salario: 6000.25;
}
```

Sempre que criarmos um Intersection Type, usamos a sintade de `Tipo1 & Tipo 2` usando o 'E comercial' `&` 
