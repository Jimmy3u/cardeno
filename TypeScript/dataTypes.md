# Tipos de dados

### Tipos Primitivos

São os tipos mais basicos de dados sendo eles:

- **String** representa linhas de texto, palavras e etc 
  
  ```ts
  let bomDia: string = "Bom dia grupo do zapzap";
  ```

- **Number**  usado para todos os tipos de numeros, seja inteiros ou de ponto flutuante.
  
  ```ts
  let nice: number = 69;
  let float: number = 6.9;
  ```

- **Boolean** para os valores true e false
  
  ```ts
  let verdadeiro: boolean = false;
  ```

- **Enum** usado para representar um conjunto de valores enumerados por um indice, por exemplo:
  
  ```ts
  enum StatusContratado{
       Permanente,                 // Representa o indice 0
       Temporario,                 // 1
       Estagiario                  // 2
  }
  ```

- **Any** representa qualquer tipo e permite a alteração irrestrita sem a checagem de tipo e de erros
  
  ```ts
  let randomValue: any = 10;
  randomValue = 'Mateo';     // Ok, pode ser atribuido um tipo diferente
  randomValue = true;        // Ok
  
  console.log(randomValue.name) // Retorna "undefined" no console
  console.log(randomValue)      // Retorna "True"
  randomValue();                // Retorna que "randomValue" não é uma função
  ```

- **Unknown** assim como o **Any** aceita qualquer tipo porem com limitações de acesso e chamadas a suas propriedades. Por exemplo :
  
  ```ts
  let randomValue: unknown = 10;
  randomValue = true;
  randomValue = 'Mateo';
  
  console.log(random.Value);      // Ira printar 'Mateo'
  console.log(randomValue.name);  // Error: Objeto é do tipo unknown
  randomValue();                  // Error: Object é do tipo unknown
  randomValue.toUpperCase();      // Error: Object é do tipo unknown
  ```
