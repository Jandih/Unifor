# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo

## Exercício 1
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite suas notas:}}
B --> C[/N1, N2/]
C --> D[M = N1 + N2 / 2]
D --> E{M >= 7}
E --NÃO--> F[Reprovado]
F --> H([Fim])
E --SIM--> G[Aprovado]
G --> H
````
### Pseudocódigo
````
1 ALGORITMO calcular_média
2 DECLARE N1, N2, M: NÚMERICO
3 ESCREVA "Digite suas notas" 
4 LEIA N1, N2
5 M = (N1 + N2) / 2
6 SE M >= 7 ENTÃO
8 	ESCREVA "Aprovado"
9 SENÃO
10 	ESCREVA "Reprovado"
11 FIM_ALGORITMO
````

## Exercício 2
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite o salário atual:}}
B --> C[/X/]
C --> D{X <= 500}
D --NÃO--> E[Y = 1.10 * X]
D --SIM--> F[Y = 1.20 * X]
E --> G[Novo salário: Y]
F --> G
G --> H([Fim])
````
### Pseudocódigo
````
1 ALGORITMO calcular_novo_salário
2 DECLARE X, Y: NÚMERICO
3 ESCREVA "Digite o salário atual:" 
4 LEIA X
5 SE X <= 500
6 	ENTÃO Y = 1.20 * X
7 SENÃO
8 	Y  = 1.10 * X
9 ESCREVA "Novo salário:", Y
10 FIM_ALGORITMO
````

## Exercício 3
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite seu número:}}
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
2 DECLARE Número, Resto: NÚMERICO
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

## Exercício 4
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Insira a idade:}}
B --> C[/I/]
C --> D{I >= 18}
D --SIM--> E[Pode tirar a CNH]
D --NÃO--> F[anos_faltam = 18 - I]
F --> G[Faltam, anos_faltam, anos para tirar a CNH]
G --> H
E --> H([Fim])
````
### Pseudocódigo
````
1 ALGORITMO determinar_cnh
2 DECLARE I, anos_faltam: NÚMERICO
3 ESCREVA "Insira a idade:" 
4 LEIA I
5 SE I >= 18 ENTÃO
6 	ESCREVA "Pode tirar a CNH"
7 SENÃO
8 	anos_faltam = 18 - I
9 	ESCREVA "Faltam", anos_faltam, "ano(s) para tirar a CNH"
10 FIM_ALGORITMO
````
