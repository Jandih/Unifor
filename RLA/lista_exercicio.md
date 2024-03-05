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
