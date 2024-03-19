<img src="https://drive.google.com/uc?id=1SOzRTjUt7cuBJpSqoK90fcAiKBrnpUJo" width="400">

**Curso:** Ciência da Computação <br>
**Disciplina:** Raciocínio Lógico Algorítmico <br>
**Código/Turma:** T160-40 <br>
**Professor:** Ricardo Carubbi <br>
**Data:** 20/03/2024 <br>
**Aluno(a):** Lucas Carreiro Gomes <br>
**Matrícula:** 2417144 <br>

**1a chamada (Sim/Não):** Sim <br>
**2a chamada (Sim/Não):** Não

# Avaliação Diagnóstica 1

### Questão 01 - Troca dos valores de duas variáveis

#### Pseudocódigo
```
ALGORITMO
DECLARE a,b: REAL
INÍCIO
a = valor_de_a
ESCREVA "Digite duas variáveis"
LEIA a,b
ESCREVA "Valores das variáveis:", a, b
a = b
b = valor_de_a
ESCREVA "Valores após a troca:", a, b
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite duas variáveis}}
B --> C[\a, b\]
C --> D[a = valor_de_a]
D --> G[a = b]
G --> H[b = valor_de_a]
H --> I{{Valores após a troca:, a, b}}
I --> Z([FIM])
```
#### Teste de mesa
| a | b | valor_de_a | a | b | Saída |
| -- | -- | -- | -- | -- | -- |
| 7 | 2 | 7 | 2 | 7 | 2, 7 |

### Questão 02 - Contagem

#### Pseudocódigo
```
ALGORITMO
DECLARE nota: REAL, cont, n: INTEIRO
INÍCIO
cont == 0
ESCREVA "Digite um conjunto de notas"
LEIA n
SE nota > 100 ou nota < 0
  REPITA
  ESCREVA "Apenas notas entre 0 e 100 são válidas"
  ATE_QUE n <= 100 e n >= 0
SENÃO
  PARA i de 1 ATÉ n FAÇA
    SE nota >= 50
      cont == cont + 1
    SENÃO
      cont == cont
  FIM_PARA
  ESCREVA "A quantidade de aprovados é:", cont
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite um conjunto de notas}}
B --> C[\n, notas, cont\]
C --> D[\cont = 0\]
D --> D2{nota > 100 ou nota < 0}
D2 --FALSE--> E[[i=1 ATÉ n]]
D2 --TRUE--> D3{{Apenas notas entre 0 e 100 são válidas}}
D3 --> B
E --> H{{A quantidade de aprovados é:, cont}}
E --> F{nota >= 50}
F --FALSE--> G2[cont = cont]
G2 --LOOP--> E
F --TRUE--> G[cont = cont + 1]
G --LOOP--> E
H --> Z([FIM])
```
#### Teste de mesa
| it | n | nota | nota >= 50 | cont | aprovados |
| -- | -- | -- | -- | -- | -- |
| 1 | 10 | 90 | V | 1 |  |
| 2 | 10 | 78 | V | 2 |  |
| 3 | 10 | 85 | V | 3 |  |
| 4 | 10 | 45 | F | 3 |  |
| 5 | 10 | 92 | V | 4 |  |
| 6 | 10 | 82 | V | 5 |  |
| 7 | 10 | 40 | F | 5 |  |
| 8 | 10 | 88 | V | 6 |  |
| 9 | 10 | 35 | F | 6 |  |
| 10 | 10 | 65 | V | 7 |  |

### Questão 03 - Soma de um conjunto de números

#### Pseudocódigo
```
ALGORITMO
DECLARE n, rep: INTEIRO, i, soma: REAL
INÍCIO
ESCREVA "Digite um número não-negativo"
LEIA n
soma == 0
SE n < 0
  REPITA
  ESCREVA "O número deve ser positivo"
  ATE_QUE n >= 0
SENÃO
  PARA i de 1 ATÉ n PASSO 1 FAÇA
    soma == soma + i
    ESCREVA "A soma atual é:", soma
  FIM_PARA
  ESCREVA "A soma final é:",
FIM_ALGORITMO
```
#### FLUXOGRAMA
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite a quantidade de números}}
B --> C[\numero\]
C --> D[\soma = 0\]
D --> D2[i=1]
D2 --> E{n < 0}
E --FALSE--> G[[i=1 ATÉ n]]
G --> J{{A soma final é:, soma}}
G --> H[soma = soma + i]
H --> I{{A soma atual é:, soma}}
I --LOOP--> G
E --TRUE--> F{{O número deve ser positivo}}
F -->B
J --> Z([FIM])
```
#### Teste de mesa
| it | n | soma | i | soma = soma + i |
| -- | -- | -- | -- | -- |
| 1 | 5 | 0 | 1 | 1 |
| 2 | 5 | 1 | 2 | 3 |
| 3 | 5 | 3 | 3 | 6 |
| 4 | 5 | 6 | 4 | 10 |
| 5 | 5 | 10 | 5 | 15 |

### Questão 05 - Cálculo fatorial

#### Pseudocódigo
```
ALGORITMO
DECLARE n, fatorial: INTEIRO
INÍCIO
ESCREVA "Digite um número não-negativo"
LEIA n
fatorial == 1
SE n < 0
  REPITA
  ESCREVA "O número deve ser positivo"
  ATE_QUE n >= 0
