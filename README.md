# T01.6-Ejercicios simples sobre listas y tuplas

## Bloque 1 - Listas y tuplas 

1. En un módulo `funciones_ui.py` implementa una función `solicitar_datos_persona` que solicite por consola a un usuario su nombre, su peso y su estatura, y devuelva una tupla formada por un entero y dos reales con estos tres valores. Un ejemplo de uso sería el siguiente:
    ```python
    >>> Introduzca su nombre: Jane
    >>> Introduzca su peso (en kg): 75
    >>> Introduzca su estatura(en metros): 1.90
    ```
    En este caso, la función debe devolver la tupla `('Jane', 75.0, 1.90)`.
    Pruebe la función en un módulo `test_funciones_ui.py`.
2. En el módulo `funciones_ui.py` implementa una función `solicitar_datos_personas` que, dado un número n. solicite por consola los datos de n personas y devuelva una lista de tuplas con los datos de las n personas. Si el parámetro n toma el valor 3, un ejemplo de uso sería el siguiente:
    ```python
    Introduzca los datos de la persona  1
    Introduzca su nombre: Jane
    Introduzca su peso (en kg): 60.0
    Introduzca su estatura (en m): 1.55
    Introduzca los datos de la persona  2
    Introduzca su nombre: John
    Introduzca su peso (en kg): 90
    Introduzca su estatura (en m): 1.75
    Introduzca los datos de la persona  3
    Introduzca su nombre: Mary
    Introduzca su peso (en kg): 67
    Introduzca su estatura (en m): 1.79
    ```
      En este caso, la función debe devolver la lista: `[('Jane', 60.0, 1.55), ('John', 90.0, 1.75), ('Mary', 67.0, 1.79)]`.
      Pruebe la función en el módulo `test_funciones_ui.py`.

3. En un módulo `funciones_personas.py` implementa una función `estatura_media` que, dada una lista de tuplas con datos de personas, devuelva la estatura media de las personas de la lista. Si la media no se puede calcular, devuelve `None`.
Pruebe la función en un módulo `test_funciones_personas.py`. Haz dos pruebas distintas: (1) Usa la función `solicitar_datos_personas` para generar una lista de tuplas y úsala como entrada a la función, (2) Crea listas de tuplas de forma manual y prueba la función con estas listas de tuplas.
    ```python
    >>> estatura_media ([('Jane', 60.0, 1.55), ('John', 90.0, 1.75), ('Mary', 67.0, 1.79)])
    1.6974999999999998
    >>> estatura_media ([("Jane", 60, 1.50), ("John", 70, 1.69), ("Mary", 65, 1.70), ("Paul", 80, 1.90)  ]
    1.6966666666666665
    >>>estatura_media([('Ana', 50.0, 1.60)])
    1.6
    >>>estatura_media([])
    None
   ```  
4. En el módulo `funciones_personas.py` implementa una función `existe_persona_con_problemas_peso` que, dada una lista de tuplas con datos de personas, devuelva cierto si hay alguna persona en la lista con problemas de peso. Una persona tiene problemas de peso si su estado nutricional es "Bajo peso" u "Obesidad". Reutilice la función `estado_nutricional` implementada en ejercicios anteriores.

   ```python
    >>> existe_persona_con_problemas_peso ([('Jane', 60.0, 1.55), ('John', 100.0, 1.70), ('Mary', 67.0, 1.79)])
    True
    >>> existe_persona_con_problemas_peso ([('Jane', 60.0, 1.55), ('John', 70.0, 1.79), ('Mary', 50.0, 1.80)])
    True
    >>> existe_persona_con_problemas_peso ([('Jane', 60.0, 1.55), ('John', 70.0, 1.79), ('Mary', 67.0, 1.79)])
    False
   ```  
5. En el módulo `funciones_personas.py` implementa una función `contar_superan_estatura_media` que, dada una lista de tuplas con datos de personas, devuelva el número de personas de la lista que superan la estatura media. Reutilice la función `estatura_media` implementada en ejercicios anteriores.
    ```python
    >>>contar_superan_estatura_media ([('Jane', 60.0, 1.55), ('John', 90.0, 1.75), ('Mary', 67.0, 1.79)])
    2
    >>>contar_superan_estatura_media ([("Jane", 60, 1.50), ("John", 70, 1.69), ("Mary", 65, 1.70), ("Paul", 80, 1.90)  ]
    2
    >>>contar_superan_estatura_media([('Ana', 50.0, 1.60)])
    0
    >>>contar_superan_estatura_media([])
    0
   ```  
     
6. En el módulo `funciones_personas.py` implementa una función `todos_superan_estatura` que, dada una lista de tuplas con datos de personas, y un número real que representa una estatura, devuelva cierto si todas las personas de la lista tienen una estatura superior o igual a la dada como parámetro.
    ```python
    >>>todos_superan_estatura ([('Jane', 60.0, 1.55), ('John', 90.0, 1.75), ('Mary', 67.0, 1.79)], 1.70)
    False
    >>>todos_superan_estatura ([('Jane', 60.0, 1.55), ('John', 90.0, 1.75), ('Mary', 67.0, 1.79)], 1.50)
    True
    >>>todos_superan_estatura([], 1.70)
    True
   ```  

## Bloque 2 - Lectura de ficheros

1. En el módulo `funciones_personas.py`implementa una función, que dada la ruta a un archivo con información de personas (su nombre, su estatura y su peso), devuelva una lista de tuplas con los datos leídos de las personas.

2. En el módulo `funciones_personas.py` implementa una segunda versión de la función anterior usando `csv.reader`.

## Bloque 3 - namedtuple

1. Modifica el código de las funciones de los bloques 1 y 2 para usar la siguiente `namedtuple` (que debe añadir al módulo `funciones_personas.py`).

```python
Persona = namedtuple ("Persona", "nombre, peso, estatura")
```
