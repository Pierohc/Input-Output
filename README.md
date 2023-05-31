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
    
    
    
    
    
    
 -----------------------
 
 
      import numpy as np
      import time

      if __name__ == '__main__':
          inicio_total = time.perf_counter()

          inicio_es = time.perf_counter()
          with open("notas.csv", "r") as f:
              contenido = f.read()
          final_es = time.perf_counter()


          inicio_cpu = time.perf_counter()
          filas = contenido.split("\n") #salto de linea


          for i in range(1,len(filas)-1):

              dt_str = (filas[i].split(","))
              dt_float = np.asarray(dt_str, dtype = float)

              promedio_lab = sum(dt_float[1:15])/14

              nota_final = ((promedio_lab*50) + ((dt_float[15])*25) + ((dt_float[16])*25)) /100

              print(f"La nota final del alumno con codigo {int(dt_float[0])} es: {nota_final}")

          final_cpu = time.perf_counter()
          final_total = time.perf_counter()

          print(f"Tiempo total de ejecucion: {final_total - inicio_total}")
          print(f"Tiempo total de operaciones E/S: {final_es - inicio_es}")
          print(f"Tiempo total de procesamiento : {final_cpu - inicio_cpu}")
          
          
 Otras formas de convertir un arreglo tipo string a float o int: 
 1:
 
      arreglo_str = ["1.5", "2.3", "4.7", "3.2"]

      arreglo_float = list(map(float, arreglo_str))

      print(arreglo_float)
      
      [1.5, 2.3, 4.7, 3.2]
      
      
  2:
  
      arreglo_str = ["1.5", "2.3", "4.7", "3.2"]

      arreglo_float = [float(elemento) for elemento in arreglo_str]

      print(arreglo_float)
      
      [1.5, 2.3, 4.7, 3.2]



 
 
 


