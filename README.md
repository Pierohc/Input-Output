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


