Contexto
El objetivo de este desafío es crear una página web sencilla con un “workspace” de Google Blockly y un botón para “ejecutar” el código programado por el usuario en el espacio de trabajo. Es un desarrollo sencillo, al estilo de un “Hola Mundo” o “getting started” (primeros pasos) con la librería, sin entrar en la profundidad de sus funcionalidades más complejas.

Detalles
Bloques custom
La “toolbox” o barra de bloques disponibles deberá incluir 3 “bloques”:
saludar(nombre) → recibe un parámetro de texto simple; se traduce con generador de javascript a alert(“¡Hola, ” + nombre + “!”)
preguntar(pregunta) → recibe un parámetro de texto simple; se traduce con generador de javascript a prompt(pregunta)
sumar(numeroA, numeroB) → recibe dos parámetros numéricos; se traduce con generador de javascript a:
	resultado = numeroA+numeroB; 
	alert(“El resultado de tu suma es: “+ resultado)

Funcionalidad
Al presionar el botón de “ejecutar”, se debe obtener el código JS generado por lo bloques ubicados por el usuario en el workspace, es decir, obtener el string de los bloques traducidos a javascript.

Existen diversas maneras de lograr “correr” dicho código, pero, por el alcance de este desafío, elegiremos la más sencilla, aunque no sea la más recomendable: se deberá ejecutar el código del string mediante la función global eval().

Algo así:

var codigoJS = “....” // métodos necesarios para generar la “traducción”
eval(codigoJS)

Documentación

Los siguientes links pueden resultar de mucha utilidad para resolver el desafío:

Documentación general de Blockly
Herramientas para desarrolladores

