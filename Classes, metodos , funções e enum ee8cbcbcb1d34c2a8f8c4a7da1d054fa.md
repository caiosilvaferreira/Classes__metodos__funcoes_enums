# Classes, metodos , funções e enum

**Classe**
• É um tipo estruturado que pode conter (membros):
• Atributos (dados / campos)
• Métodos (funções / operações)
• A classe também pode prover muitos outros recursos, tais como:
• Construtores
• Sobrecarga
• Encapsulamento
• Herança
• Polimorfismo

 **Exemplos:**
• **Entidades**: Produto, Cliente, Triangulo
• **Serviços**: ProdutoService, ClienteService, EmailService, StorageService
• **Controladores**: ProdutoController, ClienteController
• **Utilitários**: Calculadora, Compactador
• **Outros** (views, repositórios, gerenciadores, etc.)

![Untitled](Classes,%20metodos%20,%20func%CC%A7o%CC%83es%20e%20enum%20ee8cbcbcb1d34c2a8f8c4a7da1d054fa/Untitled.png)

![Untitled](Classes,%20metodos%20,%20func%CC%A7o%CC%83es%20e%20enum%20ee8cbcbcb1d34c2a8f8c4a7da1d054fa/Untitled%201.png)

# Object

![Untitled](Classes,%20metodos%20,%20func%CC%A7o%CC%83es%20e%20enum%20ee8cbcbcb1d34c2a8f8c4a7da1d054fa/Untitled%202.png)

# Métodos e funções C#

```csharp
using System;

class HelloWorld {
    static void Main(String[] args) {

        MeuMetodo();     // declarou meu metodo.
        
        string nome = retornaNome("caio","silva");   /* criou uma variavel string e 
vinculou no metodo (retornaNome), e deu valor de duas strings para o metodo sendo nome
 caio e sobrenome silva.*/

        Console.WriteLine(nome);        /* essa impressao de dados so vai funcionar 
dentro do main, pois o nome esta sendo declaro aqui e dentro e com valores aqui tbm.*/
    }

    static void MeuMetodo() {
        Console.WriteLine("C# e legal");  /* ele imprime a frase, mas ela poderia esta
 dentro do metodo main tbm.*/
    }
    static String retornaNome(String nome, String sobrenome, int idade=27) {
        
        return nome + " "+sobrenome+" tem "+idade.ToString()+ " anos"; 
/* aqui ele concatena todos os valores e dentro do main todos esses valores 
esta incluido e tbm sendo imprimido na tela.*/
        
    }
}
```

# Structs

A anatomia de uma estrutura normalmente **[é](https://pt.wiktionary.org/wiki/%C3%A9):**

```csharp
struct Product 
{

		//Propriedades
		// Métodos

}
```

Criando uma instancia

```csharp
static void Main(string[] args)

{ //Cria uma estrutura

var product = new Product(); // aqui ele instancia para puxar as informacoes da classe.

}
```

**Anatomia de um método**

```csharp
 struct Product
{
public int Id; // ele usa a variavel Id com o metodo publico, para todos terem acesso. 
public float Price; //ele usa a variavel preco com metodo publico tambem.

public float PriceInDolar(float dolar)
{
return Price * dolar;
}
}
```

**Criar uma estrutura**

**ex:**

```csharp
var product = new Product();

product.Id = 1;
product.Title = "Mouse gamer";
product.Price = 197.23f;

Console.WriteLine(product.Id);
Console.WriteLine(product.Title);
Console.WriteLine(product.Price);
```

ex de enumeradores

```csharp
enum EEstadoCivil
{
	Solteiro = 1,
	Casado = 2,
	Divorciado = 3
}

// sem enumeradores
var cliente = new Cliente("João Silva", 1);

// com enumeradores 
var cliente = new Cliente("João Silva", EEstadoCivil.Casado);

Console.WriteLine(cliente.Nome);
Console.WriteLine(cliente.EstadoCivil); // escreve Casado
Console.WriteLine((int)cliente.EstadoCivil); // escreve 2 (com a conversao implicita)
```