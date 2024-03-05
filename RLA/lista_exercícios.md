# UNIFOR
**Nome:** Lucas Carreiro
**Disciplina**: Raciocínio Lógico Algorítmico

## Exercício 03
### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite um número:}}
B --> C[\número\]
C --> D{número > 0}
D --NÃO--> F[O número não é positivo]
D --SIM--> E[resto = número % 2]
F --> Z([FIM])
E --> G{resto == 0}
G --NÃO--> H{{O número é ímpar!}}
G --SIM--> I{{O número é par!!}}
H --> Z
I --> Z
```
