# :white_circle: Lectura y ejercicios del ARM32

<p align="center"><a href="https://es.cooltext.com"><img src="https://images.cooltext.com/5474975.png" width="963" height="101" alt="Resumen de los elementos " /></a>
<br /><a href="https://es.cooltext.com"><a href="http://es.cooltext.com" target="_top"><img src="https://cooltext.com/images/ct_pixel.gif" width="80" height="15" alt="Cool Text: Generador de Logotipos y Gráficos." border="0" /></a></p>
  
#### Raspberry Pi surge con el objetivo de promover la ensenanza en informatica mediante el uso de conceptos basicos, sin embargo no se esperaba que se convirtiera en un ordenador de bajo costo  con multiples usos.

#### La funcionalidad que posee a un costo increiblemente bajo son el atractivo principal que posee la plataforma, dado que ofrece multiples conceptos atractivos que independientemente de que sean complejos sihuen atrayendo a muchas personas en general.

#### ARM es una arquitectura RISK de 32 bits, Se trata de una arquitectura que establece la base en la que se trabajara (plataforma patentada), pero quienes crean chips basados en esta son otras empresas lo que se difiniria como third parties , por lo que cada vez que es utilizada la arquitectura se reciven un porcentaje por su uso.

#### El chip en concreto que lleva la Raspberry Pi es el BCM2835, que contiene además de la CPU otros elementos como un núcleo GPU y un núcleo DSP el cual es un procesador más pequeño y simple que el principal, pero especializado en el procesado y representación de señales analógicas. La CPU en cuestión es la ARM1176JZF-S, un chip de la familia ARM11 que usa la arquitectura ARMv6k.

#### La arquitectura ARMv6 presenta un conjunto de 17 registros de los cuales 16 son principales y uno es de estado de 32 bits cada uno.

#### Su función de los registros generales es el almacenamiento temporal de datos. Son los 13 registros que van R0 hasta R12.existen Registros Especiales estos son los últimos 3 registros principales: R13, R14 y R15.

#### estos poseen dado su proposito e importancia nombres alternativos los cuales son:

#### SP/R13. Stack Pointer ó Puntero de Pila.irve como puntero para almacenar variables locales y registros en llamadas a funciones.
####
#### LR/R14. Link Register ó Registro de Enlace. Almacena la dirección de retorno cuando una instrucción BL ó BLX ejecuta una llamada a una rutina.
####
#### PC/R15. Program Counter ó Contador de Programa. Es un registro que indica la posición donde está el procesador en su secuencia de instrucciones. Se incrementa de 4 en 4 cada vez que se ejecuta una instrucción, salvo que ésta provoque un salto.
####
#### <p align="left"><a href="https://es.cooltext.com"><img src="https://images.cooltext.com/5474976.png" width="218" height="71" alt="Entorno" /></a>
<br /><a href="https://es.cooltext.com"><a href="http://es.cooltext.com" target="_top"><img src="https://cooltext.com/images/ct_pixel.gif" width="80" height="15" alt="Cool Text: Generador de Logotipos y Gráficos." border="0" /></a></p> 
###
#### Los pasos habituales para hacer un programa sin importar que que lenguaje se trate son los siguientes: 
####
- Escribir el programa en el lenguaje fuente mediante un editor de programas. 
- El resultado es un fichero en un lenguaje que puede entender el usuario, pero no la máquina. - utilizar un programa traductor Para traducir a lenguaje máquina. 
- generacion de un fichero con la traducción de dicho programa.  
- creacion de un fichero ejecutable el cual contiene el programa traducido más una serie de códigos que debe tener todo programa que vaya a ser ejecutado en una máquina determinada. 
- Poseer e implementar librerías del lenguaje. 
- unir el código del programa con el código de las librerías lo que se conoce como mantador el cual crea el ejecutable.
####
#### Una vez que se tiene un programa sintácticamente correcto lo podemos ejecutar, pero ésto no implica que el programa sea correcto. Todas las instrucciones pueden ser correctas, pero se puede haber olvidado poner la condición de salida de un bucle o que sencillamente el programa no funcione como se esperaba. Estos errores sólo se pueden detectar en tiempo de ejecución. Para poder eliminarlos se utiliza un depurador de programas. El depurador nos permite ejecutar el programa instrucción a instrucción y ver todos los valores que se van a calcular, de manera que podemos encontrar los errores.
####
##
#### El ensamblador es un lenguaje de bajo nivel que permite un control directo de la CPU y todos los elementos asociados. Cada línea de un programa ensamblador consta de una instrucción del procesador y la posición que ocupan los datos de esa instrucción.
####
#### Desarrollar programas en lenguaje ensamblador es un proceso laborioso. El procedimiento es similar al de cualquier lenguaje compilado. estas terminan siendo un conjunto de instrucciones que forman un módulo fuente. Este módulo es la entrada del compilador, que se encarga de checar la sintaxis y lo traduce a código máquina formando un módulo objeto. Finalmente, un enlazador traduce todas las referencias relativas a direcciones absolutas y termina generando el ejecutable.
  
