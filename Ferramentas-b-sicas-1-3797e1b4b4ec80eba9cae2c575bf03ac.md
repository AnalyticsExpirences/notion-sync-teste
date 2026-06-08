
## Anotações importantes:


---

<details>
<summary>Em python, a contagem começa em ZERO (0)‼️</summary>

```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(fruits[0])
print(fruits[1])
print(fruits[2])
```


```python
#Resultado:
apple
banana
cherry
```


</details>

<details>
<summary>No teclado</summary>

ctrl+enter Para rodar o código no VSCode


</details>

<details>
<summary>Diferença entre lista e tupla</summary>

L**istas** e **tuplas** são estruturas para armazenar coleções de valores.


📌 Lista (`list`)

- Pode ser alterada depois de criada
- Permite **adição, remoção e modificação** de elementos
- Usa colchetes `[]`
- Mais flexível, porém  mais pesada em memória

```python
lista = [1, 2, 3, 4]
lista[0] = 10
lista.append(5)
print(lista)

#Resposta
#[10, 2, 3, 4, 5]
```


📌 Tupla (`tuple`)

- Não pode ser alterada após criada
- Não permite adicionar, remover ou modificar elementos
- Usa parênteses `()`
- Mais eficiente em **memória** e **performance**

```python
tupla = (1,2,3,4)
tupla[0] = 10  # ❌ Erro
```


**Quando usar:**

- Dados que **não devem mudar**
- Representar registros fixos (ex: coordenadas, RGB, datas)
- Como **chave de dicionários** (listas não podem)

</details>


---


## type() e random()

    - type() para ver qual o tipo da variável
    - Use a  biblioteca random para criar uma variavel ( outras coisas também) aleatória

        ```python
        import random
        print(random.randrange(1,10))
        ```

    - a estrutura do tipo de variavel para setar o tipo de variavel que você precisa que ela seja, por exemplo:

        ```python
        #Preciso que x seja do tipo inteiro
        x = int(1)
        ```


## Conversão de tipos


    ```python
    z = str(3.0) # z will be '3.0'
    y = int(2.8) # y will be 2
    z = float("3") # z will be 3.0
    ```


