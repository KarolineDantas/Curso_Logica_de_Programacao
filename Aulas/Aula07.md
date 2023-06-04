## Estruturas condicionais
Se eu tiver dinheiro vou fazer uma viagem para Disney. Ou seja, se minha determinada condição for atendida, algo irá acontecer.

No VisuAlg, a estrutura fica assim:

```
Se (expressão) entao
  Bloco
FimSe  
```

## Utilizando o Senão nas estruturas condicionais
O Senão é utilizado para os casos em que a condição não é atendida. Exemplo:
```
Se (expressão) entao
  Bloco A
senao
  Bloco B
FimSe   
```

## Exercícios práticos
**1) Se eu tiver dinheiro vou fazer uma viagem para Disney**
```
Algoritmo "Pratica1"

var
 dinheiro: Real

inicio
Se (dinheiro >= 10000) entao
  Escreval("Partiu Disney!")
FimSe

fimalgoritmo
```

**2) Aprimorando o algoritmo da idade**
```
Algoritmo "Pratica2"

var
 ano_atual, ano_nasc, idade: Inteiro

inicio
Escreval("Em que ano estamos?")
Leia(ano_atual)
Escreval("Em que ano eu nasci?")
Leia(ano_nasc)

idade <- ano_atual - ano_nasc
Escreval("Em", ano_atual, " você terá", idade, " anos.")
Se(idade >= 21) entao
  Escreval("E você terá atingido a maior idade")
FimSe  

fimalgoritmo
```

**3) Aprimorando o algoritmo da viagem para Disney**
```
Algoritmo "Pratica3"

var
 dinheiro: Real

inicio
Escreval("Quantos reais eu tenho?")
Leia(dinheiro)
Se (dinheiro >= 10000) entao
  Escreval("Partiu Disney!")
senao
  Escreval("Não vou a Diney :(")
  Escreval("#chateado")
FimSe

fimalgoritmo
```

**4) Par ou impar**
```
Algoritmo "Pratica4"

var
  num: Inteiro

inicio
Escreval("Digite um número qualquer")
Leia(num)

Se(num % 2 = 0) entao
  Escreval("O número", num, " é par")
senao
  Escreval("O número", num, " é ímpar")
FimSe  
  fimalgoritmo
```

**5) Cálculo do imc**

```
Algoritmo "Pratica5"

var
 peso, altura, IMC: real

inicio
Escreval("Digite seu peso")
Leia(peso)
Escreval("Digite sua altura")
Leia(altura)

imc <- peso/ (altura^2)

Se (IMC < 17) entao
   Escreval ("Seu IMC é ", IMC:5:2, ". Você está muito abaixo do peso! ideal")
   FimSe
Se (IMC > 17) e (IMC <= 18.5) entao
   Escreval ("Seu IMC é ", IMC:5:2, ". Você está abaixo do peso ideal.")
   Fimse
Se (IMC > 18.5) e (IMC <= 25) entao
   Escreval ("Seu IMC é ", IMC:5:2, ". Seu peso está ótimo!")
   Fimse
Se (IMC > 25) e (IMC <= 30) entao
   Escreval ("Seu IMC é ", IMC:5:2, ". Você está com sobrepeso!")
   Fimse
Se (IMC > 30) e (IMC <= 35) entao
   Escreval ("Seu IMC é ", IMC:5:2, ". Você está obeso!")
   Fimse
Se (IMC > 35) e (IMC <= 40) entao
   Escreval ("Seu IMC é ", IMC:5:2, ". Você está com obesidade severa!")
   Fimse
Se (IMC > 40) entao
   Escreval ("Obesidade mórbida")
   Fimse

fimalgoritmo
```

**6) Está apto para dirigir?**
```
Algoritmo "Pratica6"

var
ano_atual, ano_nasc, idade: Inteiro

inicio
Escreval("--------------------------")
Escreval("DEPARTAMENTO DE TRANSITO")
Escreval("--------------------------")
Escreval("Ano atual (yyyy):")
Leia(ano_atual)
Escreval("Ano de nascimento (yyyy):")
Leia(ano_nasc)

idade <- ano_atual - ano_nasc


Escreval("--------STATUS---------")
Escreval("IDADE:", idade)

se(idade >= 18) entao
  Escreval("APTO A TIRAR A CARTEIRA")
senao 
  Escreval("NÃO APTO A TIRAR A CARTEIRA")
FimSe
Escreval("--------------------------")

fimalgoritmo
```
