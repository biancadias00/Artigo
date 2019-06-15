Acadêmicas do 3º período de LCC - IFTO - *Campus* Dianópolis.
Bianca Rodrigues Dias e Larissa Rodrigues Pereira.
# Ponteiros em linguagem C
A ultilização de ponteiros em C é uma das caracteristicas que faz com que a liguagem se torne mais flexivel. Os ponteiros são variaveis de armazenamento, ondem armazenam endereço de memoria de outra variaveis. Eles podem indica qualquer variavel, sendo ela int, float, double, reg, entre outras.

####Alguns exemplos de declarações de ponteiros:

- Para utilizar a variavel ponteiro deve-se utilizar o símbolo "*"  entre o tipo e o nome da variável. A forma geral da declaração é:
```c
Tipo_da_variável * Nome_da_Variável;
```
-- Declaração de ponteiro *p* inteiro:
```c
int *p;
```
-- Declaração de ponteiro *p* para um registro reg:
```c
struct reg *p;
```
-- Declaração de um ponteiro *r* para um ponteiro que apontará um inteiro:
```c
int **r;
```

#### Operadores de ponteiros

O ponteiros trabalha com dois operadores, são eles:
O operador de indireção "*";
O operador unário (constante) "&" para obter o endereço de uma variável (representa um endereço de memória fixo).
```c
int varX = 10;
int * pt_varX;
 
pt_varX = &varX; 		//atribui o endereço de varX para o ponteiro pt_varX 
```
####Aplicando ponteiro em um programa:
Na linguagem C, é possivel imprimir o endereço armazenado em um ponteiro, utilizando a função *printf* com o formatador *%p* .
####Ex:
```c
#include <stdio.h>
void main()
{
  int x;			 //x é a variável que será apontada pelo ponteiro
  int *ptr;			//declaração de variável ponteiro
  ptr = &x;		//atribuindo o endereço da variável x ao ponteiro
  printf("O endereço de X é: %p\n", ptr);
}
```

####Explicação:

O operador "*" foi utilizado para indicar que a variável ptr é um ponteiro. Já que o objetivo é armazenar o endereço da variável  X por ser uma variável do tipo int, o ponteiro também deve ser do tipo int. Ou seja, ele vai apontar para uma variável do tipo inteiro.

O operador "&" foi utlizado para atribuir o endereço da variável X ao ponteiro ptr, porque vamos referir ao endereço da variável X e não ao conteúdo da mesma.

A expressão %p, foi utilizada para exibir o endereço e o conteúdo do ponteiro ptr.

#Referência em Java

Quando associamos um obejot a uma variavel, na verdade a varrievel vai acessa o objeto, ou seja, fara a chamda da referência.

É por esse motivo que, diferente dos tipos primitivos como int e long , precisamos dar new
depois de declarada a variável:
```java
public static void main(String[] args) {
Conta c1;
c1 = new Conta();
Conta c2;
c2 = new Conta();
}
```
Nesse caso a  c1 se refere a um objeto, pois c1 é uma variável referência.

Basta lembrar que, em Java, uma variável nunca é um objeto. Não há, no Java, uma maneira de criarmos o que é conhecido como "objeto pilha" ou "objeto local", pois todo objeto em Java, sem exceção, é acessado por uma variável referência.
Esse código nos deixa na seguinte situação:
```java
Conta c1;
c1 = new Conta();
Conta c2;
c2 = new Conta();
```
Nesse exemplo a c1 e c2 vão guardar um número indica em que posição da memória aquela Conta está. Dessa forma, quando usamos "." para navegar, o Java vai acessar a Conta que se encontra naquela posição de memória, e não uma outra.

Perceba que é parecido com o ponteiro, porém você não pode manipur como número e nem utilizar em aritmética, ela é tipada.

# Parâmetros em Java
Parametros são valores passados para um método.

Será recebido atraves de parâmentros quanod um method rreceber dados.

#####Ex:
```java
[dados_do_método] tipo_de_retorno nome_do_método (tipo nome_do_parametro1, tipo nome_do_parametro2){
    //código do method
}
```
Quando se declara um parâmetro para um método ou um construtor, é preciso dar um name para esse parâmetro. Esse nome é usado dentro do corpo do método para se referir ao argumento anteiror.

