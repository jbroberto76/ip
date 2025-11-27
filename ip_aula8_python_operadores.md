---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: /layered-steps-right.svg
title: Operadores
description: Introdução a Programação
exportFilename: ip_aula8_python_operadores
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
{{ $slidev.configs.description }}

---

# Objetivo de Aprendizagen
- Conhecer operadores de uso geral do Python

---

# Agenda
- Módulos
- `math`
- Operadores
- Formatação de números
- Funções de texto padrão

---
layout: section
---

# Módulos Externos

---
layout: quote
---

> Um módulo Python é um arquivo contendo um conjunto de funções e declarações que pode ser incluído em um *script*. Um módulo pode ser entendido como uma biblioteca de códigos. O Python disponibiliza diversos módulos embutidos e existem ainda módulos de terceiros.

---

# Módulos Típicos
- Existem diversos módulos disponíveis
- Exemplos:
    - `math`
    - `platform`
    - `os`
    - Dentre muitos outros

---

# Como usar um módulo?

- Vamos utilizar como exemplo o módulo `math`
- O primeiro passo é a importação do módulo: `import math`

```python{*}{class:'!children:text-2xl'}
import math
print(math.pi)
```

---

# O que acontece ao executar os códigos?

```python{*}{class:'!children:text-2xl'}
import math
print(math.ceil(1.45))
print(math.floor(1.45))
print(math.factorial(3))
print(math.fabs(-1))
print(math.pow(2,3))
print(math.sqrt(2))
```

---
layout: center
---

# Lista completa do Módulo Math

