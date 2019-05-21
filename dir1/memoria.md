---
layout: "page"
title: Memoria
permalink: /memoria
---
<h1>Memoria.</h1>
Grupo techno team:<br>
• Guzmán Bernaldo de Quirós Fernández.<br>
• Ricardo Zambrana Zúñiga.<br>
• José Andrés Gómez Suarez.<br>
• Miguel Herraez.<br>
• Álvaro alcaide.<br>
</h3>1) Introduccion a la memoria:</h3>
Comenzamos el proyecto del videojuego realizando una encuesta a un grupo de personas a las que se
iba a dirigir a través de una amiga de un miembro del grupo; los resultados de las encuestas nos hicieron
enfocarnos hacia juegos de estrategia y nos pareció buena idea tomar como referencia el juego fire
emblem al cual varios miembros del grupo habíamos jugado, este consiste en un juego por turnos con
un protagonista y otros personajes que le acompañan y con los que también juegas para avanzar a
través de las diferentes pantallas hasta llegar al final del juego topándote con un jefe final con el que
debes acabar para ganar. Elegimos este título ya que nos pareció que la mecánica que tiene se ajusta a
las preferencias que tenían las personas encuestadas y además en un primer momento nos pareció
relativamente sencilla de implementar; los mapas se dividen en casillas y cada personaje tiene un
número determinado de casillas que puede avanzar y en función de esto el jugador selecciona a cuál
debe desplazarse cada personaje para atacar al enemigo.<br>
En primera instancia comenzamos con la historia la cual se basa en un grupo de guerreros los cuales se
unen por orden de un rey para realizar una misión, haciéndose grandes amigos e iniciando su propia
aventura en busca de una legendaria espada. Tras esto el diseñador gráfico comenzó a crear las
imágenes (mapas, sprites…) que utilizaríamos para el videojuego para la creación de estos usamos
programas como Tiled, Photoshop o Gimp; mientras tanto el desarrollador de la página web comenzó a
trabajar en ella utilizando Jekyll, y los programadores empezaron con el videojuego haciendo uso de
Netbeans.<br>
Mientras avanzábamos con el videojuego observábamos el código de otros juegos en Github para tomar
ideas que pudiésemos implementar en nuestro juego y nos ayudasen a mejorarlo. Uno de los primeros
cambios que hicimos en nuestro planteamiento inicial fue en el sistema de desplazamiento de los
personajes ya que nos dimos cuenta de que si en vez de seleccionar la casilla a la que se quería mover el
personaje utilizábamos el teclado el juego sería más dinámico. Todos los sonidos incluidos en el juego
los sacamos de una página llamada Opengameart.<br>
A lo largo de el proceso nos surgieron problemas como es inevitable: el principal problema fue que tras
añadir los portales si había zonas de colisión cerca el personaje no cambiaba de mapa; pero tras ajustar
el tamaño de las zonas de colisión cercanas conseguimos solventarlo.
Con la fecha de entrega cada vez más próxima nos dimos cuenta que quizás nuestro proyecto inicial era
demasiado ambicioso ya que el planteamiento de utilizar un grupo de personajes suponía una cantidad
de trabajo desmesurada para el tiempo del que disponíamos por lo que tuvimos que reducirlo a un
único personaje jugable. Para los combates con los enemigos nos basamos en Pokémon ya que este tipo
de combates son fáciles de aprender y no necesitan una explicación previa; de manera que el jugador
avanza por el mapa encontrándose con enemigos y tras derrotarlos podrá usar los portales
implementados para cambiar de mapa.<br>
<h3>2) Desarrolo del juego:</h3>
Tyrfing es un juego rpg por turnos basado en una historia fantástica medieval. En el menu principal
podrás escoger entre jugar ( que empezarás a crear al protagonista ), opciones ( que te permitirá hacer
pequeños cambios ), créditos ( muestra los créditos del juego ) y exit ( que te permitirá cerrar el juego )
Todo este menu esta creado desde Estado_0_MENU, configurando imagenes con variable de image de
la librería slick. Este devuelve el id 0 que sera iniciado desde la clase game.
Aquí puedes ponerle el nombre que quierás al personaje y equilibrar las estadísticas a tu gusto y elegir
entre un protagonista que sea chico o chica. Y no podrás empezar a jugar hasta que distribuya todos los
puntos de nivel.<br>
Esta pantalla es creada en la clase Estado_14_CREAR_PROTAGONISTA Y cuando le des a empezar
empezará la clase Estado_1_INTRODUCCION dibujando la imagen de historia.
Esto creará una imagen que explicará la acción a realizar y contará la historia de fondo. Despues iniciará
la clase Estado_1_PLAY que dibujará al mapa, protagonista elegido y los enemigos del mapa.
Dentro de este mapa cambiarás de mapa si acabas con el enemigo que esta a la derecha al final del
camino o a la izquierda en el otro final del camino o entrar al templo que se encuentra arriba a la
derecha.<br>
Si llegas hasta el enemigo, primero entraran en una fase de dialogo dentro de la clase BBDD_Dialogo
que se llamará de la clase Portales y tras acabar entrarás al estado de batalla que se encuentra en la
clase Estado_7_BATALLA.
Tras eso se empezará la batalla contra un enemigo.
Para acabar la batalla tendrás que bajar la vida del enemigo hasta 0 o menor. Una vez que termina
experimentarás otra pantalla de historia y volverás al mapa.
tras eso podrás cambiar el mapa pasando por los lugares antes mencionados llegando a lugares con
diferentes enemigos.<br>
Todo estos mapas y diseños de personaje han sido creados con Rpg maker traspasados a tiled para
poder ser usados. Y la música que se escucha ha sido cogida de la página opengameart.
Con eso ya estaría indicado todos los mapas creados para el juego. Para finalizar el juego necesitarás
entrar en el último mapa y derrotar al dragón que se encuentra en esa zona para recuperar un objeto
preciado<br>
<h3>3) Desarrollo de la página web</h3>
La página web la desarrollamos con Jekyll, usando el lenguaje de programación html; Jekyll ofrece la
opción de crear tus propios layouts creando archivos html e indicándolos al comienzo del código en los
archivos .md, estos hacen que la página cuente con los elementos creados en el layout especificado de
manera que no tengas que declararlos cada vez que crees una nueva página acelerando el trabajo; por
ejemplo las página de los personajes utilizan un mismo layout que muestra una imagen de cada uno de
ellos y a través del uso de condicionales conseguimos un fondo rojo en la imagen del personaje en el
que pincha el usuario.<br>
De la misma manera Jekyll permite utilizar headers los cuales son elementos que podemos implementar
en la parte del código que deseemos, de manera que no necesitamos reescribir el código del elemento
el concreto si no que solo tenemos que invocarlo. Por ejemplo el cabecero de nuestra página es un
header de manera que podemos introducirlos sin necesidad de volver a codificar el hipervínculo y la
imagen lo cual viene muy bien para agilizar el trabajo.<br>
Jekyll permite además la creación de variables propias; tales como el título de la página, el título del sitio
o el correo del desarrollador de manera que puedes acceder a ellas rápidamente y operar con ellas
como necesites, estas han de ser especificadas en el archivo config.yml.
Como podéis comprobar hay más personajes principales que los que usamos en el juego. Esto fue
debido a un cambio de planes por falta de tiempo. pero en un principio se tenía pensado usar 5
protagonistas y una historia algo diferente.
