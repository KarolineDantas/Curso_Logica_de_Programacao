## Estruturas de repetição
Enquanto uma expressão for verdadeira, o código continuará repetindo.

```
Enquanto expressão faca
  Bloco
FimEnquanto
```

## Exercícios práticos
**1) Programa que conta até 10**
```
Algoritmo "Prática1"

var
  contador: inteiro
inicio
  contador <- 0
  Enquanto (contador <= 10) faca
    Escreval(contador)
    contador <- contador + 1
  FimEnquanto
  Escreval("Acabei de contar!")
    
fimalgoritmo
```

**2) Programa que conta de 10 a 0**
```
Algoritmo "Prática2"

var
  contador: inteiro
  
inicio
  contador <- 10
  Enquanto (contador >= 0) faca
    Escreval(contador)
    contador <- contador - 1
  FimEnquanto
  Escreval("Acabei de contar!")
    
fimalgoritmo
```

**3) Programa que conta de 0 até o número que o usuário quiser**
```
Algoritmo "Prática3"

var
  contador, num: inteiro
  
inicio

  Escreva("Até quantos quer contar? ")
  Leia(num)
  contador <- 0
  
  Enquanto (contador <= num) faca
    Escreval(contador)
    contador <- contador + 1
  FimEnquanto
  Escreval("Acabei de contar!")
    
fimalgoritmo
```

**4) Programa que conta de 0 até onde o usuário quiser, com salto**
```
Algoritmo "Prática4"

var
  contador, num, salto: inteiro
  
inicio

  Escreval("Até quantos quer contar? ")
  Leia(num)
  Escreval("Quer pular de quantos em quantos? ")
  Leia(salto)
  
  contador <- 0
  
  Enquanto (contador <= num) faca
    Escreval(contador)
    contador <- contador + salto
  FimEnquanto
  Escreval("Acabei de contar!")
    
fimalgoritmo
```

**5) Programa que lê e soma 5 números**
```
Algoritmo "Prática5"

var
  contador, soma, num: Inteiro
inicio
  
  contador <- 1
  soma <- 0
  
  Enquanto (contador <= 5) faca
    Escreval("Digite o ", contador, ". número")
    Leia(num)
    soma <- soma + num
    contador <- contador + 1
  FimEnquanto
  
  Escreval("Acabei de contar! A soma de todos os valores é igual a", soma)

fimalgoritmo
```

**5.1) Programa que lê e soma 5 números, além de dizer qual foi o maior valor digitado pelo usuário**
```
Algoritmo "Prática5.1"

//Adicional: mostrar qual foi o maior valor digitado pelo usuário
//Criar uma variável chamada maior. Ela irá guardar o maior número

var
  contador, soma, num: Inteiro
  maior: Inteiro
  
inicio
  
  contador <- 1
  soma <- 0
  
  Enquanto (contador <= 5) faca
    Escreval("Digite o ", contador, ". número")
    Leia(num)
    
    //irá guardar os valores em "maior", e comparar se o próximo a ser digitado é superior ao valor que já está guardado
    Se(num > maior) entao
      maior <- num
    FimSe
    
    soma <- soma + num
    contador <- contador + 1
  FimEnquanto
  
  Escreval("Acabei de contar! A soma de todos os valores é igual a", soma)
  Escreval("O maior valor digitado foi", maior)
fimalgoritmo
```

**5.2) Programa que lê e soma 5 números, além de dizer qual o maior e menor valor digitado pelo usuário**
```
Algoritmo "Prática5.2"

var
  contador, soma, num, maior, menor: Inteiro
  
inicio
  
  contador <- 1
  soma <- 0
  maior <- 0

  Enquanto (contador <= 5) faca
    Escreval("Digite o ", contador, ". número")
    Leia(num)

    //irá guardar os valores em "maior", e comparar se o próximo a ser digitado é superior ao valor que já está guardado
    Se(num > maior) entao
     maior <- num
     FimSe
     
    Se(menor = 0) entao
       menor <- num
     senao
       Se(num < menor) entao
        menor <- num
     FimSe
     FimSe

    soma <- soma + num
    contador <- contador + 1
  FimEnquanto

  Escreval("Acabei de contar! A soma de todos os valores é igual a", soma)
  Escreval("O maior valor digitado foi", maior, ", e o menor valor digitado foi", menor)
  fimalgoritmo
```

**6) Conversão em dólar**
O objetivo é converter o valor informado pelo o usuário 4 vezes.

```
Algoritmo "Prática6"

var
 contador: Inteiro
 reais, dolar: Real
 
inicio

  contador <- 0

  Enquanto(contador <= 4) faca
    Escreval("Qual o valor em R$?")
    Leia(reais)
    dolar <- reais*2.22
    Escreval("O dólar custa atualmente 2.22, portanto, R$", reais:5:2, " é igual a", dolar:5:2, " dólares.")
    contador <- contador + 1
  FimEnquanto
  
fimalgoritmo
```

**6.1) Repetir a conversão em dólar quantas vezes o usuário quiser**

```
Algoritmo "Prática6.1"

var
 contador, repeticao: Inteiro
 reais, dolar: Real
inicio
  
  Escreval("Quantas conversões deseja realizar?")
  Leia(repeticao)
  
  contador <- 0

  Enquanto(contador <= repeticao) faca
    Escreval("Qual o valor em R$?")
    Leia(reais)
    dolar <- reais*2.22
    Escreval("O dólar custa atualmente 2.22, portanto, R$", reais:5:2, " é igual a", dolar:5:2, " dólares.")
    contador <- contador + 1
  FimEnquanto

fimalgoritmo
```

**7) Contagem inteligente**
```
Algoritmo "Contagem inteligente"

var
  inicio, fim, contador: Inteiro
  
inicio
  Escreval("CONTAGEM INTELIGENTE")
  Escreval("--------------------")
  Escreval("Início: ")
  Leia(inicio)
  Escreval("Fim")
  Leia(fim)
  Escreval("--------------------")
  Escreval("C O N T A N D O")
  Escreval("--------------------")
  
  contador <- 0

  Se(inicio < fim) entao
      Enquanto(contador <= fim) faca
        Escreva(contador,"...") 
        contador <- contador + 1
      FimEnquanto  
    senao 
      contador <- inicio
      Enquanto(contador >= 0) faca
        Escreva(contador,"...") 
        contador <- contador - 1
      FimEnquanto
  FimSe
fimalgoritmo
```

**7) Melhor aluna da turma**
```
Algoritmo "Prática 7"

var
  num_alunas, contador: Inteiro
  nota, melhor_nota: Real
  nome, melhor_aluna: Caractere
  
inicio
  Escreval("--------------------")
  Escreval("Escola Santa Paciência")
  Escreval("--------------------")
  Escreval("Quantos alunos a turma tem?")
  Leia(num_alunas)
  
  contador <- 0
  
  Enquanto (contador <= num_alunas) faca 
    Escreval("-----------------")
    Escreval("ALUNA", contador)
    Escreval("Nome do Aluna:")
    Leia(nome)
    Escreval("Nota de ", nome)
    Leia(nota)
  FimEnquanto  
  
  Se(nota > maior_nota) entao
    melhor_aluna <- aluna
    maior_nota <- nota
  FimSe
  
  Escreval("O melhor aproveitamento foi de", melhor_aluna, " com a nota", maior_nota)

fimalgoritmo
```