[Mathematical functions](https://docs.python.org/3/library/math.html)

---

# Outras funções matemáticas

```python{*}{class:'!children:text-2xl'}
# retorna o valor absoluto de um número
abs(-3)
# retorna o valor máximo de uma sequência
max(1, 2, 3)
# retorna o valor mínimo de uma sequência
min(1, 2, 3)
# arredonda um float para o inteiro mais próximo
round(3.14)
# arredonda um float para um determinado número de casas decimais
round(3.14, 1)
# retorna a soma de uma sequência de números
sum([1, 2, 3])
```

---

# Exemplo

```python{*}{class:'!children:text-2xl'}
top = max(5, 10, 25)
print(f"Máximo: {top}\nMínimo: {min(5, 10, 25)}")
```

---
layout: section
---

# Operadores

---

# Operadores Aritméticos

| **Operador** 	| **Nome**        	| **Função**                                                              	|
|--------------	|-----------------	|-------------------------------------------------------------------------	|
| `+`          	| Adição          	| Realiza a soma de ambos operandos.                                      	|
| `-`          	| Subtração       	| Realiza a subtração de ambos operandos.                                 	|
| `*`          	| Multiplicação   	| Realiza a multiplicação de ambos operandos.                             	|
| `/`          	| Divisão         	| Realiza a Divisão de ambos operandos.                                   	|
| `//`         	| Divisão inteira 	| Realiza a divisão entre operandos e a parte decimal de ambos operandos. 	|
| `%`          	| Módulo          	| Retorna o resto da divisão de ambos operandos.                          	|
| `**`         	| Exponenciação   	| Retorna o resultado da elevação da potência pelo outro.                 	|

---

# Operações Aritméticas

```python{*}{class:'!children:text-2xl'}
a = 5
b = 3
c = a + b # soma de dois números
d = a - b # subtração de dois números
e = a * b # multiplicação de dois números
f = a / b # divisão de dois números
g = a // b # divisão inteira de dois números
g = a % b # módulo de dois números
h = a ** b # exponenciação de dois números
```

---

# Operadores de Comparação

| **Operador** 	| **Nome**       	| **Função**                                              	|
|--------------	|----------------	|---------------------------------------------------------	|
|     ==     	|     Igual a    	| Verifica se um valor é igual ao outro                   	|
|     !=     	|  Diferente de  	| Verifica se um valor é diferente ao outro               	|
|      >     	|    Maior que   	| Verifica se um valor é maior que outro                  	|
|     >=     	| Maior ou igual 	| Verifica se um valor é maior ou igual ao outro          	|
|      <     	|    Menor que   	| Verifica se um valor é menor que outro                  	|
|     <=     	| Menor ou igual 	| Verifica se um valor é menor ou igual ao outro          	|
|      **    	| Exponenciação  	| Retorna o resultado da elevação da potência pelo outro. 	|

---

# Operações de Comparação

```python{*}{class:'!children:text-xl'}
var = 5
if var == 5:
    print('Os valores são iguais')
if var != 7:
    print('O valor não é igual a 7')
if var > 2:
    print('O valor da variável é maior de 2')
if var >= 5:
    print('O valor da variável é maior ou igual a 5')
if var < 7:
    print('O valor da variável é menor que 7')
if var <= 5:
    print('O valor da variável é menor ou igual a 5')
```

---

# Operadores de Atribuição

| **Operador** 	| **Nome**   	| **Função** 	|
|--------------	|------------	|------------	|
|      `=`     	| Atribuição 	| x = 1      	|
|     `+=`     	| Incremento 	| x = x + 1  	|
|     `-=`     	| Decremento 	| x = x - 1  	|
|     `*=`     	|            	| x = x * 1  	|
|     `/=`     	|            	| x = x / 1  	|
|     `%=`     	|            	| x = x % 1  	|

---

# Operações de Atribuição

```python{*}{class:'!children:text-xl'}
n = 10
n += 1
print(n)
n += 5
print(n)
n -= 3
print(n)
n *= 2
print(n)
n /= 2
print(n)
n %= 12
print(n)
```

---
layout: section
---

# Formatação

---

# Formatação de Números
Casas decimais

```python{*}{class:'!children:text-2xl'}
import math
pi = math.pi
print(f"Pi: {pi}")
print(f"{pi:.1f}")
print(f"{pi:.3f}")
print(f"{pi:09.5f}")
print("{:.2f}".format(pi))
```

---

# Formatação de Números
Percentuais

```python{*}{class:'!children:text-2xl'}
p = 0.215
print(f"Seu desconto é de {p:.2%}")
```

---

# Formatação de Strings
Maiúsculas e Minúsculas

```python{*}{class:'!children:text-2xl'}
sigla = "mmc"
significado = "mínimo múltiplo comum"
print("{} = {}".format(sigla.upper(),significado.title()))
```
<br><br>
```python{*}{class:'!children:text-2xl'}
cmd1 = "PRINT"
cmd2 = "INPUT"
print("Alguns exemplos de comandos do Python: {} e {}".format(cmd1.lower(),cmd2.lower()))
```

---

# Formatação de Strings
Contagem de ocorrências

```python{*}{class:'!children:text-2xl'}
texto = "I love apples. Apples are my favorite fruits"
x = texto.count("apple")
print(x)
```

---

# Formatação de Strings
Verificação de dígito ou número

```python{*}{class:'!children:text-2xl'}
sn = "50800"
model = "A320"
sigla = "MMC"
x = sn.isdigit()
print(x)
x = model.isdigit()
print(x)
x = model.isalnum()
print(x)
x = sigla.isalpha()
print(x)
```

---

# Validação de Entrada
Exemplo

```python{*}{class:'!children:text-2xl'}
usuario = input("Digite o nome de usuário (apenas letras): ")

if not usuario.isalpha():
    print("Nome de usuário inválido. Use apenas letras (sem números ou símbolos).")
else:
    senha= input("Digite a senha (apenas números): ")
    if not senha.isdigit():
        print("Senha inválida. Use apenas números (sem letras ou símbolos).")
    else:
        print("Usuário e senha válidos!")
```

---

# Comprimento de Strings
`len()`

- A função `len()` retorna o número de itens de um objeto
- Quando o objeto é uma string, retorna a quantidade de caracteres

```python{*}{class:'!children:text-2xl'}
fruits = ["apple", "banana", "cherry"]
x = len(fruits)
```
<br><br>
```python{*}{class:'!children:text-2xl'}
msg = "Hello, world!!!"
x = len(msg)
```

---

# `len()`

- Apenas faz sentido aplicar a função para tipos de dados iteráveis
    - Listas
    - Dicionários
    - Conjuntos
    - Strings
- Para tipos de dados que armazenam apenas um item `len()` apresenta erro

---

# Exemplo

```python{*}{class:'!children:text-xl'}
nome = input("Digite seu nome: ")

print(f"\nNome em maiúsculas: {nome.upper()}")

tamanho = len(nome.strip())
print(f"Seu nome tem {tamanho} letras!")

if tamanho <= 4:
    print("Seu nome é curto!")
elif tamanho <= 6:
    print("Seu nome tem um tamanho médio.")
else:
    print("Seu nome é longo!")
```

---
layout: fact
---

# Exercícios

---

# 1

<!-- > Crie um *script* em Python que informa ao usuário a quantidade de vogais que existe em uma mensagem passada pelo usuário. -->

> Crie um *script* em Python uma Calculadora Geométrica para realizar cálculos de área e perímetro de um círculo ou retângulo, segundo opção do usuário. Caso escolha o círculo o usuário deve informar o raio, mas caso escolha o retângulo deve informar a base e altura do mesmo.

<!-- 
```python
import math

print("=== Calculadora Geométrica ===")
print("Escolha uma figura para calcular:")
print("1 - Círculo")
print("2 - Retângulo")

opcao = input("\nDigite o número da figura (1 ou 2): ")

if opcao == "1":
    # Cálculos para o círculo
    raio = float(input("\nDigite o raio do círculo: "))
    area = math.pi * (raio ** 2)
    perimetro = 2 * math.pi * raio
    print(f"\n- Área do círculo: {round(area, 2)}")
    print(f"- Circunferência: {round(perimetro, 2)}")

elif opcao == "2":
    # Cálculos para o retângulo
    base = float(input("\nDigite a base do retângulo: "))
    altura = float(input("Digite a altura do retângulo: "))
    area = base * altura
    perimetro = 2 * (base + altura)
    print(f"\n- Área do retângulo: {area}")
    print(f"- Perímetro do retângulo: {perimetro}")

else:
    print("\nOpção inválida! Digite 1 ou 2.")
``` 
-->

---

# 2

> Crie um *script* em Python que realiza a criação de usuário para um sistema de banco de dados. Tanto o login quanto a senha possuem regras específicas que devem ser atendidas. O login do usuário deve possuir no mínimo 3 caracteres e no máximo 8, deve conter apenas caracteres do alfabeto e não possuir espaços em branco nem no início, nem no final. Já a senha deve ter pelo menos 6 caracteres e possuir caracteres do alfabeto ou numéricos. Mensagens de sucesso e erro devem ser exibidas ao usuário.

<!-- 
```python
print("=== Cadastro de Usuário ===")

# Solicita dados
login = input("\nDigite seu login: ").strip()
senha = input("Digite sua senha: ").strip()

# Variáveis para armazenar erros
erros = []

# Validação do login
if len(login) < 3 or len(login) > 8:
    erros.append("O login deve ter entre 3 e 8 caracteres.")
if not login.isalpha():
    erros.append("O login deve conter apenas letras (sem números ou símbolos).")
if len(login) != len(login.strip()):
    erros.append("O login não pode ter espaços no início ou final.")

# Validação da senha
if len(senha) < 6:
    erros.append("A senha deve ter pelo menos 6 caracteres.")
if not senha.isalnum():
    erros.append("A senha deve conter apenas letras e números.")

# Exibe resultados
if not erros:
    print("\n=== Cadastro concluído com sucesso! ===")
    print(f"Login: {login}")
    print(f"Senha: {'*' * len(senha)}")
else:
    print("\n=== Erros encontrados ===")
    for erro in erros:
        print(f"✖ {erro}")
```
-->

---

# Referências
- [W3 Schools](https://www.w3schools.com/python/python_modules.asp)
- [Python Math](https://docs.python.org/3/library/math.html)

---
src: /snippets/end.md
---
