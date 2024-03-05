# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo

## Exercício 1
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{ Digite suas notas:}}
B --> C[/N1, N2/]
C --> D{N1 e N2 >= 4}
D --NÃO--> E[Reprovado]
E --> H([Fim])
D --SIM--> F[N1 + N2 / 2]
F --> G[Aprovado]
G --> H
````
### Pseudocódigo
````
1 ALGORITMO calcular_média
2 DECLARE N1, N2 NÚMERICO
3 ESCREVA "Digite suas notas" 
4 LEIA N1, N2
5 SE N1 e N2 >= 4
6 	(N1 + N2) / 2 ENTÃO
7 		ESCREVA "Aprovado"
8 SENÃO
9 	ESCREVA "Reprovado"
10 FIM_ALGORITMO
````

## Exercício 3
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{ Digite seu número:}}
B --> C[/Número/]
C --> D{Número > 0}
D --NÃO--> E[O número não é positivo]
D --SIM--> F[Resto = número % 2]
E --> Z([Fim])
F --> G{Resto == 0}
G --NÃO--> H[O número é impar]
G --SIM--> I[O número é par]
H --> Z
I --> Z
````
### Pseudocódigo
````
1 ALGORITMO verificar_par_impar
2 DECLARE Número, Resto NÚMERICO
3 ESCREVA "Digite um número" 
4 LEIA Número
5 SE Número > 0
6 	Resto = Número % 2
7 	SE Resto == 0 ENTÃO
8 		ESCREVA "O número é par"
9 	SENÃO
10 		ESCREVA "O número é impar"
11 SENÃO
12 	ESCREVA "O número não é positivo"
13 FIM_ALGORITMO
````
