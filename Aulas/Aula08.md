## Estruturas condicionais #2
Na aula passada aprendemos o Se e o Senão. Entretanto, sabemos que nem sempre uma decisão tem apenas dois caminhos diferentes.
Nos casos em que há mais de três opções é possível escrever o código da seguinte maneira:

```
Se (situação 1) entao
  Bloco A
senao
  Se (situação 2) entao
    Bloco B
  senao 
    Bloco C
  FimSe    
FimSe  
```

Entretanto há também uma segunda forma de escrever um código em que existem três ou mais condições.
Para isso, utilizamos o Caso.

```
Escolha(variável)
Caso Valor A
  Bloco A
Caso Valor B
  Bloco B  
Caso Valor C
  Bloco C
OutroCaso
  Bloco D 
FimEscolha  
```

## Exercícios práticos
**1) Aprimorando o algoritmo de viagem para a Disney**
```
Algotirmo "Prática1"

var
  dinheiro: Real

inicio
  Escreval("Quantos reais eu tenho?")
  Leia(dinheiro)
  
  Se(dinheiro >= 10000) entao
    Escreva("#Partiu Disney!")
  senao  
    Se(dinheiro >= 5000) e (dinheiro < 10000) entao
      Escreva("Visitar família")
    senao
      Escreva("Vou ficar em casa")
    FimSe
  FimSe
  
fimalgoritmo
```

**2) Aluna aprovada, reprovada ou em recuperação**
```
Algotirmo "Prática2"

var
 n1, n2, media: Real

inicio
  Escreval("Digite a primeira nota da estudante:")
  Leia(n1)
  Escreval("Digite a segunda nota da estudante:")
  Leia(n2)

  media <- (n1 + n2) / 2

 Escreval("----------------")
 Escreval("MEDIA:", media:4:2)

 Se(media >= 7) entao
  Escreval("ALUNA APROVADA")
 senao
  Se(media >= 5) e (media < 7) entao
    Escreval("ALUNA EM RECUPERAÇÃO")
  senao
    Escreval("ALUNA REPROVADA")
  FimSe
 FimSe

 Escreva("----------------")
fimalgoritmo
```

**3) Utilizando o Caso para um programa de doação**
Neste programa aparecerá opções de doações para o usuário selecionar.

```
Algoritmo("Prática3")

var
  num_selecionado: Inteiro
  Valor_doacao: Real

inicio
  Escreval("----------------")
  Escreval("CRIANÇA ESPERANÇA")
  Escreval("----------------")
  Escreval("Muito obrigada por ajudar!")
  Escreval("Digite 1 para doar R$10 ")
  Escreval("Digite 2 para doar R$25 ")
  Escreval("Digite 3 para doar R$50 ")
  Escreval("Digite 4 para doar outros valores ")
  Escreval("Digite 5 para cancelar ")

  Leia(num_selecionado)
  Escolha(num_selecionado)

  Caso 1
    Valor_doacao <- 10
  Caso 2
    Valor_doacao <- 25
  Caso 3
    Valor_doacao <- 50
  Caso 4
    Escreva("Qual o valor da doação? ")
    Leia(Valor_doacao)
  Caso 5
    Valor_doacao <- 0
  FimEscolha

  Escreval("----------------")
  Escreval("O valor de sua doação foi", Valor_doacao)
  Escreval("Obrigada!")
  Escreval("----------------")

fimalgoritmo
```

**4) Utilizando o Caso para calcular salário**
Este programa irá calcular o novo salário do funcionário baseado na quantidade de dependêntes.
Quanto mais dependentes, maior o novo salário.


```
Algoritmo("Prática4")

var
nome: Caractere
salario, Novo_salario: Real
dependentes: Inteiro

inicio
 Escreval("Qual o nome do funcionário? ")
  Leia(nome)
  Escreval("Qual o valor do salário? R$")
  Leia(salario)
  Escreval("Qual a quantidade de dependentes? ")
  Leia(dependentes)

  Escolha(dependentes)
    Caso 0
      Novo_salario <- salario + (salario*5/100)
    Caso 1, 2, 3
      Novo_salario <- salario + (salario*10/100)
    Caso 4, 5, 6
      Novo_salario <- salario + (salario*15/100)
    OutroCaso
      Novo_salario <- salario + (salario*18/100)
    FimEscolha

   Escreval("O novo salário de ", nome, " é igual a R$", Novo_salario:5:2)
fimalgoritmo
```

**5) Aproveitamento de uma aluna**
```
Algoritmo("Prática5")

var
  nota1, nota2, media: Real
  aproveitamento: Caractere

inicio
   Escreval("----------------")
  Escreval("Digite a primeira nota da aluna ")
  Leia(nota1)
  Escreval("Digite a segunda nota da aluna ")
  Leia(nota2)
  Escreval("----------------")

  media <- (nota1 + nota2) / 2

  Se(media >= 9) e (media <= 10) entao
     aproveitamento <- "A"
  senao
    Se(media >= 8)e (media <= 8.9) entao
     aproveitamento <- "B"
    senao
     Se(media >= 7) e (media <= 7.9) entao
      aproveitamento <- "C"
     senao
       Se(media >= 6) e (media <= 6.9) entao
        aproveitamento <- "D"
       senao
        Se(media >= 5) e (media <= 5.9) entao
         aproveitamento <- "E"
        senao
         Se(media >= 0) e (media < 5) entao
          aproveitamento <- "F"
         FimSe
        FimSe
       FimSe
      FimSe
     FimSe
    FimSe

  Escreval("Média: ", media)
  Escreval("Aproveitamento: ", aproveitamento)
  Escreval("----------------")

fimalgoritmo
```

**6) Uma partida de futebol**
```
Algoritmo("Prática6")

var
  bangu, madu: inteiro
  diferenca: Real
 
inicio
  Escreval("----------------")
  Escreval("Quantos gols do BANGU?")
  Leia(bangu)
  Escreval("Quantos gols do MADUREIRA?")
  Leia(madu)

  diferenca <- bangu - madu

  //utilizando se

  Se(diferenca = 0) entao
   Escreval("----------------")
   Escreval("DIFERENÇA: ", diferenca)
   Escreval("STATUS: EMPATE")
   Escreval("----------------")
  senao
    Se(diferenca > 0) e (diferenca < 5) entao
       Escreval("----------------")
       Escreval("DIFERENÇA: ",ABS(diferenca))
       Escreval("STATUS: Partida normal")
       Escreval("----------------")
    senao
       Escreval("----------------")
       Escreval("DIFERENÇA: ", diferenca)
       Escreval("STATUS: GOLEADA")
       Escreval("----------------")
    FimSe
  FimSe

//utilizando o Caso

Escolha(diferenca)
Caso 0
    Escreval("----------------")
    Escreval("DIFERENÇA: ", diferenca)
    Escreval("STATUS: EMPATE")
    Escreval("----------------")

Caso 1, 2, 3, 4
    Escreval("----------------")
    Escreval("DIFERENÇA: ", diferenca)
    Escreval("STATUS: Partida normal")
    Escreval("----------------")

OutroCaso
    Escreval("----------------")
    Escreval("DIFERENÇA: ", diferenca)
    Escreval("STATUS: GOLEADA")
    Escreval("----------------")
 FimEscolha

fimalgoritmo
```
