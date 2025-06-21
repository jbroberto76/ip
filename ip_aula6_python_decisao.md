---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: ./img/layered-steps-right.svg
title: Estruturas de Decisão
exportFilename: ip_aula6_python_decisao
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
# {{ $slidev.configs.title }}
Introdução a Programação

---

# Objetivo de Aprendizagem
- Conhecer as estruturas de decisão em Python

---

# Agenda
- *Casting*
- `if`
- `if-else`
- `if-else-elif`

---
layout: section
---

# Casting

---
layout: quote
---

# O que é *casting*?

> **Casting** é um método para converter ou forçar que uma variável seja de um determinado tipo (`string`, `int`, `float`, etc). O Python realiza o *casting* automaticamente em algumas situações. Porém, em outros casos o programador precisa fazê-lo manualmente.

---

# Como fazer *casting*?

- Existem algumas funções úteis relacionadas com o *casting*
    - `type()`
    - `int()`
    - `float()`
    - `str()`

---

# Exemplo 1

```python {*}{class:'!children:text-xl'}
# Python converte automaticamente a para int 
a = 7
print(type(a)) 
# Python converte automaticamente b para float 
b = 3.0
print(type(b)) 
# Python converte automaticamente c para float por conta da soma
c = a + b 
print(c) 
print(type(c))
# Python converte automaticamente d to float por conta da multiplicação
d = a * b
print(d)
print(type(d))
```

---
layout: two-cols-header
---

# Exemplo 2

::left::
```python {*}{class:'!children:text-xl'}
# O que acontece ao executar o
# código abaixo?
idade = input('Qual sua idade?')
idade++
print('No próximo ano minha idade será', idade)
```

::right::
- O que acontece ao executar o código?
- Qual erro apresentado?
- Como corrigir?

---
layout: two-cols-header
---

# Exemplo 2
Corrigido

::left::

```python {*}{class:'!children:text-xl'}
# O que acontece ao executar o
# código abaixo?

# a funcao int() força que idade 
# seja do tipo int
idade = int(input('Qual sua idade?'))
# variável idade é incrementada
idade++
# a mensagem é exibida
print('No próximo ano minha idade será', idade)
```

::right::

- Na linha 6 é realizado o *casting*
- Agora pode-se realizar a operação de incremento (linha 8)
- Não há mais erro

---
layout: section
---

# Estruturas de decisão

---
layout: quote
---

# Declaração Condicional
> Declarações condicionais em Python são utilizadas para executar certas partes do códigos apenas se determinadas condições forem atendidas. Estas declarações controlam o fluxo do código.

---
layout: quote
---

# `if`
> A declaração `if` executa um bloco de código caso a condição declarada seja atendida (`True`).

---

# Exemplo 3

```python {*}{class:'!children:text-xl'}
idade = 20

if idade >= 16:
    print("Cidadão pode votar.")
```

---
layout: quote
---

# `if-else`
> A declaração `if-else` executa um bloco de código caso a condição declarada seja atendida (`True`), caso contrário outro bloco (`else`) é executado. **NUNCA** ambos os blocos serão executados. **SEMPRE** haverá pelo menos um dos blocos será executado.

---

# Exemplo 4

```python {*}{class:'!children:text-xl'}
age = 10

if age <= 12:
    print("Viajante gratuito.")
else:
    print("Viajante pagante.")
```

---
layout: default
---

# Exemplo 5

```python {*}{class:'!children:text-xl'}
nota = 45
res = "Aprovado" if nota >= 60 else "Reprovado"

print(f"Result: {res}")
```

---
layout: quote
---

# `elif`
> A declaração `elif` (`else + if`) permite a checagem de condições múltiplas e executar diferentes blocos de código de acordo com a condição verdadeira. **Cuidado**, apenas uma condição pode ser verdadeira, um único bloco de código é executado.

---

# Exemplo 6

```python {*}{class:'!children:text-xl'}
idade = 25

if idade <= 12:
    print("Criança.")
elif idade <= 19:
    print("Adolescente.")
elif idade <= 35:
    print("Jovem adulto.")
else:
    print("Adulto")
    print("Adulto.")
```

---
layout: quote
---

# `if-else` aninhados
> Pode-se criar estruturas de  `if-else` dentro de outras `if-else` criando um aninhamento. Utiliza-se `if-else` aninhados para checar condições em sequência.

---

# Exemplo 7
```python {*}{class:'!children:text-xl'}
idade = 70
e_membro = True

if idade >= 60:
    if e_membro:
        print("Desconto senior, 30%")
    else:
        print("Desconto senior 20%")
else:
    print("Não elegível para desconto senior.")
```

---
layout: section
---

# Exercícios

---
layout: statement
---

# 1
Modificar a condição do `if-else` para que o código dentro do `else` seja executado. A saída do *script* deve ser '2'.

---

# 1 (cont.)


```python {*}{class:'!children:text-2xl'}
option = 2

if option > 0:
    var = 1
else:
    var = 2
 print(var)
```
 
---
layout: statement
---

# 2
Criar um *script* em Python que recebe dois números do usuário e a operação aritmética desejada (soma, subtração, multiplicação e divisão). Em seguida a operação é realizada com os números e o resultado exibido ao usuário.

---
layout: statement
---

# 3
Crie um programa que simule um sistema de login simples. O programa deve pedir ao usuário um nome de usuário e uma senha e checar se:
- O nome de usuário tem pelo menos 3 caracteres.
- A senha tem exatamente 6 dígitos (e é numérica).

Se tudo estiver correto, exibir: "Login criado com sucesso!", Caso contrário, informar qual regra não foi atendida (ex: "Senha deve ter 6 dígitos numéricos!").

<!-- ```python
# Solicita nome de usuário e senha
usuario = input("Digite seu nome de usuário: ")
senha = input("Digite sua senha: ")

# Verifica as regras
if len(usuario) >= 3 and senha.isdigit() and len(senha) == 6:
    print("Login criado com sucesso!")
else:
    # Mensagens de erro específicas
    if len(usuario) < 3:
        print("Nome de usuário deve ter pelo menos 3 caracteres!")
    if not senha.isdigit() or len(senha) != 6:
        print("Senha deve ter 6 dígitos numéricos!")
``` 
-->

---

# Referências
- [https://www.geeksforgeeks.org/type-casting-in-python/](https://www.geeksforgeeks.org/type-casting-in-python/)
- [https://www.geeksforgeeks.org/conditional-statements-in-python/](https://www.geeksforgeeks.org/conditional-statements-in-python/)

---
layout: image
image: ./img/layered-steps-down.svg
---

# Prof. {{ $slidev.configs.author }}
# {{ $slidev.configs.author }}
jbroberto@ifce.edu.br
<br><br><br><br><br><br>
<PoweredBySlidev />