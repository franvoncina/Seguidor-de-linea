# Seguidor de lineas
![foto](https://raw.githubusercontent.com/franvoncina/Seguidor-de-linea/main/mblock.programacion.jpg)
Bueno Nosotros hicimos este repositorio con el propósito de ayudar a las personas que puedan armar su mBot y que siga sus líneas de camino.
Los primero que debemos tener para armar un mBot son:
-   Placa mCore.



-   Sensor de luminosidad (en placa).



-   Emisor y receptor de infrarrojos (en placa).

   -   Dos luces LED RGB para emitir cualquier color (en placa).
   
-   Zumbador para emitir notas musicales (en placa).

-   Un pulsador programable (en placa).
 
-   Sensor de proximidad por ultrasonidos.
 
-   Sensor sigue-líneas.

-   Módulo bluetooth, para usarlo con el móvil o PC. En la versión 2.4G cambia el módulo bluetooth por un emisor y receptor USB para conectar a PC.

-   2 micro motores TT.

-   Cables y conectores.

![enter image description here](https://juegosrobotica.es/wp-content/uploads/mbot-contenido.jpg)

![enter image description here](https://juegosrobotica.es/wp-content/uploads/mBot-assembly.gif)

Como hicimos para que el mbot siga su propio carril con un obstáculo adelante para esquivarlo 
Bueno lo primero hicimos el código para que pueda funcionar y haga lo que se le dice. 
Después Los sensores de línea son  **dos optoacopladores de reflexión**  que montaremos en la parte inferior delantera del robot. Utilizan la reflexión de  **luz infrarroja para detectar el tono del suelo**  en el punto en que se encuentra el robot.

El módulo, está compuesto por una estructura compacta donde la fuente emisora de luz y el detector están dispuestos en la misma dirección para poder detectar mediante el uso de los rayos infrarrojos la luz reflejada en una superficie. Una vez aprendido como funciona el sensor, vamos a resolver la programación siguiendo la siguiente lógica:

**Si ambos sensores se encuentran sobre la línea negra nuestro robot debe avanzar hacia delante**, por lo tanto ambos motores deberán funcionar en el mismo sentido y misma velocidad.
Si nuestro robot se desvía hacia la izquierda, es decir, el sensor de la parte izquierda queda fuera de la línea, el motor izquierdo irá a más velocidad que el derecho para rectificar la posición. Si por el contrario nuestro robot se desvía hacia la derecha quedando el sensor de la parte derecha fuera de la línea, el motor derecho irá a más velocidad que el izquierdo para volver al centro de la línea.

Ya disponemos de la lógica a seguir para programar nuestro robot. Ahora podemos reflejar está discusión en una tabla de la verdad, para que nos resulte más fácil llevar a cabo el programa.
![tabla](https://github.com/franvoncina/Seguidor-de-linea/blob/main/fotos/TABLA.png)
