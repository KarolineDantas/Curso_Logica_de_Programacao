## Exercícios práticos

**1) Creuza vai fazer aniversário, mas esqueceu quantos anos vai fazer**
```
Algoritmo "Creuza01"

var
  ano_atual, ano_nasc, idade: inteiro
  
inicio
  Escreval("Em qual ano estamos?")
  Leia(ano_atual)
  Escreval("Em qual ano eu nasci")
  Leia(ano_nasc)
  
  idade <- ano_atual - ano_nasc
  Escreval("Tenho então", idade, " anos de idade.")
  
fimalgoritmo
```

**2) Em comemoração ao seu aniversário, Creuza vai viajar para outro país e precisa comprar dólares**

Para esse exercício vamos considerar que um dólar vale 2,22 reais.
```
Algoritmo "Creuza02"

var
 reais, dollar: Real
 
inicio
  Escreval("Quantos reais tenho?")
  Leia(reais)
  
  dollar <- reais * 2.22
  
  Escreva("Creuza tem ", dollar, " dolares.")
  
fimalgoritmo
```


**3) Creuza viajou e chegou no outro país. Ela viu a previsão do tempo e não entendeu porque mostravam a temperatura em F ao invés de C**

A conversão de F para C é igual a: C = (F-32)/1,8

```
Algoritmo "Creuza03"

var
F, C: Real
 
inicio
  Escreval("Qual a temperatura atual (em fahrenheit)?")
  Leia(F)
  
  C <- (F - 32) / 1.8
  
  Escreval("No Brasil estaria", C, " graus.")
  
fimalgoritmo
```

**4) Creuza voltou de viagem e comprou muitas coisas. Porém, precisa pagar um imposto em seus produtos**
Vamos considerar que a taxa do imposto é igual a 60% do valor do produto.

```
Algoritmo "Creuza04"

var
preco, imposto: Real
 
inicio
  Escreval("Qual o valor do produto?")
  Leia(preco) 
  imposto <- (preco*60)/100
  
  Escreval("O imposto será de R$", imposto, ".")
  
fimalgoritmo
```

**5) Creuza não tem dinheiro para pagar os impostos, então teve que pegar um empréstimo no banco**
Vamos considerar que a taxa de juros é igual a 20%. É possível também parcelar o empréstimo.

```
Algoritmo "Creuza05"

var
preco, imposto: Real
 
inicio
  Escreval("Quanto quero pegar de empréstimo?")
  Leia(emprestimo)
  Escreval("Em quantas vezes quero parcelar?")
  juros <- (emprestimo*20)/100
  emprestimo_final <- emprestimo + juros
  
  Escreval("O imposto será de R$", imposto, ".")
  
fimalgoritmo
```
