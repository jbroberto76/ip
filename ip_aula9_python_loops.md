---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: /layered-steps-right.svg
title: Estruturas de Repetição
description: Introdução a Programação
exportFilename: ip_aula9_python_loops
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
{{ $slidev.configs.description }}

---

# Objetivo de Aprendizagen
- Conhecer e aplicar estruturas de repetição

---

# Agenda
- Listas
- `for`
- `while`

---
layout: section
---

# Listas

---
layout: quote
---

# Lista

> Trata-se de uma coleção de dados agrupados (listados) através de um único nome. Seria como armazenar diversos valores usando um único nome de variável.

---

# Listas
Exemplos

- São definidas utilizando-se colchetes `[ ]` com elementos (itens) separados por vírgula

```python{*}{class:'!children:text-2xl'}
# exemplos de listas
notas = [9.0, 7.5, 5.6, 7.9, 0.0]
quant = [1, 6, 7, 8, 4, 6]
usuarios = ['@joaosilva', '@mpaula12', '@jfs']
info = ['Ricardo Lima', 37, 127.2]
```

---

# Listas 
Tipo de dado

```python{*}{class:'!children:text-2xl', lines: false}
>>> l = []
>>> type(l)
<class 'list'>
```

---

# Acessando Itens
Indexação

> Cada item possui um índice para acesso individual

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja']
print(f'Primeira fruta: {frutas[0]}')
print(f'Segunda fruta: {frutas[1]}')
print(f'Terceira fruta: {frutas[2]}')
```

---

# Acessando Itens
Índices negativos

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja']
```

| **Índice**  |  -4  |   -3   |   -2  |    -1   |
|-------------|:----:|:------:|:-----:|:-------:|
| **Valores** | maçã | banana | limão | laranja |

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja']
print(f'Última fruta: {frutas[-1]}')
print(f'Penúltima fruta: {frutas[-2]}')
```

---

# Erros típicos

- Acesso fora da faixa
    - `IndexError: list index out of range`
- Índices não inteiros
    - `TypeError: list indices must be integers or slices, not float`

---

# Fatiamento
*Slicing*

- Extrair uma sublista ou fração de uma lista existente
- Sintaxe: `lista[inicio:fim:passo]`
    - `inicio` índice inicial do fatiamento
    - `fim` índice do último item do fatiamento mais um
    - `passo` quantidade de saltos de cada item (**opcional**)

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja']
print(f'Algumas frutas: {frutas[0:3]}')
print(f'Outras frutas: {frutas[0:5:2]}')
```

---

# Funções especiais
Adicionar, ordenar e apagar itens

```python{1-5|6|8}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja']
frutas.append('abacaxi')
print(frutas)
frutas.append('kiwi')
print(frutas)
frutas.sort()
print(frutas)
frutas.remove('kiwi')
print(frutas)
```

---
layout: section
---

# `for`

---
layout: quote
---

# Estruturas de repetição

> São estruturas que permitem a execução de blocos de código uma determinada quantidade de vezes ou até que uma condição seja atingida.

---

# `for`
*Loops* ou laços

- Permite percorrer itens de uma lista ou qualquer outro tipo iterável (*iterable*)

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja', 'abacaxi']
for f in frutas:
    print(f)
print('Estas são as frutas disponíveis')
```

---

# `for`
*Loops* ou laços

- Permite percorrer itens de uma lista ou qualquer outro tipo iterável (*iterable*)

```python{*}{class:'!children:text-2xl'}
texto = 'algum conteúdo'
for c in texto:
    print(c)
```

---

# `for`
Exemplo 1

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja', 'abacaxi']
cont = 0
frutas.sort()
for f in frutas:
    cont += 1
    print(f'{str(cont)} - {f.title()}')
print(f'Estas são as {cont} frutas em ordem')
```

---

# `for`
Exemplo 2 `continue`

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja', 'abacaxi']
for f in frutas:
    if f == 'banana':
        continue
    else:
        print(f)
print('Lista de frutas sem banana')
```

---

# `for`
Exemplo 3 `break`

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja', 'abacaxi']
for f in frutas:
    if f == 'banana':
        print(f)
        break
print('Há banana na lista')
```

---

# `range()`
Exemplo 4

