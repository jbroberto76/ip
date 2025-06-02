---
theme: default
lineNumbers: true
layout: intro
title: Estruturas de Decisão
author: José Roberto Bezerra
---

# Estruturas de Decisão

Introdução a Programação

---
layout: section
---

# Casting


---
layout: quote
---

# O que é *casting*?

> **Casting** é um método para converter ou forçar que uma variável seja de um determinado tipo (```string```, ```int```, ```float```, etc). O Python realiza o *casting* automaticamente em algumas situações. Porém, em outros casos o programador precisa fazê-lo manualmente.

---
layout: default
---

# Como fazer *casting*?

- Existem algumas funções úteis relacionadas com o *casting*
    - ```type()```
    - ```int()```
    - ```float()```
    - ```str()```

---
layout: default
---

# Exemplo 1

```python
# Python converte automaticamente  
# a para int 
a = 7
print(type(a)) 

# Python converte automaticamente  
# b para float 
b = 3.0
print(type(b)) 

# Python converte automaticamente  
# c para float por conta da soma
c = a + b 
print(c) 
print(type(c))

# Python converte automaticamente  
# d to float por conta da multiplicação
d = a * b
print(d)
print(type(d))
```

---
layout: two-cols-header
---

# Exemplo 2

::left::
```python
# O que acontece ao executar o
# código abaixo

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

# Exemplo 2 - Corrigido

::left::

```python
# O que acontece ao executar o
# código abaixo

# a funcao int() força que idade 
# do tipo int
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

# ```if```
> A declaração ```if``` executa um bloco de código caso a condição declarada seja atendida (```True```) e outro bloco caso não seja atendida (```False```).

---
layout: default
---

# Exemplo 3

```python
idade = 20

if idade >= 16:
    print("Cidadão pode votar.")
```

---
layout: default
---

# Exemplo 4

```python
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

```python
nota = 45
res = "Aprovado" if nota >= 60 else "Reprovado"

print(f"Result: {res}")
```

---
layout: quote
---

# ```elif```
> A declaração ```elif``` significa ```else + if```. Permite a checagem de condições múltiplas e executar diferentes blocos de código de acordo com a condição verdadeira. **Cuidado**, apenas uma condição pode ser verdadeira, um único bloco de código é executado.

---
layout: default
---

# Exemplo 6

```python
idade = 25

if idade <= 12:
    print("Criança.")
elif age <= 19:
    print("Adolescente.")
elif age <= 35:
    print("Jovem adulto.")
else:
    print("Adult.")
```

---
layout: quote
---

# ```if-else``` aninhados
> Pode-se criar estruturas de  ```if-else``` dentro de outras ```if-else``` criando um aninhamento. Utiliza-se ```if-else``` aninhados para checar condições em sequência.

---
layout: default
---

# Exemplo 7
```python
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
layout: fact
---

# Exercício 1
Modificar a condição do ```if-else``` para que o código dentro do ```else``` seja executado. A saída do *script* deve ser '2'.

---
layout: full
---

```python
option = 2

if option > 0:
    var = 1
else:
    var = 2
 print(var)
 ```
    
---
layout: fact
---

# Exercício 2
Criar um *script* em Python que recebe dois números do usuário e a operação aritmética desejada (soma, subtração, multiplicação e divisão). Em seguida a operação é realizada com os números e o resultado exibido ao usuário.

---
layout: default
---

# Referências
- [https://www.geeksforgeeks.org/type-casting-in-python/](https://www.geeksforgeeks.org/type-casting-in-python/)
- [https://www.geeksforgeeks.org/conditional-statements-in-python/](https://www.geeksforgeeks.org/conditional-statements-in-python/)

