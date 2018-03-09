#Respuestas
##Varios bugs
Al correr el programa _segfault en el debugger sin haberlo compilado 
utilizando flags de debug solamente nos dice el error que se produce, 
sin especificar la linea en el que este ocurre. Al compilar con este 
flag sabemos porque se rompe el programa, dado a que el espacio de 
memoria al que apuntan los punteros a y b no ha sido asignado, problema 
que resolvemos utilizando la funcion malloc. La mejor opcion de 
optimizacion para debuggear es -O0, ya que practicamente no realiza 
cambios al codigo al momento de compilar. Al agregar los warnings 
podemos determinar si el error fue de compilacion o de linkeo.
 
##FPE
Al agregar el flag -DTRAPFPE, le indicamos al compilador que el programa
incluya la funcion set_trap_fpe, lo que provoca que el codigo nos avise
cuando se produjo una excepcion de punto flotante, como cuando se divide
por 0 o se intenta calcular la raiz de un numero negativo.
