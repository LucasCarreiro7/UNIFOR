# UNIFOR
**Nome:** Lucas Carreiro Gomes

**Disciplina:** Raciocínio Lógico Algorítmico

## Lista de exercícios 02

### Exercício 01

#### Pseudocódigo
```
ALGORITMO
DECLARE N1, N2, N3, N4: inteiro
INÍCIO
ESCREVA “Digite quatro números inteiros”
LEIA N1, N2, N3, N4
M == (N1 + N2 + N3 + N4) / 4
ESCREVA “A média é igual a:”, M
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite quatro números inteiros}}
B --> C[\numero inteiro\]
C --> D["M == (N1 + N2 + N3 + N4) / 4"]
D --> E{{A média é igual a:, M}}
E --> Z([FIM])
```
#### Teste de mesa
| N1 | N2 | N3 | N4 | M | Saída |
| -- | -- | -- | -- | -- | -- |
| 7 | 10 | 11 | 18 | 11,5 | A média é igual a: 11,5 |
| 0 | 0 | 0 | 0 | 0 | A média é igual a: 0 |
| -2 | -4 | -7 | -10 | -5,75 | A média é igual a: 5,75 |

### Exercício 02

#### Pseudocódigo
```
