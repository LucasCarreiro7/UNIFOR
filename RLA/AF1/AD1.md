<img src="https://drive.google.com/uc?id=1SOzRTjUt7cuBJpSqoK90fcAiKBrnpUJo" width="400">

**Curso:** Ciência da Computação <br>
**Disciplina:** Raciocínio Lógico Algorítmico <br>
**Código/Turma:** T160-40 <br>
**Professor:** Ricardo Carubbi <br>
**Data:** preencha com a data de envio <br>
**Aluno(a):** Lucas Carreiro Gomes <br>
**Matrícula:** 2417144 <br>

**1a chamada (Sim/Não):** Sim <br>
**2a chamada (Sim/Não):** Não

# Avaliação Diagnóstica 1

### Questão 03 - Soma de um conjunto de números

#### Pseudocódigo
```
ALGORITMO
DECLARE n, rep: inteiro, i, soma: real
INÍCIO
ESCREVA "Digite um número positivo"
LEIA n
soma == 0
SE n < 0
  ESCREVA "O número deve ser positivo"
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
A([INÍCIO]) --> B{{Digite um número}}
B --> C[\numero\]
C --> D[\soma = 0\]
D --> E{n < 0}
E --FALSE--> G[[i=1 ATÉ n PASSO 1]]
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