O nome de um parâmetro deve ser unico em seu escopo. Não pode igual ao nome de outro parâmetro para o mesmo método ou construtor e também não pode ser o nome de uma variável local dentro do método ou construtor. porém um parâmetro pode ter o mesmo nome de um dos campos da classe. Se este for o caso, o parâmetro é dito para sombrear o campo. 
Por exemplo, considere a seguinte Circleclasse e seu setOriginmétodo:
```java
Círculo de Classe Pública {
    privado int x, y, raio;
    public void setOrigin (int x, int y) {
        ...
    }
}
```

#Retorno em java

As funções permitem retornar valores de um processo que já foi executado dentro delas e esse valor pode ser guardado dentro de uma variável. Dessa forma o programa torna mais simples.

Para criar uma função que retorna valores é preciso ficar atento ao retorno. Como as demais funções não retornavam valores, seu retorno era vazio - void. Agora, temos que declarar que tipo de retorno virá da função.

O retorno é acontece no comando *return*, que finaliza a função e da o retorno. A variável ou valor que utilizarmos para return será o tipo de retorno da função.

Em uma suposição de três funções, a primeira retornar um inteiro, a segunda um double e a terceira uma string. Então fica da sefuinte forma:
```java
public static int funcaoDeInteiro (){} public static double funcaoDeDouble (){} public static String funcaoDeString (){}
```

No exemplo a seguir, serácriado uma função que retornar um valor de verdadeiro ou falso. Usando o retorno, vamos determinar o que será feito dentro de uma estrutura seletiva (if).
```java
public static boolean ehPrimo(long nr) {
if (nr < 2)
return false;
for (long i = 2; i <= (nr / 2); i++) {
if (nr % i == 0)
return false;
}
return true;
}
public class Primo { http://www.tiexpert.net/programacao/java/funcoes.php

public static void main(String[] args) {
long x = 5;
if (ehPrimo(x)) 		// se for primo
System.out.println(x + " é primo");
else 		// se não for primo
System.out.println(x + " não é primo");
}
w.tiexpert.netPág. 3 de 3 }
```
O que a função faz é verificar se um número é primo ou não.

#Recursividade em java

A recursividade é semelhante a um laço de repetição, na verdade o que é possível fazemos em laço também pode ser feito em recursividade. A recursividade é  uma função dentro da outra.

Ela tabalha da segunte forma: Vai calcular ou seguir as instruções descendo até a base, dessa forma os resultdos são emplihado a parit da bate até o topo.

Agora vamo demonstra na pratica um exmplo de Recursividade.

#####Ex:
```java
public class Fatorial{
//Método recursivo para cálculo de fatorial
	public int fatorialRecursivo (int num){
		//se não é igual a 0, retona 1
		if (num == 0)
		return 1;
		//Caso contrario, o método recursivo é chamado:
		return num*fatorialRecursivo(num-1);
	}
}
```
É importante lembrar também que a recursividade trabalha com o conceito de pilha.

#Biblioteca
Blibiotecas é um arquivo de JajaScript que constitui por diversas funções, funções essas que se realizam tarefas úteis para sua página da web. Em quase todas bibliotecas há documentações que contém listas de funções disponíveis.

#### Biblioteca do JavaScript jQuery
O jQuery é uma biblioteva do JavaScripy que possibilita aos programadores melhorias, facilidade e rapidez em páginas Web. A sinttaxe utiliza variáveis em forma de setoresCSS como maneira de conectar efeitos e qualquer elemento alvo do DOM. Como essa biblioteca é um JavaScript ela pode ser aplicada a qualquer prjeto JavaScript.

### Referências
FEOFILOFF, Paulo. Algoritmos em linguagem C. Elsevier Brasil, 2009.
BACKES, André. Linguagem C: completa e descomplicada. Elsevier Brasil, 2018.
PINHO, Márcio Sorroglia. Apontadores/ Ponteiros/ Pointers. Programação em C/C++. Escola politécnica - GRU grupo de reslidade virtual - PUCRS.
CASAVELLA, Eduardo, Ponteiro em C. Escola deprogramação Intellectuale Tecnologia e Treinamento Ltda.
GARCIA, Fernando DEluno. Ponteiro em C: Definição. Embarcados, 14/12/2016.
https://docs.oracle.com/javase/tutorial/java/javaOO/arguments.html
https://www.ebah.com.br/content/ABAAAfq8kAA/funcoes
http://www.linhadecodigo.com.br/artigo/3316/recursividade-em-java.aspx#ixzz5qt1upbUu