- `range()` cria uma sequência de números
- É útil quando não há um iterável no código e deseja-se realizar um *loop*
<br><br>
```python{*}{class:'!children:text-2xl'}
for x in range(6):
  print(x)
```

---

# `range()`
Exemplo 5 (números pares entre 11 e 21)

```python{*}{class:'!children:text-2xl'}
for n in range(11, 22):
    if (n % 2 == 0):
        print(n)
    else:
        continue
```

---

# `range()`
Exemplo 6 (soma dos números ímpares entre 11 e 21)

```python{*}{class:'!children:text-2xl'}
soma = 0
for n in range(11, 22):
    if n % 2:
        soma += n
```

---
layout: section
---

# `while`

---

# `while`

- Executa os comandos do bloco enquanto uma condição é verdadeira

```python{*}{class:'!children:text-2xl'}
i = 1
while i < 6:
  print(i)
  i += 1
```

---

# Utilizando `while`
Exemplo 7

```python{*}{class:'!children:text-2xl'}
frutas = ['maçã', 'banana', 'limão', 'laranja', 'abacaxi']
cont = 0
frutas.sort()
while cont<len(frutas):
    cont += 1
    print(f'{str(cont)} - {frutas[cont-1].title()}')
print(f'Estas são as {cont} frutas em ordem')
```

---

# Exemplo 8
Somar números até o usuário digitar 0

```python{*}{class:'!children:text-2xl'}
soma = 0

while True:
    num = int(input("Digite um número (0 para sair): "))
    if num == 0:
        break
    soma += num

print("A soma dos números digitados é:", soma)
```

---

# Laços infinitos

- `while` permite criar laços infinitos
- Laços que são executados indefinidamente, pois a condição pode não ser atendida nunca

---

# Laços infinitos
Exemplo 9 (controle de opções do usuário e saída de um programa)

```python{*}{class:'!children:text-xl'}
while True:
    print("=== Menu ===")
    print("1. Sacar dinheiro\n2. Depositar dinheiro")
    print("3. Consultar saldo\n0. Sair")
    opcao = input("Escolha uma opção (1-3): ")
    if opcao == '1':
        print("Realizando saque")
    elif opcao == '2':
        print("Realizando depósito")
    elif opcao == '3':
        print("Seu saldo é .....")
    else:
        print("Opção inválida. Tente novamente.")
        break
```

---

# `while` versus `for`

|                     | `for`                                       | `while`                                   |
|----------------------------------|--------------------------------------------------|------------------------------------------------|
| **Quando usar?**                  | Quando o número de iterações é conhecido ou finito | Quando o número de iterações **é incerto**     |
| **Controle da repetição**        | Itera sobre uma **sequência** ou intervalo fixo  | Repetição controlada por uma **condição lógica** |
| **Exemplo típico**               | `for i in range(5):`                             | `while x < 10:`                                |
| **Interrupção manual**          | Pode usar `break`, mas geralmente não precisa    | Normalmente usa `break` ou altera a condição   |
| **Loops infinitos** | ✅ Sim (se bem definido)                        | ❌ Pode entrar em loop infinito      |
| **Sintaxe com coleções**         | Ideal para listas, tuplas, strings, etc.         | Não é ideal para iteração direta em coleções   |

---
layout: section
---

# Exercícios

---

# 1

> Criar um *script* em Python que recebe um texto do usuário e conta a quantidade de palavras desse texto.

---

# 2
> Modifique o *script* do exercício anterior para que seja feita a contagem das vogais do texto passado pelo usuário.

---

# 3
> Escrever o jogo **Adivinhe o Número**. Um número aleatório entre 0 e 10 é iniciado em uma variável. Em seguida o usuário deve tentar adivinhar esse número através de uma quantidade ilimitada de tentativas. **Sugestão**: utilize a função `randint()`, conforme mostrado no exemplo para gerar o número aleatório (É necessário adicionar o módulo `random`).

```python{*}{class:'!children:text-2xl'}
from random import randint
# como usar o randint?
numero_aleatorio = randint(0, 10)
print(numero_aleatorio)
```

---

# Referências
- [Python.org](https://docs.python.org/pt-br/3.13/tutorial/controlflow.html)
- [Python Academy](https://pythonacademy.com.br/blog/estruturas-de-repeticao)

---
src: /snippets/end.md
---
