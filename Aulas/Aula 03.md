# Utilizando atribuições
```Algoritmo "MeuNome"
var 
  nome: caractere
inicio
  Escreval("Digite seu nome: ")
  Leia(nome)
  Escreval("Muito prazer, " + nome)

FimAlgoritmo
```
**Execução no VisuAlg:**
![Captura de tela 2023-05-31 140046](https://github.com/KarolineDantas/Curso_Logica_de_Programacao/assets/107884724/5aff5268-a72c-4fad-9e07-13cd8ae56aa1)

## Operadores Aritméticos

1) Adição (+)
2) Subtração (-)
3) Multiplicação (*)
4) Divisão (/)
5) Divisão inteira (\)
6) Exponenciação (^)
7) Módulo (%)


## Ordem de precendência

1) Parênteses ()
2) Exponenciação ^
3) Multiplicação e divisão * /
4) Adição e subtração + -

## Funções aritméticas
1) Abs (Valor absoluto)
2) Exp (Exponenciação)
3) Int (Valor inteiro)
4) RaizQ (Raiz quadrada)
5) Pi (Reporta pi)
6) Sen (Seno (rad)) 
7) Cosseno (Cosseno (rad))
8) Tan (Tangente (rad))
9) GraupRad (Graus para Rad)  

### Para praticar
**1) Solicitar dois números para o usuaário e mostrar a soma entre eles**

``` 
Algoritmo "Pratica1"

var 
  n1, n2, soma: inteiro
inicio
  Escreval("Digite o primeiro número: ")
  Leia(n1)
  Escreval("Digite o segundo número: ")
  Leia(n2)
  
  soma <- n1 + n2
  
  Escreval("A soma de", n1, " mais", n2, " é igual a", soma)
  ```
  
**2) Calcular a média de dois valores**  

``` 
Algoritmo "Pratica2"

var 
 n1, n2: inteiro
 media: Real
 
inicio
  Escreval("Digite o primeiro número: ")
  Leia(n1)
  Escreval("Digite o segundo número: ")
  Leia(n2)
  
  media <- (n1 + n2) / 2
  
 Escreval("A media entre", n1, " e", n2, " é igual a", media)
  ```
  
**3) Converter Graus para Rad**  

``` 
Algoritmo "Pratica3"

var 
  A: Real
 
inicio
  A <- GraupRad(90)
  Escreval(A)
  ```