SENAO
  PARA i de 1 ATÉ n FAÇA
  fatorial = fatorial * i
  FIM_PARA
  ESCREVA "O fatorial de", n, "é", fatorial
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite um número não-negativo}}
B --> C[\numero, fatorial\]
C --> D[\fatorial = 1\]
D --> E{n < 0}
E --FALSE--> G[[i=1 ATÉ n]]
G --i>n--> I{{O fatorial de, n, é, fatorial}}
G --i=1,2...n--> H[fatorial = fatorial * i]
H --LOOP--> G
E --TRUE--> F{{O número não pode ser negativo}}
F --> B
I --> Z([FIM])
```
#### Teste de mesa
| it | n | i | fatorial |
| -- | -- | -- | -- |
| 1 | 5 | 1 | 1 |
| 2 | 5 | 2 | 2 |
| 3 | 5 | 3 | 6 |
| 4 | 5 | 4 | 24 |
| 5 | 5 | 5 | 120 |

### Questão 6 - Geração da sequência de Fibonacci

#### Pseudocódigo
```
ALGORITMO
DECLARE a, b, n, next: INTEIRO
INÍCIO
ESCREVA "Digite o número de termos da sequência"
LEIA n
ESCOLHA
  CASO n <= 0
    ESCREVA "O número deve ser positivo"
  CASO n = 1
    ESCREVA "0"
  CASO n = 2
    ESCREVA "0, 1"
  CASO n > 2
    a == 0
    b == 1
    PARA i de 3 ATÉ n FAÇA
      ESCREVA "0, 1"
      next = a + b
      ESCREVA next
      a = b
      b = next
    FIM_PARA
FIM_ESCOLHA
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite o número de termos da sequência}}
B --> C[\numero\]
C6 --> C7{{O número deve ser positivo}}
C7 --> Z
C --> C2{n = 1}
C2 --> C3{{0}}
C --> C4{n = 2}
C3 --> Z([FIM])
C4 --> C5{{1}}
C5 --> Z
C --> C6{n <=  0}
C --> C8{n > 2}
C8 --> D[\a = 0\]
D --> E[\b = 0\]
E --> F[[i=1 ATÉ n]]
F --> G{{0, 1}}
G --> H[next = a + b]
H --> I[a = b]
I --> J[b = next]
J --LOOP-->F
F --> Z
```
#### Teste de mesa
| it | n  | a  | b  | i  | saída | next | a = b | b = next |
| -- | -- | -- | -- | -- | -- | -- | -- | -- |
| 1  | 5  | 0  | 1  | 1  | 0 | 0 + 1 = 1 | 1 | 1 |
| 2  | 5  | 1  | 1  | 2  | 1 | 1 + 1 = 2 | 1 | 2 |
| 3  | 5  | 1  | 2  | 3  | 1 | 1 + 2 = 3 | 2 | 3 |
| 4  | 5  | 2  | 3  | 4  | 2 | 2 + 3 = 5 | 3 | 5 |
| 4  | 5  | 3  | 5  | 5  | 3 | 3 + 5 = 8 | 5 | 8 |

### Questão 7 - Inversão dos dígitos de um número inteiro

#### Pseudocódigo
```
ALGORITMO
DECLARE n, num_inv, digito: INTEIRO
INÍCIO
ESCREVA "Digite um número positivo"
LEIA n
num_inv == 0
SE n < 0
  ESCREVA "O número deve ser positivo"
SENAO
  ENQUANTO n > 0
    digito == n % 10
    num_inv == num_inv * 10 + digito
    n == n / 10
  FIM_ENQUANTO
  ESCREVA "O número invertido é:", num_inv
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite um número inteiro}}
B --> C[\numero, num_inv, digito\]
C --> D[\num_inv = 0\]
D -->E{n < 0}
E --FALSE--> G{n > 0}
G --FALSE--> K{{O número invertido é, num_inv}}
K --> Z([FIM])
G --TRUE--> H[digito = n % 10]
H --> I[num_inv = num_inv * 10 + digito]
I --> J[n == n / 10]
J --LOOP--> G
E --TRUE--> F{{O número deve ser positivo}}
F --> B
```
#### Teste de mesa
| it | n | num_inv | digito | num_inv | n |
| -- | -- | -- | -- | -- | -- |
| 1 | 1234 | 0 | 4 | 4 | 123 |
| 2 | 123 | 4 | 3 | 43 | 12 |
| 3 | 12 | 43 | 2 | 432 | 1 |
| 4 | 1 | 432 | 1 | 4321 |  |
