## sirio-doc

#Descripcion general 
SIRIO es una variante de un respirador automatizado.
Hemos decidido usar un movimiento lineal en vez que rotatorio para empujar el depósito de aire.
El diseño es compacto y estamos trabajando en dos líneas paralelas:
- VERSION INDUSTRIAL  fabricado en corte láser y doblado de acero mas piezas mecanizada en material sanitario 
Gracias al proceso de corte láser y doblado de chapa es posible fabricar rápidamente varios modelos al dia, el material es resistente a temperatura y se puede esterilizar.
Se está trabajando en una electrónica custom.

- VERSIÓN EMERGENCIA: Fabricado por impresión 3D y posiblemente corte laser 
Todas las piezas caben en una impresora estándar con área de impresión de 200*200*200, la electrónica es una básica de impresora (arduino mega + ramps + display) pero estamos evaluando la posibilidad de fabricar una shield sencilla.
Las piezas mecánicas son varillas lisas de 8mm típica de reprap, tuercas y tornillos estándar
La única pieza más complicada para conseguir es el husillo que nos ha proporcionado Igus. Para la versión Maker, estamos evaluando la posibilidad de usar un husillo con un paso amplio y  tener la posibilidad de cambiar los parámetros de velocidad desde la pantalla.

#Mecanica
Despues de probar las ventajas del husillo. Nos dimos cuenta del handicap que tenia la geometria que estabamos trabajando. Cuando queriamos adaptar diferentes tipos de rees. Asi que nos hemos puesto manos a la obra. Y hemos rediseñado de nuevo por completo todo el sistema. 
Ahora trabaja con una trayectoria vertical completamente. Por lo que no tenemos desplazamiento en el globo.
Lo tenemos abrazado por una parte mas pequeña. Ojo esto es muy importante. Ya que permite al globo una deformacion tangencial. Sin probocar pliegues de donde se pueda iniciar una fisura. Por lo que este sistema es mas amable con las deformaciones que se producen en el mismo.
Para aumentar la fiabilidad hemos añadido rodamientos 608 con unos collarines que se abrazan al husillo y absorveran los esfuerzos axiales. Por lo cual el motor ya no sobre ningun esfuerzo y solamente tiene que transmitir par.
Hemos reducido el tamaño con este diseño. Permitiendo imprimir todo el conjunto en maquinas con cama de 200x200. 
Al unir las 2 guias por arriba y por abajo. Con la pletina que porta el husillo. Todo el sistema queda echo un cuerpo. Eso significa que los casquillos que hacen de guia no tengan que tener mucha precision. Y puede trabajar perfectamente con 0.5mm de holgura sin que eso afecte a su funcionamiento. Es decir. Se puede poner rodamientos lineales. Pero en caso de necesidad el acabado de impresion seria mas que suficiente.
Hemos desarrollado el sistema pensando en la facilidad en el resto del mundo. Pudiendo usar husillo de igus. De 6_8_10.  Husillo de los sistemas empleados en impresoras. E incluso varilla roscada de m12 en casos muy heavys
Tambien es bastante mas seguro ya que toda la mecanica se queda dentro de un cajon. Y el resto lo que sobresale es solamente el empujador.
El prototipo estara listo mañana. Y quedamos a la espera de colaboracion en cuanto a asesoramiento para desarrollar los sistemas de valvulas. Y sensores necesarios para poder convertir casi cualquier balon. En un respirador util para salvar vidas. 
Tambien nos gustaria si no es mucho pedir que compartais la informacion de los parametros que necesitaremos programar y como gestionar todo eso ya que en ese sentidos estamos un poco parados. 

#Electronica
Bill of materials actual y futura
placa base
https://www.amazon.es/impresora-Controlador-Controller-Mega2560-disipador/dp/B07XV2YKG4/ref=sr_1_9?__mk_es_ES=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=ramps&qid=1584969011&sr=8-9
display
https://www.amazon.es/Kookye-Pantalla-controlador-adaptador-impresora/dp/B019SXNH1S/ref=sr_1_11?__mk_es_ES=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=ramps&qid=1584969011&sr=8-11

sensor presion
   https://es.rs-online.com/mobile/p/sensores-de-presion/8369039/


#SOFTWARE


MENU:
Hola mundo
Homing
Offset botella
velocidad
START

#Neumatica (Alberto)
El sistema de válvulas unidireccionales se realizó en una primera versión directamente todo en PLA. Conforme fuimos avanzando, nos dimos cuenta de ciertos aspectos para mejorar tanto la impresión, como la estanqueidad del conjunto, tomando la decisión de incorporar una ranura para una junta tórica que asegurara el cierre hermético en la dirección de bloqueo, y mejorando la calidad del obturador disminuyendo la altura de capa en la impresión.El sistema ha sido diseñado con racores para tubo de 22mm flexible. Tras seis diseños sucesivos, logramos conseguir un sistema funcional que consta de las siguientes piezas y características:


Válvula (cuerpo inferior):




Layer height (Altura de capa): 0.2
Perimeters (Líneas perimetrales): 5
Infill (Densidad de relleno): 50%

Impresión sin soportes en la misma disposición que en la foto.






Válvula (cuerpo superior):




Layer height (Altura de capa): 0.2
Perimeters (Líneas perimetrales): 5
Infill (Densidad de relleno): 50%

Impresión sin soportes en la misma disposición que en la foto.





Obturador:


Layer height (Altura de capa): 0.1
Perimeters (Líneas perimetrales): 2
Infill (Densidad de relleno): 100%

Impresión sin soportes en la misma disposición que en la foto.

El obturador ha de completarse con una junta tórica de 19mm de Diámetro interior y 2.5 mm de grosor.



Collarín soporte:





Layer height (Altura de capa): 0.2
Perimeters (Líneas perimetrales): 5
Infill (Densidad de relleno): 50%

Impresión sin soportes en la misma disposición que en la foto.