#### El lenguaje ensamblador presenta una serie de ventajas e desventajas con respecto a otros lenguajes de más alto nivel. Al ser un lenguaje de bajo nivel, presenta como principal característica la flexibilidad y la posibilidad de acceso directo a nivel de registro. como desventaja programar en ensamblador es laborioso puesto que los programas contienen un número elevado de líneas y la corrección y depuración de éstos se hace difícil.
  
#### Las directivas son expresiones que aparecen en la fuente e indican al compilador que realice determinadas tareas en el proceso de compilación. Son fácilmente distinguibles de las instrucciones. El uso de directivas es aplicable sólo al entorno del compilador, por tanto varían de un compilador a otro y para diferentes versiones de un mismo compilador.


```a1 :   .byte         1        /* tipo byte, inicializada a 1 */ 
   var2 : .byte        ’A ’      /* tipo byte, al caracter ’A’ */
   var3 : .hword      25000      /* tipo hword (16 bits ) a 25000 */
   var4 : .word     0x12345678   /* tipo word de 32 bits */
   b1 :   .ascii     " hola "    /* define cadena normal */
   b2 :   .asciz     " ciao "    /* define cadena acabada en NUL */
   dat1 : .zero        300       /* 300 bytes de valor cero */
   dat2 : .space      200,4      /* 200 bytes de valor 4 */

```


<p align="left"><a href="https://es.cooltext.com"><img src="https://images.cooltext.com/5474978.png" width="350" height="82" alt="Tipos de dato" /></a> <br /><a href="https://es.cooltext.com"><a href="http://es.cooltext.com" target="_top"><img src="https://cooltext.com/images/ct_pixel.gif" width="80" height="15" alt="Cool Text: Generador de Logotipos y Gráficos." border="0" /></a></p> 
 
#### Tabla de lso tipos de datos básicos así como su tamaño y rango de representación.

```
ARM         Tipo en C            bits            Rango
.byte       unsigned char         8              0 a 255
            (signed) char         8           -128 a 127
.hword      unsigned short int    16             0 a 65.535
.short      (signed) short int    16       -32.768 a 32767
.word       unsigned int          32             0 a 4294967296
.int        (signed) int          32   -2147483648 a 2147483647
unsigned    long int              32             0 a 4294967296
(signed)    long int              32   -2147483648 a 2147483647
.quad       unsigned long long    64             0 a 2
```    
#### En el lenguaje ensamblador los tipos son neutrales al signo, lo importante es la longitud en bits del tipo. La mayoría de las instrucciones hacen la misma operación tanto si se trata de un número natural como si es entero en complemento a dos. 

#### Las instrucciones de salto pueden producir saltos incondicionales (b y bx) o saltos condicionales. Cuando saltamos a una etiqueta empleamos b, mientras que si queremos saltar a un registro lo hacemos con bx. La variante de registro bx la solemos usar como instrucción de retorno de subrutina, raramente tiene otros usos.

#### En los saltos condicionales se anaden dos o tres letras a la (b/bx), mediante las cuales se condiciona si se salta o no dependiendo del estado de las banderas. Estas condiciones se pueden añadir a cualquier otra instrucción, aunque la mayoría de las veces lo que nos interesa es controlar el flujo del programa y así ejecutar o no un grupo de instrucciones dependiendo del resultado de una operación.


``` 
main :       mov r1, # 1
             mov r2, # 2
             bl nivel1
             mov r5, # 5       /* Siguiente instrucción */
             ...
             
nivel1 :     push { lr }
             mov r3, # 3
             bl nivel2
             pop { lr }
             bx lr
             
nivel2 :     mov r4, #4
             bx lr
``` 

#### Las instrucciones de salto en la arquitectura ARM abarcan una zona muy extensa.
