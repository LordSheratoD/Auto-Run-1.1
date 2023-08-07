# Bot de recolección de recursos de New World

Permite ejecutar un bot para recolectar recursos siguiendo una ruta predefinida. El programa no utiliza los recursos del juego, solo interactúa con la interfaz utilizando la biblioteca OpenCV.

## Instalación:

1. Descarga e instala OverWolf, consulta el readme en la carpeta "ts" para más información.

2. Copia el repositorio en Visual Studio o ejecuta la solución.

3. Compila el proyecto en Visual Studio.

4. Después de compilar, se creará una carpeta "bin" en la carpeta "AutoRun 1.1". Mueve/Copia la carpeta "Images" a "..\Auto Run 1.1\bin\Debug\net5.0-windows". Los "Images" contienen las plantillas necesarias para que el bot funcione durante la recolección de recursos.

## Controles:

- Tecla F2: Inicia el bot.
  
- Tecla F4: Detiene la ejecución del programa.

- Tecla E: Inicializa el punto de recolección de recursos.

- Botón "StartStream": Inicializa la grabación de la ruta mientras el personaje se mueve.

## Descripción:
En este momento, solo se puede ejecutar el bot estando en la lista blanca de OverWolf, ya que el equipo de desarrollo ha deshabilitado la capacidad de ejecutar y probar aplicaciones no autorizadas. La API de OverWolf permite obtener las coordenadas del personaje del juego y guardarlas en un archivo, lo que permite extraer estos datos y dirigir al personaje en la dirección deseada. Existe otra forma de hacerlo utilizando OCR, pero incluso con el uso de filtros, este método es bastante impreciso, y otra limitación es el bajo FPS, alrededor de 7-10 cuadros por segundo, lo cual no es suficiente para un funcionamiento correcto.

## Grabación de la ruta:
Antes de comenzar, es necesario planificar la ruta más segura, minimizando los objetos que puedan obstaculizar al bot (montañas donde se deba saltar o caer desde una altura, edificios, pasajes estrechos). La ruta debe ser cíclica, es decir, el punto de inicio debe coincidir con el punto final de la ruta. El botón "StartStream" inicia la grabación del movimiento del personaje y el archivo con las coordenadas grabadas se encuentra en la ruta <nombre_de_usuario>\Documents\OverwolfAutopath\stream.pos. Al presionar la tecla "E", se grabará la ubicación actual como punto de recolección de recursos. Al finalizar la ruta, es necesario detener la grabación presionando el botón "StopStream" para crear el archivo "stream.pos" con las coordenadas de la ruta recorrida.

## Ejecución del bot:
Después de que la ruta se haya grabado y se haya creado el archivo "steam.pos", puedes ejecutar el bot directamente. Antes de iniciar, asegúrate de configurar la resolución a 1280x1024 en modo ventana, ya que se utiliza la biblioteca OpenCV para identificar el recurso por patrón. No hay plantillas disponibles para otras resoluciones, por lo que el bot no funcionará correctamente con una resolución diferente, ignorando los puntos de recolección de recursos. Otro aspecto importante es ajustar la velocidad de la cámara en la configuración del juego al mínimo. Puedes iniciar el bot presionando la tecla F2 o el botón "StartBot". Puedes iniciar en cualquier punto cercano a la ruta grabada. Si el personaje está lejos de la coordenada más cercana, correrá en línea recta ignorando los obstáculos, lo que aumenta la probabilidad de que el personaje quede atascado. Puedes detener la ejecución presionando la tecla F4 o el botón "StopBot".

## Video
https://www.youtube.com/watch?v=J6WFTHFlyuw&ab_channel=%D0%94%D0%BC%D0%B8%D1%82%D1%80%D0%B8%D0%B9%D0%94%D0%BE%D0%BD