## Strings


    ### Essencial


        Para criar strings simples, já sabemos que é só usar 


        ```python
        a = "Hello"
        print(a)
        ```


        Mas se for preciso criar uma string com varias frases por exemplo, é só separar elas por virgula e usar e aspas simples ‘’’


        ```python
        a = '''Lorem ipsum dolor sit amet,
        consectetur adipiscing elit,
        sed do eiusmod tempor incididunt
        ut labore et dolore magna aliqua.'''
        print(a)
        ```


        É possivel checar o tamanho da string usando len( ) de lenght:


        ```python
        a = "Hello, World!"
        print(len(a))
        
        # 13
        ```


        E também checar se uma sstring especifica está dentro de outra por meio de uma função simples:


        ```python
        txt = "The best things in life are free!"
        if "free" in txt:
          print("Yes, 'free' is present.")
        ```


        Como já visto no vscode, pára acessar um caracter usamos [ ] e a posição dele:


        ```python
        a = "Hello, World!"
        print(a[1])
        
        #Respostas: e
        ```


        Podemos imprimir um peçado da string com base na posição de cada elemento


        ```python
        #  A CONTAGEM SEMPRE COMEÇA EM ZERO!!!!!
        b = "Hello, World!"
        print(b[2:5])
        > llo
        
        b = "Hello, World!"
        print(b[:5])  #significa de 0 à 5
        > Hello
        
        b = "Hello, World!"
        print(b[2:]) #significa da posição 2 a última posição
        > llo, World!
        ```


        Se for usado posições “negativas” indica que estamos contando do final para frente:


        ```python
        b = "Hello, World!"
        print(b[-5:-2])
        
        #Contando de trás pra frente, contamos
        ```


        Podemos deixar uma string inteira no maiusculo ou minúsculo:


        ```python
        # MAISCULO
        a = "Hello, World!"
        print(a.upper())
        > HELLO, WORLD
        
        # minusculo
        a = "Hello, World!"
        print(a.lower())
        > hello, world
        ```


        E também tirar os espaços do começo ou do fim (ou ambos) entre as strings


        ```python
        a = " Hello, World! "
        print(a.strip()) # returns "Hello, World!"
        ```


        Remover uma string específica 


        ```python
        a = "Hello, World!"
        print(a.replace("H", "J"))
        # Jello, World!
        ```


        E até separa uma string de acordo com o jeito que vc queira


        ```python
        a = "Hello, World!"
        print(a.split(",")) 
        # ['Hello', ' World!']
        ```


    ### Resumo de funções para string


        **⇒ Todas essas funções retornam novos valores e substituem o original)**


        | Method                                                                         | Description                                                                              | Method       | Description                                                                                   |
        | ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- | ------------ | --------------------------------------------------------------------------------------------- |
        | [capitalize()](https://www.w3schools.com/python/ref_string_capitalize.asp)     | Converts the first character to upper case                                               | join()       | Converts the elements of an iterable into a string                                            |
        | [casefold()](https://www.w3schools.com/python/ref_string_casefold.asp)         | Converts string into lower case                                                          | ljust()      | Returns a left justified version of the string                                                |
        | [center()](https://www.w3schools.com/python/ref_string_center.asp)             | Returns a centered string                                                                | lower()      | Converts a string into lower case                                                             |
        | [count()](https://www.w3schools.com/python/ref_string_count.asp)               | Returns the number of times a specified value occurs in a string                         | lstrip()     | Returns a left trim version of the string                                                     |
        | [encode()](https://www.w3schools.com/python/ref_string_encode.asp)             | Returns an encoded version of the string                                                 | maketrans()  | Returns a translation table to be used in translations                                        |
        | [endswith()](https://www.w3schools.com/python/ref_string_endswith.asp)         | Returns true if the string ends with the specified value                                 | partition()  | Returns a tuple where the string is parted into three parts                                   |
        | [expandtabs()](https://www.w3schools.com/python/ref_string_expandtabs.asp)     | Sets the tab size of the string                                                          | replace()    | Returns a string where a specified value is replaced with a specified value                   |
        | [find()](https://www.w3schools.com/python/ref_string_find.asp)                 | Searches the string for a specified value and returns the position of where it was found | rfind()      | Searches the string for a specified value and returns the last position of where it was found |
        | [format()](https://www.w3schools.com/python/ref_string_format.asp)             | Formats specified values in a string                                                     | rindex()     | Searches the string for a specified value and returns the last position of where it was found |
        | [format_map()](https://www.w3schools.com/python/ref_string_format_map.asp)     | Formats specified values from a dictionary in a string                                   | rjust()      | Returns a right justified version of the string                                               |
        | [index()](https://www.w3schools.com/python/ref_string_index.asp)               | Searches the string for a specified value and returns the position of where it was found | rpartition() | Returns a tuple where the string is parted into three parts                                   |
        | [isalnum()](https://www.w3schools.com/python/ref_string_isalnum.asp)           | Returns True if all characters in the string are alphanumeric                            | rsplit()     | Splits the string at the specified separator, and returns a list                              |
        | [isalpha()](https://www.w3schools.com/python/ref_string_isalpha.asp)           | Returns True if all characters in the string are in the alphabet                         | rstrip()     | Returns a right trim version of the string                                                    |
        | [isascii()](https://www.w3schools.com/python/ref_string_isascii.asp)           | Returns True if all characters in the string are ascii characters                        | split()      | Splits the string at the specified separator, and returns a list                              |
        | [isdecimal()](https://www.w3schools.com/python/ref_string_isdecimal.asp)       | Returns True if all characters in the string are decimals                                | splitlines() | Splits the string at line breaks and returns a list                                           |
        | [isdigit()](https://www.w3schools.com/python/ref_string_isdigit.asp)           | Returns True if all characters in the string are digits                                  | startswith() | Returns true if the string starts with the specified value                                    |
        | [isidentifier()](https://www.w3schools.com/python/ref_string_isidentifier.asp) | Returns True if the string is an identifier                                              | strip()      | Returns a trimmed version of the string                                                       |
        | [islower()](https://www.w3schools.com/python/ref_string_islower.asp)           | Returns True if all characters in the string are lower case                              | swapcase()   | Swaps cases, lower case becomes upper case and vice versa                                     |
        | [isnumeric()](https://www.w3schools.com/python/ref_string_isnumeric.asp)       | Returns True if all characters in the string are numeric                                 | title()      | Converts the first character of each word to upper case                                       |
        | [isprintable()](https://www.w3schools.com/python/ref_string_isprintable.asp)   | Returns True if all characters in the string are printable                               | translate()  | Returns a translated string                                                                   |
        | [isspace()](https://www.w3schools.com/python/ref_string_isspace.asp)           | Returns True if all characters in the string are whitespaces                             | upper()      | Converts a string into upper case                                                             |
        | [istitle()](https://www.w3schools.com/python/ref_string_istitle.asp)           | Returns True if the string follows the rules of a title                                  | zfill()      | Fills the string with a specified number of 0 values at the beginning                         |
        | [isupper()](https://www.w3schools.com/python/ref_string_isupper.asp)           | Returns True if all characters in the string are upper case                              |              |                                                                                               |


![49e3bd37-56ef-4105-9c8e-23d449e77cef.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/76bc0050-b5b4-4172-ac9d-ed17acc6bce2/b510cbe4-ee3c-47b7-83d7-06fb355f154c/49e3bd37-56ef-4105-9c8e-23d449e77cef.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB4663MCPPKYH%2F20260608%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20260608T020837Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEOH%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLXdlc3QtMiJHMEUCIEW8wi2Ew2bu%2F1MReP7S9tAZ%2FSTfEMo4X4DdYzKSK%2BMDAiEAjhACA8%2B%2FC4A6CQe%2F6JZE%2F5e2Z4PN04kZJjgLpYcoaswqiAQIqv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAAGgw2Mzc0MjMxODM4MDUiDG%2F6cggfAD63f47XJircAw7eZsWunogJ9WUsCUg92wQH%2BCjOAQCYeNTXhielQ43WIN56bvOx0En%2FvEt8J0JLIwnrSPGgdu39KM%2BM6loi7Lr8Jr7jXT8Azc2zRd%2BxHFulEiQmCQfuIbUobEpvRfbl6QqycZwZ1AbX4k04l42qrgW7n2LPdPxlz69x9mXJGR98cWjT1eyCs%2FOYNzCi%2Bfar%2BsxwWYHJWcNR7hnW%2FOBq0L47QoDd3PllCqxR%2BPaFj6rGJwAG%2BlKnMN6znwhrQpbTn4ZVijX36SGi3PB6fiQ7hi6PV%2FmcQ9Bu2t%2BIwXA4EDb%2Bi5PnUFGQn2V1gd8gmxhMB7jBDuSJlbgBFWOSuTt8CtcW1z62lXa5zddAahDyg4srQJ6Tt5glMKZTc4ijNDCVuPdVhF6t2%2FF%2BcbV8xzRdql1opCCUXFKMpC%2BxQMZPehXRsIwtt3WR1tfMvnMU76LYnIsyCOEvPN%2FWL2TKkFnzR%2BlqHy9XGMBQeLHYZA3GB0M21OBrnnyNGIpPJNvYfOBLjQAMwgT7UcLSidDX1z52%2FXS%2FDPPBu0PF3rRo5UJeWfRkzLx63MhJkvJlCH4a7wDtwRosFh%2B3qr0FqHdOT6RGtlDChdOyLrDfnmfwSfgrM9zMdzIErgiWkGrr4acLMKikmNEGOqUBFrvDI0Ekkbh5zAOhy9u80SnNK6tG7zeKsk9%2Be8ASZ0FLA3hbgM5NTX%2FK7rsRujIXzJNkDAIjwg96zaj7glWk3CPigczl0OLbsxgndWafacbA4ihL%2BiCg470iVXUP7KiHTrLtyoiDMFwG9Pqi4N05V3cmoZ3tHLAtvJfGLj%2FO4NlYnpT5lOpQ19og1m9cCR0LHssiG9Wk0p8EHamVWi9SzoW2Dz90&X-Amz-Signature=9d6c73fb9e619a0d3eecc62185c417d5d893e28aa4a138b8386df895ae897782&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)


[bookmark](https://www.w3schools.com/python/python_ref_string.asp)

