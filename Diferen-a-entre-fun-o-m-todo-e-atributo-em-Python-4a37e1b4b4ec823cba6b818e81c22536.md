
# 🔹 1️⃣ Por que `x.append()` funciona?


Porque `append()` é um **método do tipo list**.


Exemplo:


```python
x = [1, 2, 3]
x.append(4)
```


Aqui:

- `x` é um objeto do tipo `list`
- `append()` é um **método definido dentro da classe list**
- O método modifica o próprio objeto

Em Python, quando você escreve:


```python
x.metodo()
```


Você está chamando um **método que pertence ao tipo daquele objeto**.


---


# 🔹 2️⃣ Por que `x.type()` não funciona?


Porque `type` **não é um método do objeto**.


Ele é uma **função global da linguagem**.


Ou seja:


```python
type(x)
```


✔️ Correto


```python
x.type()
```


❌ Errado


---


# 🔹 3️⃣ Diferença fundamental


Existem 3 coisas diferentes em Python:


## 🟢 1) Funções globais


São funções que existem independentemente do objeto.


Exemplos:


```python
type(x)
len(x)
print(x)
sum(x)
```


Elas recebem o objeto como argumento.


---


## 🔵 2) Métodos


São funções que pertencem ao tipo do objeto.


Exemplos para listas:


```python
x.append()
x.pop()
x.sort()
x.remove()
```


Esses métodos fazem parte da classe `list`.


---


## 🟣 3) Atributos (não são funções)


São informações do objeto, sem parênteses.


Exemplo:


```python
x = 3 + 4j
x.real
```


Aqui `real` não é função — é um atributo.


---


# 🔹 4️⃣ Como saber se algo é método ou função?


Use:


```python
dir(x)
```


Isso mostra tudo que o objeto possui.


E para saber o tipo:


```python
type(x)
```


---


# 🔹 5️⃣ Regra prática


Pergunta mental que resolve 90% dos casos:

> Isso é algo que o objeto FAZ ou algo que eu quero SABER sobre ele?

Se for algo que o objeto faz → provavelmente é método


Se for algo geral da linguagem → provavelmente é função global


---


# 🔹 6️⃣ Comparação prática


### Lista


```python
x = [1,2,3]

len(x)        # função global
x.append(4)   # método da lista
type(x)       # função global
```


---


# 🔹 7️⃣ Por que Python foi feito assim?


Porque:

- Métodos são comportamentos específicos daquele tipo
- Funções globais são operações gerais da linguagem

Exemplo:


`len()` funciona para:

- lista
- string
- tupla
- dicionário

Por isso é função global.


Já `append()` só faz sentido para listas.


---


# 🎯 Resumo final


| Forma        | O que é              | Exemplo      |
| ------------ | -------------------- | ------------ |
| `x.metodo()` | Método do objeto     | `x.append()` |
| `funcao(x)`  | Função global        | `type(x)`    |
| `x.atributo` | Informação do objeto | `x.real`     |

