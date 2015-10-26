# Introdução a Python 2.7

## Saída padrão
```python
print 'Ola, mundo!'
```

## Entrada padrão (strings)
```python
nome = raw_input()
print 'Ola, ' + nome + '!'
```

```python
nome = raw_input()
print 'Ola, %s!' % nome
```

## Comentário
```python
# Esta linha começa com cerquilha e é um comentário
```

## Principais tipos de dados
```python
# Booleano (boolean)
True
False

12    # Inteiro normal (int)
12L   # Inteiro longo (long)
3.14  # Ponto flutuante (float)

# Texto ASCII (string)
'Um texto usando aspas simples'
"Um texto usando aspas duplas"

# Lista (list)
[]
[1, 2, 3]
['um', 'dois', 'tres']
[1, 'dois', 3.0]
[[0, 0], [0, 1], [1, 0], [1, 1]]

# Tupla (tuple)
()
(1, 2, 3)
(0, 'Zero')

# Dicionário (dict)
{
  'monte': 'Elevacao de terreno',
  'piton': 'Serprente da Asia e da Africa, nao venenosa'
}

{
  'manga': 4,
  'laranja': 12,
  'banana': 15
}

{12: 'doze', 34: 'trinta e quatro'}
```

## Variáveis
Não precisam ser declaradas; basta fazer ```nome_var = valor```
```python
a = 1
b = 2
```

Variáveis não tem tipo. Podem receber valores de qualquer tipo.
```python
x = 1
y = 'dois'
z = [3, 4]
z = 5.0  # atribuindo a z novamente. lista anterior é perdida.
```

## Strings e listas
```python
s = [0, 10, 20, 30]

# Tamanho
len(s)  # 4

# Indexação na ordem direta
s[0]    # 0
s[1]    # 10
s[2]    # 20
s[3]    # 30

# Indexação na ordem inversa
s[-1]   # 30
s[-2]   # 20
s[-3]   # 10
s[-4]   # 0

# Sublista
s[1:3]  # [10, 20]
s[1:3] = [15, 25]   # Altera a lista para [0, 15, 25, 30]

# Cópia da lista
copia = s[:]
```

## Igualdade
```python
# Vendo se o conteúdo é igual
s == s      # True
s == copia  # True

# Vendo se o objeto é o mesmo (ou seja, vendo se estão na mesma posição de memória)
s is s      # True
copia is s  # False
```

## Condicional
```python
a = 2
if a == 2: print 'a vale 2'
```
```python
if resposta == 'sim' and esta_funcionando: print 'ok'
```
```python
if resposta == 'nao' or not esta_funcionando: print 'erro'
```

## Blocos
Python usa endentação significativa. A endentação determina a existência de um bloco. Não existe abre-chaves/fecha-chaves nem begin-end.

```python
print 'Deseja continuar?'

continuar = raw_input()

if continuar == 'sim':
  print 'Continuando'
  print '...'
elif continuar == 'nao'
  print 'Encerrando'
else
  print 'Erro. Favor digitar sim ou nao'.
```

## Laços
```python
for i in range(10): print i   # numeros de 0 a 9
```

```python
for i in range(10):
  print 'Estamos no %d. Deseja continuar?' % i
  continuar = raw_input()
  if (continuar == 'nao'): break
```

```python
i = 0
continuar = raw_input()
while continuar != 'nao':
  print i
  i += 1
  continuar = raw_input()
```

## Funções
```python
def dizer_ola(nome):
  print 'Ola, %s!' % nome

dizer_ola('Jorge')
dizer_ola('Zelia')
```

```python
import math

def raiz_quadrada_da_soma_dos_quadrados_dos_catetos(um_cateto, outro_cateto):
  return math.sqrt(um_cateto ** 2 + outro_cateto ** 2)

def area_do_circulo(raio):
  return math.pi * raio ** 2
```

## Classes
```python
class ClasseSemAtributos:
    def __init__(self):
        print 'Construtor foi chamado'

    def metodo_1_sem_retorno(self):
        print 'Metodo 1 foi chamado'

    def metodo_2_com_retorno(self):
        print 'Metodo 2 foi chamado'
        return 200

obj1 = ClasseSemAtributos()
obj2 = ClasseSemAtributos()
```

```python
class Pessoa:
    def __init__(self, nome, idade):
        self._nome = nome
        self._idade = idade

    def maior_de_idade(self):
        return self._idade >= 18

    def nome(self):
        return self._nome

ulisses = Pessoa('Ulisses', 39)
iara = Pessoa('Iara', 42)
```

## Mais
- Operadores: http://www.learnpython.org/en/Basic_Operators
- Funções map, reduce, filter: https://pythonhelp.wordpress.com/2012/05/13/map-reduce-filter-e-lambda/