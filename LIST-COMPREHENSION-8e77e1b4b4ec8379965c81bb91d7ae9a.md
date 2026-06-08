
## 📌 Estrutura Básica


### 🔹 Sem condição:


```python
[expressão_retornada for item in lista]
```


### 🔹 Com if:


```python
[expressão_retornada for item in lista if condição]
```


    ### 🔹 Com if/else:


```python
[valor1 if condição else valor2 for item in lista]
```


> ⚠️ Os `if/else` sempre vem **antes** do `for`   
> 🏷️Evite usar quando ficar confuso ou muito complexo.


## 📌 Comparação com FOR tradicional


    ### **Exemplo 1:** filtrar números pares


        ---


🔹 **For normal:**


```python
pares = []
for n in numeros:
    if n % 2 == 0:
        pares.append(n)
```


**🔹 List comprehension:**


```python
pares = [n for n in numeros if n % 2 == 0]
```


    ### Exemplo 2: usando IF e ELSE


        ---


**🔹 For normal:**


```python
resultado = []

for n in num:
    if n % 2 == 0:
        resultado.append("par")
    else:
        resultado.append("ímpar")
```


        **🔹 List comprehension:**


```python
resultado = ["par" if n % 2 == 0 else "ímpar" for n in num]
```


    ### Exemplo 3:


        ---


```python
[x if cond1 else y if cond2 else z for item in lista]
```


        > **LEIA ASSIM:** 👉🏻 “Retorne **x** se **cond1** for válida, retorne **y** se **cond2** for válida, retorne **z** caso nenhuma das condições forem válidas, para cada "item" em "lista".

