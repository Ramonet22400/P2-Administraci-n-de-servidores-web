# P2. Administración de servidores web

**1. Explique con sus palabras que es una petición GET, POST, PUT y DELETE, remarcando sus diferencias.**

* GET: La petición lo que hace es solicitar un recurso.(ficheros, cookies...)
* POST: Esta petición es la encargada de enviar datos al servidor.
* PUT: Crea un elemento, pero es cierto que aunque se parezca a la petición POST, PUT es idempotente es decir que solo se ejecutara una vez.
* DELETE: Como bien indica el nombre esta petición elimina del servidor recursos.


**2. Cambie del puerto 80 al puerto 4444 el servidor apache2. Muestra desde el navegador 
su funcionamiento adjuntando una captura de pantalla.**

![img.png](img.png)

**3. Explica como activar, desactivar, reiniciar y recargar un servidor de Apache2
explicando la diferencia entre cada uno de los comandos utilizados.**

* Activar: para iniciar el servidor Apache2, tendremos que introducir el siguiente comando: sudo etc/init.d/apache2 start.
* Desactivar: detendremos el apache2 mediante el comando: sudo etc/init.d/apache2 stop.
* Reiniciar: para reiniciar apache2: sudo etc/init.d/apache2 restart
* Recargar: sudo etc/init.d/apache2 graceful, y de esta forma recargamos el servidor. Tendrás que tener el servidor iniciado

**4. ¿Dónde se encuentran los ficheros de configuración de Apache2?**

Para poder acceder al principal archivo de configuración de apache2, tendremos
que ejecutar el comando: nano /etc/apache2/apache2.conf.

**5. ¿Dónde se encuentran los ficheros de ejecución de Apache2?**

Podemos acceder a los ficheros de ejecución mediante la ruta /usr/bin.

**6. ¿Dónde se encuentran los ficheros de monitorización de Apache2?**

Para poder acceder a los ficheros de monitorización tendremos que poner /var/log.

**7. ¿Qué es un Firewall? ¿Para qué funciona? ¿Por qué es necesario?**

* ¿Qué es? Este es un programa de software o hardware, que filtran y examinan que reciben a traves de la conexión internet.

* Su función: Bloquear accesos no autorizados a equipos informáticos, a su vez permitiendo al mismo tiempo comunicaciones autorizadas.

* ¿Por qué es necesario?: Dada la gran cantidad de información y software malicioso que hay en la red, 
   los equipos han de ser debidamente protegidos para mantener tanto su integridad y funcionamiento, como la información que estos contienen.

**8. Explica con tus palabras las diferentes partes de una URL.**

La URL está dividida en: protocolo, servicio, dominio y finalmente la ruta.

* Protocolo: este especifica que método se ha utilizado para el intercambio de datos entre cliente y servidor.
* Servicio: este es el soporte de información. Este es la forma mediante se conectan los archivos.
* Dominio: se trata de un nombre único con el que se identifica una subarea de internet, es decir un sitio que está en el mar de internet. Digamos que el dominio es la ID.
* Ruta: esta es la navegación a traves de carpetas, archivos que se a echo para llegar a la pagina o lugar donde te encuentras. 

**9. Explica el funcionamiento del protocolo HTTP.**

Para entendernos la función que ejerce el HTTP es establecer como las páginas web se comunican desde el servidor web al navegador del usuario.

Dicho esto es HTTP funciona de la siguiente forma:

Primero de todo el HTTP acepta las peticiones desde el puerto 80.
Las sesiones HTTP se abren por un cliente HTTP (es decir, el navegador del usuario)
a través de un agente de usuario y se envía un mensaje de petición de conexión al servidor HTTP (es decir, el servidor web).

* Línea de petición
* Encabezadps
* Línea vacía
* Un cuerpo del mensaje opcional
* Una vez que la respuesta ha sido entregada el servidor web cierra la conexión.

Este tipo de conexión es conocido como Stateless. La conexión solo existe por el periodo que dure el intercambio de datos.
En función de la disponibilidad o no del recurso, HTTP proporciona un código de estatus apropiado 
(también conocido como ‘respuesta del servidor’), determinado por el protocolo. Son los siguientes:

1xx: un simple mensaje informativo

2xx: éxito de algún tipo (ej: 200 OK – file found)

3xx: el cliente a otra URL (ej: 301 moved permanently)

4xx: un error en el lado del cliente (ej: 404 archivo no encontrado)

5xx: un error en el lado del servidor (ej: 500 server error)