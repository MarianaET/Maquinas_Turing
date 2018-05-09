#Maquinas Turing


Las Definiciones de las máquinas las encontrará en https://prezi.com/view/Ei0aQFNM3QT4U0CAfiEg/

Este proyecto consiste en la elaboración de cinco máquinas de Turing las cuales cada una haga una tarea entre

*Reconocer cadenas de palíndromos con lenguaje {a,b,c}
*Copiar patrones con lenguaje {a,b,c}
*Realizar una multiplicación en código unario con lenguaje {1,*} o {1,*,=}
*Realizar una suma en código unario con lenguaje {1,+} o {1,+,=}
*Realizar una resta en código unario con lenguaje {1,-} o {1,-,=}

Para que el programa funcione corretamente se debe de ingresar una cadena con el lenguaje indicado anteriormente en el textbox indicado como "Input".
Luego debe de seleccionar la máquina con la que quiere trabajar con el Menu Strip. 

Para ver el funcionamiento de las máquinas hay dos opciones, el botón "Run" y el botón "Por Paso".
El botón "Run" cada medio segundo realiza un paso de la máquina escogida y solo se debe de observar como va cambiando la cinta y como se mueve el cabezal analizando cada posición.
Con el botón "Por Paso" el procedimiento es distinto. Este necesita clicks para que la máquina vaya avanzando. Esto es para poder analizar de una mejor forma el cambio en la cinta y de posiciones del cabezal.

El botón "De Nuevo" refresca los datos de la máquina escogida y de la cinta, para que pueda cambiar la máquina a usar o analizar otra entrada. Si le da un click y no se cambia de máquina, el programa asume que va a seguir utilizando la misma máquina
Luego se tienen dos textbox llamados indicados estado y paso, los cuales indicarán en qué estado está la máquina y un contador de los pasos que se está llevando en analizar la cadena.

El programa detecta cuando no se ha agregado ninguna cadena o no se ha escogido una máquina, exceptuando en el caso del botón "De Nuevo". 
Cuando se tiene la cadena y la máquina se procede a graficar la máquina en el datagrid, en el cual se pueden ver los cambios que se le van haciendo a la cinta según la sílaba que se está analizando y el estado en el que se encuentra la máquina.
La cinta tendrá el espacio de columnas en blanco necesarias para realizar la operación ya que el programa las calcula antes que la máquina empiece a funcionar para no tener columnas de más o de memos.

Si la máquina encuentra una sílaba que no esté en los lenguajes indicados con anterioridad, marca error diciendo que hay un error en la entrada.
Si la máquina no tiene transición con una sílaba en el estado indicado, se mostrará un error diciendo de la cadena no cumple con los requerimientos.
De lo contrario, se mostrará un mensaje diciendo que la cadena ha sido verificada, se ha duplicado el patrón o se ha realizado la operación.
La posición de la cabeza de la cinta se estará indicando con un cuadro de color morado en la parte inferior de la cadena en el DataGridView

Para las operaciones no es necesario escribir el símbolo "=", ya que el programa detecta si está o no. De ser el segundo caso, lo agrega.

Las transiciones se trabajaron de la siguiente forma:
*Con un switch se escoje el símbolo que se está analizando
*Con if, else if y else se analiza el estado en el que se encuentra la máquina.


Mi programa funciona correctamente ya que detecta todos los errores e indica los errores que se tienen en las transiciones. Además haberle implementado el botón de "Por Paso"