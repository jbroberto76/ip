---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: /layered-steps-right.svg
title: Funções
description: Introdução a Programação
exportFilename: ip_aula10_python_functions
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
{{ $slidev.configs.description }}

---

# Objetivos de Aprendizagen
- Construir funções personalizadas
- Utilizar módulos

---

# Agenda
- Funções personalizadas
- Módulos

---
layout: section
---

# Conceito

---
layout: quote
---

> Uma função é um bloco de código que é executada quando é chamada. Dados (**parâmetros**) podem ser passados para função. Uma função pode ainda **retornar** um resultado.

---

# Criando funções
`def`

- Para declarar uma função utiliza-se `def` e indentação
- `def` também é uma palavra reservada

```python{*}{class:'!children:text-2xl'}
def my_function():
    print("Hello...")
```

---

# Chamando funções

- Funções apenas podem ser utilizadas após sua declaração

```python{*}{class:'!children:text-2xl'}
def my_function():
    print("Hello...")

my_function()
```

---

# Argumentos
ou Parâmetros

- Informação é passada às funções através de argumentos ou parâmetros
- Argumentos são sequenciais, ou seja, a ordem importa

```python {*}{class:'!children:text-2xl'}
def my_function(name, fname):
    print("Hello, ", name.upper(), fname.upper())

my_function('john', 'lennon')
```

---

# Argumentos Não Nomeados
`*args`

- Quando a quantidade de argumentos é indefinida adiciona-se `*` antes do parâmetro

```python{*}{class:'!children:text-2xl'}
def my_args(*nums):
    for n in nums:
        print(n)

my_args(1, 2, 4, 6, 8, 10)
```

---

# Retornando valores
`return`

- Funções podem devolver valores, resultados das operações

```python{all|5}{class:'!children:text-2xl'}
def add(*nums):
    sum = 0
    for n in nums:
        sum += n
    return sum

print(f"Soma vale: {add(7,6,3)}")
```

---

# Retornando valores
`return`

```python{*}{class:'!children:text-2xl'}
def area_ret(base, altura):
    return base * altura

print("/|\ Área do Retângulo /|\ ")
b = int(input("Entre com a base do retângulo:"))
h = int(input("Entre com a altura do retângulo:"))
print(f"A área do retângulo vale {area_ret(b, h)}")
```

---

# Argumentos por palavra chave
`**kwargs`

- Argumentos são passados através de pares `nome=valor`

```python{*}{class:'!children:text-2xl'}
def show_values(**kwargs):
    print(f'Valores recebidos: {kwargs}')

    for valor in kwargs.values():
        print(f'{valor}')

show_values(var1=10, var2=20)
```

---

# Argumentos por palavra chave
`**kwargs`

```python{*}{class:'!children:text-2xl'}
def show_values(**kwargs):
    print(f'Nomes recebidos (keys): {kwargs}')

    for k in kwargs.keys():
        print(f'{k}')
        
show_values(var1=10, var2=20)
```

---

# Argumentos por palavra chave
`**kwargs`

```python{*}{class:'!children:text-2xl'}
def show_user_info(**data):
    for chave, valor in data.items():
        print(f"{chave.capitalize()}: {valor}")

show_user_info(user='jlennon@gmail.com', age=21, city='London')
```

---

# Valor padrão

```python{*}{class:'!children:text-2xl'}
def show_user_info(country='Brazil', **data):
    print("Origem: ", country)
    for chave, valor in data.items():
        print(f"{chave.capitalize()}: {valor}")

show_user_info(user='jlennon@gmail.com', age=21, city='London')
show_user_info(country='UK', user='jlennon@gmail.com', age=21, city='London')
```

---

# Valor padrão

```python{*}{class:'!children:text-2xl'}
def calcular_preco(preco, desconto=0):
    apagar = preco - (preco * desconto)
    return apagar

print(calcular_preco(100))
print(calcular_preco(100, 0.1))
```

---
layout: section
---

# Módulos

---

# Módulos

> Permitem agrupar código para ser utilizado como uma biblioteca de funções, variáveis e dados em geral. Existem módulos do usuário e aqueles disponibilizados pela linguagem ou por terceiros.

---

# Módulos do usuário

1. Crie um arquivo com a extensão `.py` com as definições de função abaixo
2. Faça o *upload* do arquivo na pasta do Google Colabs com o nome `geocalc.py`

```python{*}{class:'!children:text-2xl'}
import math
def area_ret(base, altura):
    return base * altura

def area_circ(raio):
    return math.pi*raio*raio
```

---

# Módulos do usuário

3. Imagine que o *script* a seguir foi criado para utilizar as funções contidas no módulo `geocalc.py`

```python{*}{class:'!children:text-xl'}
import geocalc
print("/|\ Calculadora de Áreas Online /|\ ")
opc = input("Digite 1 para retângulo ou 2 para círculo:")
if opc == '1':
    b = int(input("Base:"))
    h = int(input("Altura:"))
    print(f"Área do retângulo: {geocalc.area_ret(b, h)}")
else:
    r = int(input("Raio:"))
    print(f"Área do círculo: {geocalc.area_circ(r)}")
```

---

# Módulos do usuário
Como executar no Google Colab

4. Se esse código for executado num ambiente local, ou seja na sua própria máquina, nenhum erro será exibido. Porém, como está sendo executado no ambiente do Google é necessário fazer com que o Colab "enxergue" um arquivo externo
5. Adicione as linhas de código abaixo e em seguida tente rodar novamente

```python{*}{lines: false, class:'!children:text-xl'}
from google.colab import drive
drive.mount('/content/gdrive')
import sys
sys.path.insert(0, '/content/gdrive/MyDrive/Colab Notebooks/IP')
```

---

# Renomeando módulos

```python{1|7,10}{class:'!children:text-xl'}
import geocalc as gc
print("/|\ Calculadora de Áreas Online /|\ ")
opc = input("Digite 1 para retângulo ou 2 para círculo:")
if opc == '1':
    b = int(input("Base:"))
    h = int(input("Altura:"))
    print(f"Área do retângulo: {gc.area_ret(b, h)}")
else:
    r = int(input("Raio:"))
    print(f"Área do círculo: {gc.area_circ(r)}")
```

---

# Importanto partes do módulo
`import from`

```python{*}{class:'!children:text-xl'}
from geocalc import area_circ
print(f"A área de um círculo de raio 2 é {area_circ(2)}")
```

---

# Importanto módulo inteiro
`import *`

```python{*}{class:'!children:text-xl'}
from geocalc import *
print(f"A área de um círculo de raio 2 é {area_circ(2)}")
```

---
layout: fact
---

# Exercícios

---

# 1

Crie uma função em Python que calcula o delta ($\Delta = b^2 - 4ac$) de uma equação do segundo grau ($ax^2+bx+c=0$) a partir dos coeficientes $a$, $b$, e $c$. 

---

# 2

Crie um *script* em Python que utiliza a função criada no exercício anterior para calcular as raízes de uma equação do segundo grau.

---

# Referências
- [Funções e Módulos em Python](https://luizteixeira.dev.br/funcoes-e-modulos-em-python-um-guia-completo/)
- [Python Functions](https://www.w3schools.com/python/python_functions.asp)
- [Python Modules](https://www.w3schools.com/python/python_modules.asp)

---
src: /snippets/end.md
---
