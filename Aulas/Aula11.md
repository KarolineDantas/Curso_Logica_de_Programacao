  # Estruturas de Repetição III

  Relembrando as outras estruturas
  ```
    Enquanto não arrumar o quarto faca
      castigo
    FimEnquanto
      liberado

  Exemplo:
    c <- 1
    Enquanto (c<= 10) faca
      Escreval(c)
      c <- c + 1
    FimEnquanto
  ```
 ```
    Repita
      castigo
    Ate arrumar o quarto
    liberado

    Exemplo:
    Repita
      c <- c + 1
    Ate (c>10)
  ```

A nova estrutura de repetição é a seguinte:
```
Para variavel <- inicio ate fim [passo salto] faca
  Bloco
FimPara

Exemplo:
Para c <- 1 ate 10 passo 1 faca
  Escreval(c)
FimPara
```
Essa estrutura não é recomendada nos casos em que não sabe-se a quantidade final de repetições.

## Eercícios práticos
**1) Contar de 1 até 10**
```
Algoritmo "Pratica1"

var
 c: Inteiro

inicio
  Para c <- 1 ate 10 faca
    Escreval(c)
  FimPara

fimalgoritmo
```

**2) Números pares**
```
Algoritmo "Pratica2"

var
 c, valor: Inteiro

inicio
  Escreval("Este programa lista os números pares. Me diga até qual número deseja ver uma lista?: ")
  Leia(valor)
 
  Para c <- 0 ate valor faca passo 2
    Escreval(c)
  FimPara

fimalgoritmo
```

**3) Contagem regressiva de números pares**
```
Algoritmo "Pratica3"

var
 c, valor: Inteiro

inicio
 Se(valor%2=1) entao
    valor <- valor -1
  FimSe

  Para c <- valor ate 0 passo -2 faca
    Escreval(c)
  FimPara

fimalgoritmo
```

**4) Quantos valores estão entre 0 e 10?**
```
Algoritmo "Pratica4"

var
 c, num, zeroADez: Inteiro

inicio
Escreval("Estre programa diz quantos valores entre 0 e 10 foram digitados")

 zeroADez <- 0
 
  Para c <- 0 ate 6 faca
   Escreva("Digite um número: ")
   Leia(num)
  Se(num >= 0) e (num <= 10) entao
   zeroADez <- zeroADez + 1
  FimSe
  FimPara
  
  Escreva("Você digitou", zeroADez, " números que estão entre zero e dez.")
fimalgoritmo
```

**5) Quantos valores estão entre 0 e 10? Bônus: somando os valores ímpares digitados (somente os ímpares entre 0 e 10)**
```
Algoritmo "Pratica5"

var
 c, num, zeroADez, impar: Inteiro

inicio
 zeroADez <- 0
 impar <- 0
 
  Para c <- 0 ate 6 faca
   Escreva("Digite um número: ")
   Leia(num)

  //totalizando quantos números entre 0 a 10 existem
  Se(num >= 0) e (num <= 10) entao
   zeroADez <- zeroADez + 1
   
   //somando os valores ímpares
    Se(num%2=1) entao
     impar <- impar + num
    FimSe
  FimSe
  FimPara
  
  Escreval("Você digitou", zeroADez, " números que estão entre zero e dez.")
  Escreva("A soma dos números ímpares foi: ", impar)
fimalgoritmo
```

**6) Combinações**

```
algoritmo "Pratica6"

var
 c1, c2: Inteiro
inicio

   Para c1 <- 1 ate 3 faca
    Para c2 <- 1 ate 3 faca
      Escreval(c1, c2)
    FimPara
   FimPara

fimalgoritmo
```
