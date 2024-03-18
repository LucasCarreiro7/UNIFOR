# UNIFOR
**Nome:** Lucas Carreiro Gomes

**Disciplina:** Raciocínio Lógico Algorítmico

## Lista de exercícios 03

### Exercício 03

#### Pseudocódigo
```
ALGORITMO
DECLARE N1, N2,... Nn: INTEIRO
INÍCIO
ESCREVA "Digite uma sequência de números inteiros"
LEIA N1... Nn
soma == N1 + N2 +... + Nn
ESCREVA "A soma da sequência é:", soma
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite uma sequência de números inteiros:}}
B --> C[\numero inteiro\]
C --> D[soma == N1 + N2 +... + Nn]
D --> E{{"A soma da sequência é:", soma}}
E --> Z([FIM])
```
#### Teste de mesa
| N1 | N2 | Nn | soma | Saída |
| -- | -- | -- | -- | -- |
| 4 | 11 | -2 | 13 | A soma da sequência é: 13 |
| 0 | -7 | 19 | 12 | A soma da sequência é: 12 |

### Exercício 04

#### Pseudocódigo
```
