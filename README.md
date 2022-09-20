# Gramática dependientes del contexto usando Earley Parser

_Compilar el archivo **main.cpp**_

```
g++ main.cpp -o main
```

### Ejecución: ###

**Parámetros validos:**
```
./main nombre_archivo_gramatica.txt "Entrada_a_evaluar" nombre_archivo_salida.txt
```
- Argumento 1: Como mínimo, es necesario ingresar el archivo .txt donde este la gramatica alojada.

- Argumento 2: De no especificar la entrada, el programa te pedira ingresarlo por consola.

- Argumento 3: Nombre del archivo de salida que será generado, de no especificar, el archivo de salida será "salida.txt".

**Formato del archivo de la gramática:**
- Es un archivo de texto plano .txt.
- La primera línea tiene el número de producciones.
- La segunda línea tiene una de las producciones axioma.
- Forma de las producciones
  - Dentro de una produccion no puede haber espacios. 
  - Se escribe el contexto entre corchetes "[ ]".
  - En caso de tener el contexto más de un atributo, separarlos por comas ",".
- Ejemplo de produccion no terminal.
  
```
S ::= NP[NUM=?n] VP[NUM=?n]

VP[TENSE=?t,NUM=?n] ::= IV[TENSE=?t,NUM=?n]
```
- Ejemplo de produccion terminal.
  
```
TV[TENSE=past] ::= saw||liked

Det ::= the||some||several
```

