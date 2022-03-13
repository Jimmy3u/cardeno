# Interfaces

No TypeScript interfaces são usadas para descrever um objeto, nomeando e definindo seus tipos para assegurar seus parametros. Por exemplo faremos uma interface para definir algumas propriedades e um metodo de um objeto chamado `Funcionario`

```ts
interface Funcionario{
    nome: string;
    sobreNome: string;
    nomeCompleto(): string;
}
```

Veja que apenas definimos as propriedades e seus tipos, não inicializamos a função nem atribuimos nenhum valor, pois a questão da interface é exatamente isso. Definir o que o codigo requer enquanto a variavel, função ou objeto que usara ela definira a implementação e seus dados.

---

A defininição de interface é muito util para podermos ter o Type Checking e o intelisense do TypeScript a nossa disposição e nos avisar de possiveis erros.

---

No exemplo usaremos a interface declarando uma variavel e usando `Funcionario` como tipo

```ts
let funcionario: Funcionario{
    nome : "Clovis"
    sobreNome : "Silva"
    nomeCompleto(): string {
        return this.nome + " " + this.sobreNome;
    }
}

funcionario.nome = 1232      //Retornara erro pois nome e do tipo string
```

Podemos ver como apenas prenchemos o molde que declaramos com a interface, declarando `nome`, `sobreNome `e criando o retorno da função `nomeCompleto()`
