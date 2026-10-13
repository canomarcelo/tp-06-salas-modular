# Trabajo práctico 06
proyecto de partida es el práctico Nº 5, el cual fue modularizado.

## Proyecto de partida y cambios

Se modifico el el archivo index.js se le sacaron responsabilidades, las cuales
se crearon nuevos mmodulos.
1- se creo un modulo para los middleware, donde se creo dos archivos uno para los middleware globales
y otro para los particulares.
2- se creo un modulo servicios, el cual es el encagado de listar, buscar por id y crear reservas.
3- se creo el modulo controlador el cual es el encagado de recibir las peticiones y preparar una respuesta.
4- se creo el modulo rutas encagado de aocias un metodo http y una url.
5- se separo del index.js la responsabilidad de configura y armar la aplicacion, index.js
solo se encaga de levantar la aplicacion.

## Instalación y ejecución

para la instalacion se deje ejecutar npm install y la ejecucion npm start

## Configuración del entorno
La aplicación se configura mediante variables de entorno:
PORT = 3500  Puerto donde escucha el servidor. Debe ser un entero entre 1 y 65535. |
NODE_ENV 
Si no se define PORT, se puede abrir la aplicación en `http://localhost:3500`.

## Mapa de módulos y dependencias
index.js contiene los datos de ejemplo, crea el servicio y la aplicación.
configuracion.js lee y valida la configuración de entorno.
app.js configura Express, los middlewares globales, las vistas y las rutas.
middleware/solicitudes.js asigna un identificador a cada solicitud y registra su duracion.
middleware/reservas.js prepara las opciones de sala/turno y valida los datos enviados.
rutas/reservas.js conecta las URL y los metodos HTTP con el middleware y el controlador.
controladores/reservas.js  traduce las solicitudes en operaciones del servicio y respuestas HTML/JSON.
servicios/reservas.js mantiene en memoria las operaciones de listar, buscar por identificador y crear reservas.
## Pipeline y contrato de rutas

### Pipeline de solicitudes
### Rutas
## Formato y análisis estático
## Persistencia temporal y límites

se cargan algunas reservas desde un arreglo se puede agregar nueva reserva pero estas persisten
miestras la app siga en ejecucion, si se detiene o se reinicio la app los nuevos datos se pierden

Las reservas están almacenadas en memoria; por eso, las nuevas reservas se pierden al detener o reiniciar el servidor.