# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo
## Exercício 3
### Fluxograma

````mermaid
flowchart TD
A([Início]) --> B{{ Digite seu número:}}
B --> C[/Número/]
C --> D{Número > 0}
D --NAO--> E[O número não é positivo]
D --SIM--> F[Resto = número % 2]
E --> Z([FIM])
F --> G{Resto == 0}
G --NAO--> H[O número é impar]
G --SIM--> I[O número é par]
H --> Z
I --> Z
````
### Pseudocódigo
````
1 ALGORITMO verifica_par_impar
2 DECLARE Número, Resto NÚMERICO
3 ESCREVA "Digite um número" 
4 LEIA Número
5 SE Número > 0
6 	Resto = Número % 2
7 	SE Resto == 0 ENTÂO
8 		ESCREVA "O número é par"
9 	SENÂO
10 		ESCREVA "O número é impar"
11 SENÂO
12 	ESCREVA ESCREVA "O número não é positivo"
13 FIM_ALGORITMO
````
