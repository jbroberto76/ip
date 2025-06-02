---
theme: default
lineNumbers: true
layout: intro
title: Estruturas de Controle de Fluxo
author: José Roberto Bezerra
---

# Estruturas de Controle de Fluxo

Introdução a Programação

---
layout: section
---

# Listas

---
layout: quote
---

> Python possui alguns tipos de dados **compostos**, ou seja que podem agrupar outros valores. O mais versátil é o tipo lista (*list*)

---
layout: default
---

# Listas
- Além dos tipos básicos (`int`, `float`, `str`, etc) existem os tipos de dados compostos
    - `dictionary`
    - `sets`
    - `lists`
- Para definir uma lista basta utilizar `[` e `]` como delimitares e separar os valores com `,`
- Exemplo:
```python{*}{class:'!children:text-2xl'}
squares = [1, 4, 9, 16, 25]
```

---
layout: default
---

# Listas
- Uma única lista pode conter ítens de tipos distintos
- Exemplos
```python{*}{class:'!children:text-2xl'}
spam = ['bacon', 'eggs', 42]
l = [1, 3.14, ['a', 'b', 'c']]
```

---
layout: default
---

# Indexação
- As listas permitem o acesso a um elemento individual através da **indexação**
- Exemplo:
```python{*}{class:'!children:text-2xl'}
squares = [1, 4, 9, 16, 25]
squares[0] # retorna o primeiro elemento
squares[1] # retorna o segundo elemento
squares[-1] # retorna o ultimo elemento
```

---
layout: default
---

# `Strings` e Listas
- As `strings` são um tipo especial de lista
- Também permitem a indexação
- Exemplos:
```python{*}{class:'!children:text-2xl'}
my_text = 'hello'
my_text[0] # retorna h
my_text[1] # retorna e
my_text[-1] # retorna o
```

- As `strings` são imutáveis (*immutable*), as listas são mutáveis (*mutable*)

---
layout: default
---

# Tipos Mutáveis x Imutáveis
- Exemplo de tipo de mutável
```python{*}{class:'!children:text-2xl'}
cubes = [1, 8, 27, 65, 125] # como corrigir o quarto elemento para 64?
cubes[3] = 64
```

- Exemplo de tipo imutável
```python{*}{class:'!children:text-2xl'}
my_str = 'hellu' # como corrigir o ultimo elemento?
my_str[-1] = 'o' # qual o erro apresentado ?
```

---
layout: default
---

# Concatenação de Listas
```python{*}{class:'!children:text-2xl'}
squares = [1, 4, 9, 16, 25]
squares + [36, 49, 64, 81, 100]
```

---
layout: default
---

# Métodos para Listas
```python{*}{class:'!children:text-2xl'}
squares = [1, 4, 9, 16, 25]
squares.append(36) # adiciona novo item ao final da lista
squares.pop() # remove o ultimo elemento da lista
squares.clear() # remove todos os itens da lista
squares.count() # retorna a quantidade de itens da lista
```

---
layout: section
---

# Controle de Fluxo


---
layout: quote
---

> Estruturas de controle de fluxo permitem que partes do código sejam executadas repetidas vezes ou não, de acordo com condições especificadas pelo programador.

---
layout: default
---

# `for`

- A estrutura `for` **itera** sobre uma lista ou *string* realizando operações na mesma sequência em que os itens estão ordenados
- Exemplo:
```python{*}{class:'!children:text-2xl'}
words = ['gato', 'cachorro', 'janela']
for w in words:
    print(w, len(w))
```

---
layout: default
---

# `range()`
- Caso não tenha sido definido uma lista, pode-se utilizar uma sequência de números simples com `range()`
- Exemplos:
```python{*}{class:'!children:text-xl'}
for i in range(5):
    print(i)
```

```python{*}{class:'!children:text-xl'}
squares = []
for i in range(5):
    squares.append(i**2)
```

```python{*}{class:'!children:text-xl'}
list(range(5, 10))
list(range(0, 10, 3))
list(range(-10, -100, -30))
```

---
layout: default
---

# `while`
- A estrutura `while` executa comandos em ciclicamente (em *loop*)enquanto a condição estabelecida for válida (`true`)
- Exemplo:
```python{*}{class:'!children:text-2xl'}
i = 1
while i < 6:
  print(i)
  i += 1
```

---
layout: default
---

# `while` com `break`
- A declaração `break` finaliza a execução laço (*loop*)
- Exemplo:
```python{*}{class:'!children:text-2xl'}
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```

---
layout: default
---

# `while` com `continue`
- A declaração `continue` finaliza a iteração atual e dá continuidade a execução laço na próxima iteração
- Exemplo:
```python{*}{class:'!children:text-2xl'}
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```

---
layout: default
---

# `while` com `else`
- A declaração `else` permite que um bloco de código seja executado quando a condição for falsa (`False`)
- Exemplo:
```python{*}{class:'!children:text-2xl'}
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i não vale mais 6")
```

---
layout: fact
---

# Exemplo 1
Escrever um *script* em Python que recebe um número inteiro positivo (`n`) do usuário e exibe o quadrado dos números de 1 até `n`.

---
layout: default
---

# Solução 
```python{1|1-2|6-7|2-3|3-5|*}{class:'!children:text-2xl'}
n = input('Digite um número inteiro positivo:')
if n.isdigit():
    n = int(n)
    for i in range(n+1):
        print(f'O quadrado de {i} vale {i**2}.')
else:
    print('Número digitado não é inteiro positivo')
```

---
layout: fact
---

# Exemplo 2
Refazer o exercício anterior com as seguintes modificações:
- Utilizar `while` ao invés de `for`
- Ao invés de exibir os valores na saída, guardar numa lista (`l`)
- Exibir a lista ao final do *script*

---
layout: default
---

# Solução 
```python{1,10-11|2-5|2-6|2-7|2-8|2-9|*}{class:'!children:text-2xl'}
n = input('Digite um número inteiro positivo:')
if n.isdigit():
    n = int(n)
    i = 1
    l = []
    while i <= n:
        l.append(i**2)
        i += 1
    print(l)
else:
    print('Número digitado não é inteiro positivo')
```

---
layout: fact
---

# Exercício 1
Escrever um *script* em Python que exiba a tabuada de Soma ou Multiplicação, conforme opção do usuário. Além da operação, o usuário também deverá escolher qual o número da tabuada. A saída deve similar a mostrada a seguir:
- 1 + 1 = 2
- 1 + 2 = 3
...
- 1 + 10 = 11

Incluir título e  mensagem de encerramento. Verificar se números inteiros positivos são digitados pelo usuário. Caso contrário, mensagem de erro ou opção de digitar novamente.


---
layout: default
---

# Referências
- [Python.ORG](https://docs.python.org/3/tutorial/controlflow.html)
- [W3 Schools](https://www.w3schools.com/python/python_while_loops.asp)