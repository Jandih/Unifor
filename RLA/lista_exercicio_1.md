# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo

## Exercício 1
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite a primeira nota:}}
B --> C[\N1\]
C --> D{{Digite a segunda nota:}}
D --> E[\N2\]
E --> F[M = N1 + N2 / 2]
F --> G{M >= 7}
G --NÃO--> H{{Reprovado}}
H --> I([Fim])
G --SIM--> J{{Aprovado}}
J --> I
````
### Pseudocódigo
````
1 ALGORITMO calcular_média
2 DECLARE N1, N2, M: REAL
3 INÍCIO
4 ESCREVA "Digite suas notas" 
5 LEIA N1, N2
6 M = (N1 + N2) / 2
7 SE M >= 7 ENTÃO
8 	ESCREVA "Aprovado"
9 SENÃO
10 	ESCREVA "Reprovado"
11 FIM_SE
12 FIM
````

## Exercício 2
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite o salário atual:}}
B --> C[\X\]
C --> D{X <= 500}
D --NÃO--> E[Y = 1.10 * X]
D --SIM--> F[Y = 1.20 * X]
E --> G{{'Novo salário:', Y}}
F --> G
G --> H([Fim])
````
### Pseudocódigo
````
1 ALGORITMO calcular_novo_salário
2 DECLARE X, Y: REAL
3 INÍCIO
4 ESCREVA "Digite o salário atual:" 
5 LEIA X
6 SE X <= 500
7 	ENTÃO Y = 1.20 * X
8 SENÃO
9 	Y  = 1.10 * X
10 FIM_SE
11 ESCREVA "Novo salário:", Y
12 FIM
````

## Exercício 3
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite seu número:}}
B --> C[\Número\]
C --> D{Número > 0}
D --NÃO--> E{{O número não é positivo}}
D --SIM--> F[Resto = número % 2]
E --> Z([Fim])
F --> G{Resto == 0}
G --NÃO--> H{{O número é impar}}
G --SIM--> I{{O número é par}}
H --> Z
I --> Z
````
### Pseudocódigo
````
1 ALGORITMO verificar_par_impar
2 DECLARE Número, Resto: INTEIRO
3 INÍCIO
4 ESCREVA "Digite um número" 
5 LEIA Número
6 SE Número > 0
7 	Resto = Número % 2
8   SE Resto == 0 ENTÃO
9 		ESCREVA "O número é par"
10   SENÃO
11 		ESCREVA "O número é impar"
12   FIM_SE
13 SENÃO
14 	ESCREVA "O número não é positivo"
15 FIM_SE
16 FIM
````

## Exercício 4
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Insira a idade:}}
B --> C[\I\]
C --> D{I >= 18}
D --SIM--> E{{Pode tirar a CNH}}
D --NÃO--> F[anos_faltam = 18 - I]
F --> G{{'Faltam', anos_faltam, 'anos para tirar a CNH'}}
G --> H
E --> H([Fim])
````
### Pseudocódigo
````
1 ALGORITMO determinar_cnh
2 DECLARE I, anos_faltam: INTEIRO
3 INÍCIO
4 ESCREVA "Insira a idade:" 
5 LEIA I
6 SE I >= 18 ENTÃO
7 	ESCREVA "Pode tirar a CNH"
8 SENÃO
9 	anos_faltam = 18 - I
10 	ESCREVA "Faltam", anos_faltam, "ano(s) para tirar a CNH"
11 FIM_SE
12 FIM
````
