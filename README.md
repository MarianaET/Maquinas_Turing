#Maquinas Turing


Las Definiciones de las m�quinas las encontrar� en https://prezi.com/view/Ei0aQFNM3QT4U0CAfiEg/

Este proyecto consiste en la elaboraci�n de cinco m�quinas de Turing las cuales cada una haga una tarea entre

*Reconocer cadenas de pal�ndromos con lenguaje {a,b,c}
*Copiar patrones con lenguaje {a,b,c}
*Realizar una multiplicaci�n en c�digo unario con lenguaje {1,*} o {1,*,=}
*Realizar una suma en c�digo unario con lenguaje {1,+} o {1,+,=}
*Realizar una resta en c�digo unario con lenguaje {1,-} o {1,-,=}

Para que el programa funcione corretamente se debe de ingresar una cadena con el lenguaje indicado anteriormente en el textbox indicado como "Input".
Luego debe de seleccionar la m�quina con la que quiere trabajar con el Menu Strip. 

Para ver el funcionamiento de las m�quinas hay dos opciones, el bot�n "Run" y el bot�n "Por Paso".
El bot�n "Run" cada medio segundo realiza un paso de la m�quina escogida y solo se debe de observar como va cambiando la cinta y como se mueve el cabezal analizando cada posici�n.
Con el bot�n "Por Paso" el procedimiento es distinto. Este necesita clicks para que la m�quina vaya avanzando. Esto es para poder analizar de una mejor forma el cambio en la cinta y de posiciones del cabezal.

El bot�n "De Nuevo" refresca los datos de la m�quina escogida y de la cinta, para que pueda cambiar la m�quina a usar o analizar otra entrada. Si le da un click y no se cambia de m�quina, el programa asume que va a seguir utilizando la misma m�quina
Luego se tienen dos textbox llamados indicados estado y paso, los cuales indicar�n en qu� estado est� la m�quina y un contador de los pasos que se est� llevando en analizar la cadena.

El programa detecta cuando no se ha agregado ninguna cadena o no se ha escogido una m�quina, exceptuando en el caso del bot�n "De Nuevo". 
Cuando se tiene la cadena y la m�quina se procede a graficar la m�quina en el datagrid, en el cual se pueden ver los cambios que se le van haciendo a la cinta seg�n la s�laba que se est� analizando y el estado en el que se encuentra la m�quina.
La cinta tendr� el espacio de columnas en blanco necesarias para realizar la operaci�n ya que el programa las calcula antes que la m�quina empiece a funcionar para no tener columnas de m�s o de memos.

Si la m�quina encuentra una s�laba que no est� en los lenguajes indicados con anterioridad, marca error diciendo que hay un error en la entrada.
Si la m�quina no tiene transici�n con una s�laba en el estado indicado, se mostrar� un error diciendo de la cadena no cumple con los requerimientos.
De lo contrario, se mostrar� un mensaje diciendo que la cadena ha sido verificada, se ha duplicado el patr�n o se ha realizado la operaci�n.
La posici�n de la cabeza de la cinta se estar� indicando con un cuadro de color morado en la parte inferior de la cadena en el DataGridView

Para las operaciones no es necesario escribir el s�mbolo "=", ya que el programa detecta si est� o no. De ser el segundo caso, lo agrega.

Las transiciones se trabajaron de la siguiente forma:
*Con un switch se escoje el s�mbolo que se est� analizando
*Con if, else if y else se analiza el estado en el que se encuentra la m�quina.


Mi programa funciona correctamente ya que detecta todos los errores e indica los errores que se tienen en las transiciones. Adem�s haberle implementado el bot�n de "Por Paso"