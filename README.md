# Input-Output


## Funcion para registrar solo datos de tipo float : 

      def registrar_numeros(texto_ingresado: str)  -> float:
      control = True

      while True:
          num = input(texto_ingresado)

          try:
              num_val = float(num)
              control = True
          except ValueError:
              pass

      return num_val
      
      
  ---------------
 Explicaremos: 
 
       def registrar_numeros(texto_ingresado: str)  -> float:
 
 Esta línea de código define una función llamada "registrar_numeros" que toma un argumento llamado "texto_ingresado" de tipo "str" y devuelve un valor de tipo "float". Aquí está la explicación detallada:

- `(texto_ingresado: str)` es la declaración de parámetro de la función. Indica que la función espera un argumento llamado "texto_ingresado" de tipo "str", es decir, una cadena de caracteres.
- `-> float` es una notación de tipo de retorno de la función. Indica que la función devuelve un valor de tipo "float", es decir, un número de punto flotante.

En resumen, esta línea de código define una función llamada "registrar_solo_numeros" que espera recibir una cadena de caracteres como argumento y devuelve un número de punto flotante.

-----------------
El problema de ingresar nota por nota en un programa de python es que puede que aveces me demore en hacer esto, incluso es importante considerar esto si ingreso secuencialmente y rapido todas las notas, igualmente habra un tiempo adicional, por mas minimo que sea. Por ello, es recomendable recurrir al uso de archivos que contengan estos datos, ya que las operaciones de entrada, como ya se mencionó, pueden requerir un tiempo adicional.

Cabe resaltar que la mayoria de archivos puede abrirse como archivo de texto, la extencion es solo para especeficar su funcion del archivo o sera usado mayormente. Por ejemplo, si abrimos una imagen como archivo de texto veremos todo el codigo de cada pixel.

En este caso se trabajara con archivos de tipo:

## CSV:
C = Comma

S = Separated

V = Values

--------------

       with open("readme.md", "r") as f:
            contenido = f.read()
      

El archivo debe estar en el mismo directorio del programa, el "r" indica que el archivo sera solo de lectura

"as f" indica que usaremos el f como puntero para poder trabajar con el archivo

"contenido = f.read()"   leera lo que hay en el archivo 

----

Imprimir tipo de dato:

      print(type(contenido))
      
 --------
 Formas de imprimir:
 
    print(contenido)
    print(contenido[0])
    print(contenido[0:3])
    print(contenido[:3])
    print(contenido[-3:])
    
    
 ----------
 Separador: 
 
 
          contenido = "Esta es la primera linea\nesta es la segunda linea"
          lineas = contenido.split("\n")
          
          print(lineas[0].upper())
          print(lineas[1])
    


