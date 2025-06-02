---
theme: default
lineNumbers: true
layout: intro
title: Funções
author: José Roberto Bezerra
---

# Funções

Introdução a Programação

---
layout: section
---

# Funções

---
layout: quote
---

> As linguagens de programação modernas dispõe da capacidade de agrupar um conjunto de comandos em único nome. Dessa forma, sempre que esse nome for invocado todos os comandos associados a ele são executados.

---
layout: quote
---

> Para criar uma função e agrupar código, utiliza-se `def`. Desta forma um *bloco de código* é criado. Funções podem receber parâmetros (dados) e normalmente retornam um resultado.

---
layout: default
---

# Exemplo 1

```python{1-2|4}{class:'!children:text-2xl'}
def my_function():
  print("Hello World!!!")

my_function()
```

---
layout: two-cols-header
---

# Argumentos

:: left ::
- Informações podem ser passadas às funções como **argumentos**
- Argumentos são especificados nos parênteses e separados por vírgula
- A ordem é fundamental

:: right ::
```python{*}{class:'!children:text-xl'}
def add_user(login):
  print('Usuário', login, 'adicionado')

add_user('roberto')
```

---
layout: default
---

# Exemplo 2

```python{1-2|4}{class:'!children:text-2xl'}
def my_function(nome, snome):
    print('Nome: ', nome, '\nSobrenome: ', snome)

var1 = input('Qual seu nome?')
var2 = input('Qual seu sobrenome?')
my_function(var1, var2)
```

---
layout: quote
---

# Argumentos Arbitrários (`*args`)

> Quando a quantidade de argumentos é indeterminada utiliza-se um `*` antes do nome do argumento para indicar que uma **tupla** será recebida. A quantidade de argumentos é o mais importante

---
layout: default
---

# Exemplo 3

```python{*}{class:'!children:text-xl'}
def my_band(*integrantes):
  print('Último argumento:' + integrantes[-1])
  print('Quantidade: ' + str(len(integrantes)))

my_band('Cazuza', 'Frejat', 'Rodrigo')
my_band('Angus', 'Julia')
```

---
layout: default
---

# Exemplo 4

```python{*}{class:'!children:text-2xl'}
def fun(*nums):
    return sum(nums)

print(fun(1, 2, 3, 4)) 
print(fun(5, 10, 15))
```

---
layout: quote
---

# Argumentos com Palavra Chave (`**kwarg`)

> Também é possível utilizar argumentos com pares chave/valor. Nesse caso, a ordem não importa.

---
layout: default
---

# Exemplo 5

```python{*}{class:'!children:text-2xl'}
def fun(**kwargs):
    for key, value in kwargs.items():
        print(key, value)

fun(a=1, b=2, c=3)
```

---
layout: default
---

# Exemplo 6

```python{*}{class:'!children:text-2xl'}
def my_band(**integrantes):
  for funcao, nome in integrantes.items():
    print(funcao, ':', nome)
  
print('Barão Vermelho')
my_band(lider='Cazuza', baixo='Frejat', bateria='Guto' )
print('\nAngus and Julia Stone')
my_band(guitarra='Angus', vocal='Julia')
```

---
layout: default
---

# Exemplo 7

```python{*}{class:'!children:text-2xl'}
def my_band(band, **integrantes):
    print('Banda: ' + band.upper())
    for funcao, nome in integrantes.items():
        print(funcao, ':', nome)
    print('\n')

my_band('barão vermelho', lider='Cazuza', baixo='Frejat', bateria='Guto')
my_band('angus and julia stone', guitarra='Angus', vocal='Julia')
```

---
layout: quote
---

> É possível especificar um valor padrão (*default*) para um argumento. Caso a função seja chamada sem argumentos, o valor padrão será atribuído.

---
layout: default
---

# Valor padrão (*default value*)

```python
def my_function(country = "Brasil"):
  print("Meu país é: " + country)

my_function("Suécia")
my_function("Índia")
my_function()
my_function("EUA")
```

---
layout: quote
---

# Retornando valores

> O uso mais frequente das funções é fazendo com que elas **retornem** valores. Nos exemplos anteriores as funções apenas executam comandos, mas não retornam nenhum valor. Para que seja retornado um valor basta utilizar `return`

---
layout: two-cols-header
---

:: left ::
```python{*}{'class: !children:text-2xl'}
def my_function(x):
  return 5 * x

print(my_function(3))
var1 = my_function(5)
var2 = my_function(9)
```

::right::
```python{*}{'class: !children:text-2xl'}
def my_function(x, y):
  return x + y

print(my_function(3, 1))
var1 = my_function(5, 5)
var2 = my_function(9, 10)
```

---
layout: fact
---

# Exercício Resolvido 1

Escrever um *script* em Python que realize o cálculo da área de dois retângulos com a base e altura informados pelo usuário. Utilize o valor padrão 1 para cada uma das dimensões. Depois de calculadas as áreas, o *script* deve somar as duas áreas e exibir o resultado ao usuário.


---
layout: fact
---

# Exercício 1

Criar um *script* em Pyhton para calcular a área de uma edificação (casa, apartamento, prédio, etc). O usuário deve entrar com a largura, profundidade e o nome de ambiente. O *script* deve calcular a área de cada ambiente e exibir a área total, que corresponde a soma de todas as áreas individuais. 

<!-- # Exercício 2

Criar a função `create_user(login, passwd)` em Python que realiza o cadastro de um usuário em um sistema. A função deve receber o login do usuário e verificar se ele já existe e  deve verificar se as duas senhas (`passwd`) digitadas são idênticas. -->
 

---
layout: default
---

# Referências
- [W3 Schools](https://www.w3schools.com/python/python_functions.asp)
- [Geeks for Geeks](https://www.geeksforgeeks.org/args-kwargs-python/)