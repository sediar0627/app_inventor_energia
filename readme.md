# Energy FYL

## Descripcion

Aplicacion hecha en App Inventor cuyo proposito tiene explicar todo lo relacionado a energia y sus tipos. Implementando una ventana donde se definen los conceptos de los mismos, otra donde se evalua lo aprendido y una de anexos multimedia.

## Aspectos Tecnicos

Tanto las definiciones como las preguntas pueden ser editadas, correspondiendo a una actualizacion de los archivos de la aplicacion.

#### Notas:
- Estos cambio no involucran el codigo de la aplicacion.
- Estos cambios son hechos a archivos de texto.
- Una vez cambiado los archivos, se deben copiar en la carpeta de archivos.

### Ubiacion de la carpeta de archivos

- Almacenamiento Interno
  - Android
    - data
	  - appinventor.ai_sdiazarrieta0627.app_energia
	    - files

Se debe tener la siguiente estructura dentro de la carpeta 'file'

![Estructura internar de la carpeta file](/img/estructura_archivos.PNG)

##### Consideracion: 
Se debe tener conectado via USB al dispostivo Android que contiene la aplicacion, y con la configuracion de compartir archivos activa.

### Archivo 'root_informacion.txt'

Este archivo contiene la informacion de los conceptos. Esta compuesto por lineas con la siguiente estructura:

- Titulo del concepto
- Ruta del archivo de texto con la definicion del concepto
- Ruta del archivo de texto que contiene la imagen del concepto

##### Ejemplo:
- Fuentes de energía,conceptos/fuentes_de_energia.txt,sin_imagen
- Energía solar,conceptos/energia_solar.txt,imagenes/img_energia_solar.txt

##### Notas:
- Cada parte de la estructura de la linea es separada por una coma.
- En caso de que no se desea tener imagen, se debe escribir 'sin_imagen'.
- La definicion del concepto esta en una carpeta llamada 'conceptos', por ende se antepone al nombre del archivo que contiene la informacion la siguiente expresion 'conceptos/'. Funciona igual para la imagen.

### Archivo 'root_preguntas.txt'

Este archivo contiene la informacion de las preguntas. Esta compuesto por lineas con la siguiente estructura:

- Titulo de la pregunta
- Numero de la posicion que tiene la respuesta correcta
  - Es un numero entre 1 y 4
- Respuesta 1
- Respuesta 2
- Respuesta 3
- Respuesta 4
- Ruta del archivo de texto que contiene la imagen de la pregunta

##### Ejemplo:
- Preguna 1,1,respuesta a1,respuesta b1,respuesta c1,respuesta d1,imagenes/imagen.txt
- Preguna 2,4,respuesta a2,respuesta b2,respuesta c2,respuesta d2,sin_imagen

##### Notas:
- Cada parte de la estructura de la linea es separada por una coma.
- En caso de que no se desea tener imagen, se debe escribir 'sin_imagen'.
- Para definir la ruta de la imagen, funciona igual que la nota anterior.

### Guardado de imagenes

La aplicacion usa las imagenes codificadas en base64, para visualizarlas en la aplicacion.

##### Notas:
- Puede generar el base64 de la imagen en la siguiente URL https://www.base64-image.de

- Toda imagen codificada en base64 tiene la siguiente estructura:
  
  - data:image/tipo de imagen;base64,
  - base64 codificado de la imagen.

  ![Ejemplo de imagen en base 64](/img/ejemplo_base64.PNG)

  - Para que la aplicacion pueda leer la imagen, se debe eliminar siempre todo el contenido que esta anterior a la coma, e incluyendo la coma. Como se indica en la imagen.

  ![Ejemplo de imagen en base 64](/img/ejemplo_base64_bien.PNG)

- Guardar el codigo base64 de la imagen en un archivo de texto con un nombre descriptivo


### Guardado de definiciones

Se debe crear el archivo de texto en la carpeta 'conceptos', con el nombre que considere correcto 

![Ejemplo de imagen en base 64](/img/conceptos.PNG)

![Ejemplo de imagen en base 64](/img/ejemplo_conceptos.PNG)

### Recomendacion para el nombre de los archivos de texto:
- Guardelos con un nombre nemo tecnico, y sin caracteres especiales.
- El unico caracter especial que esta bien usar es '_'

## Importante:

Se deben de configurar todos los conceptos, con las preguntas antes de arrancar la aplicacion, para evitar errores.