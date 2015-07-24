# Sesión 2
### JBH, @escusado, 2015

> Disclaimers
> Este NO pretende ser un curso profesional de pilotaje de `UAV`'s, es un espacio
> hobbista de introducción al area de multicopters con enfoque en carreras.
>
> El vocabulario técnico usado en este taller será en inglés, dado que la mejor y
> más reciente información se encuentra en este idioma para hacer que el asistente
> se familiarice con el slang desde un principio.
> [Liang Glossary Guide](http://blog.oscarliang.net/quadcopter-acronyms-term-glossary-word-drone/)

# Autoproclaimed Aeronautic Engineer

Hoy en día el dieño y armado de multorores se ha vuelto bastante accesible tanto
economica como ingenierílmente, los costos bajan día con día y el hardware y software
se vuelve más sencillo de ultilizar. Hoy es comparable con armar una computadora
en el 2000.

## #1 Rule

- Aim for simplicity: Lo que no está a bordo no puede fallar.

No solo se vuelve sencilla la ingenieria del craft, también reduce el peso y
contribuye al lift.

## Design and iteration (Build, fly, crash, repeat)

No importa si estás desarrollando un craft desde 0, armando uno de partes compradas
ó customizando uno comercial, estarás tomando desciciones sobre la ingeniería del
craft. Esta es una **breve introducción** al diseño e ingeniería de multirotores de
carreras, aún así la matoría de los puntos aplican para cualquier tipo de multirotor.

# Design

## Problema -> solución

Piensa primero en la necesidad que el quad debe cubrir, evalua el peso y tamaño
del payload que quieres en el aire:

- Cámaras
- Sensores
- Sistemas de entrega
- Paracaídas
- Luces
- etc.

Conociendo el peso y dimensiones de tu payload podrás coemenzar a decidir que
componentes comprar, lo mejor es buscar que builds similares existen, y ver que
componentes están disponibles.

Con una idea de lo que necesitas, es necesario sumar el peso de los componentes
al peso del payload.

Es importante usar como herramienta las hojas de test de motores para saber que
fuerza tiene con varias configuraciones de baterías y props.

![strestests](/img/efficiency-test.png)

Necesitas como mínimo una proporción de 2:1 (2 thrust : 1 peso total del craft)

Y es importante envetualmente hacer tus propias pruebas de trhust:

![thrust-test](/img/thrust-test.jpg)

Lo que sigue es saber cuantos motores queremos, existen varias configuraciones
de multirotres y todas cubren una necesidad especial, pero la relga es: `Más helices
hacen a un craft más estable` dado que mueven aire en un area más grande (como
si cada motor fuera un punto de apoyo).

Al final solo tienes que dividir el trhust deseado entre la cantidad de motores.

Para poder decidir la cantidad de motores deseada es necesario conocer los
tipos de multirotores y sus usos ([ref](http://blog.oscarliang.net/how-to-choose-motor-and-propeller-for-quadcopter/)):

# Multicopter Types

Cáda configuración ofrece caracteristicas distintas, pero después de 4 las configuraciones
simetricas se comportan igual. Existen algunas asimetricas después de 3, pero son un
poco exóticas. ([ref](http://www.dronethusiast.com/what-you-should-know-about-multicopter-configurations/), [ref](http://www.computersrwilde.com/Projects/hexacopter/design1.html))

## BiCopter

Considerado el más simple ya que sólo cuenta con 2 motores que se alinean con servos
para lograr el `yaw`, el menos robusto de la familia dado que con 2
motores el rango de carga es muy corto. Poco popular en el mundo de RC ya que
son difícil de configurar y por su poca practicidad es considerado más un reto
técnico que un craft funcional: ([avar gunship](http://flitetest.com/articles/Avatar_Gunship_Scratch_Build))

![bicopter](/img/bicopter.jpg)
![bicopter-diag](/img/bicopter-diag.jpg)

## Tricopter

Cuenta con 3 motores que pueden ser configurados en posiciones `Y` o `T` usualmente
con una separación de 120º entre ellos, cuenta con 2 motores montados en los
brazos y 1 uno más en la cola, este último controla el `yaw` utilizando un `servo`,
Esto vuelve su ingeniería un poco más compleja ya que añade un segundo tipo de
componente motorizado y controlado desde tierra que comparte control del craft
con el motor de cola. Lo intenresante del tri es que precisamente esta caracteristica
lo vuelven extremadamente ágil y con un tipo de vuelo muy particular que no se
logra con otras configuraciones. ([quanum trifecta](https://www.youtube.com/watch?v=wD3rhzxb9I8))

![y-tricopter](/img/y-tricopter.png)
![t-tricopter](/img/t-tricopter.png)
![tricotper-diag](/img/tricopter-diag.jpg)

## Quadcopter

El más popular dado que es la configuración mínima para maniobrar con un sólo tipo
de motor. Existen várias configuraciónes:

# `X`

Excelente maniobrabilidad, dado que su centro de masa está justo al centro, perfecto
para vuelo acrobático. ([ref](https://www.youtube.com/watch?v=oR3q4hlmoEo))

![x-quad](/img/x-quad.jpg)

# `+`

Dado que su vuelo se asemeja más al de un avión, hay quién prefiere este tipo de
dirección, pero presentan problemas si es necesario montar una cámara que mire al
frente dado que las hélices obstruirían la vista. ([ref](https://www.youtube.com/watch?v=Cwx5GqKW--8))

![plus-quad](/img/plus-quad.jpg)

# `H`

El más popular en el mundo de FPV dado que tiene un area más gránde para el payload
y permite montar los componentes muy fácil además, dado que los motores están
separados al frente permite colocar las cámaras mirando al frente sin ningún problema.

![h-quad](/img/h-quad.jpg)

Todos funcionan bajo el mismo principio:

![quad-diag](/img/quad-diag.jpg)
([ref](https://sites.google.com/site/npaecopterguide/multirotor_getting_started/flight-theory-multi-rotor))

## Pentacopter

Otra de las configuraciones exóticas, usa las mecánicas del quad.

![pentacopter](/img/pentacopter.png)

## Hexacopter

Cuenta con 6 motores, sus mecánicas son muy parecidas a las del quad, y es la
ruta más inmediata para escalar la capacidad de carga y estabilidad. Además de
ofrecer redundancia de manera muy sencilla, uno de los motores puede fallar y aún
así poder aterrizar de manera segura.

![hexacopter](/img/hexacopter.jpg)
![hexacopter-diag](/img/hexacopter-diag.jpg)
![hexh](/img/hexh.jpg)

En el mundo de FPV los Hexas no son tán populares ya que al ser máquinas con
prestaciones más serias e ingeniería más compleja que los quads, solo los pilotos
más experimentados optan por este tipo de configuración. Por esta razón la oferta
de estas plataformas no es tán grande y dió espacio para que las pocas que existen
se hicieran algo populares:

### TBS Gmini
![tbs-gemini](/img/tbs-gemini.jpg)

### Blackout Minispider Hex
![blackout-minispider](/img/blackout-minispider.JPG)

### HK Thorax Hex
![thorax-hex](/img/thorax-hex.jpg)

### Vortex Hex (soon)
![vortex-hex](/img/vortex-hex.jpg)

### Octocopter

De nuevo la ruta para escalar a más peso y estabilidad es mediante más helices,
y 8 es es el siguiente paso simetrico, aumentando costo y redundacia esta
configuración permite que hasta 3 hélices fallen y aún así poder aterrizar.

![octocopter](/img/octocopter.jpg)
![octocopter-diag](/img/octocopter-diag.png)

### > 8

De 8 en adelánte todo es igual, escala tamaño, capacidades, costo y estabilidad.

### Scale to double motors

## Y4 – 4 motors

Este tipo de multirotores se caracteriza por tener propelas montadas en contra,
logra `yaw` aumentando o disminuyendo la potencia de cualquiera de las 2.

![y4copter](/img/y4copter.jpg)
![y4copter-diag](/img/y4copter-diag.jpg)
[y4copter](https://www.youtube.com/watch?v=QEQto96adUU)

## Y6

Esta configuración usa props CC y CCW en cada brazo para el doble de thrust,
tienen el lift cercano a un hexa pero en el tamaño de un tri, lamentablemente
la configuración coaxial lo vuelve menos eficiente.

![y6](/img/y6.jpg)
![y6-diag](/img/y6-diag.jpg)
[y6](https://www.youtube.com/watch?v=F9lLUG23MOI)

## X8 >

![x8](/img/x8.jpg)
![x8-diag](/img/x8-diag.jpg)
[x8](https://youtu.be/XIWBoIRSmTo?t=47s)

### x12

![x12](/img/x12.webp)
[x12](https://vimeo.com/102573098)

## V Tail

Pierde thrust al mantener los motores en ángulo, pero al hacer `yaw` no pierde
altura.

![vtail](/img/vtail.jpg)
[x8](https://youtu.be/7jo1MpFRJCc?t=51s)

## Cláses

![250-measures](/img/250-measures.jpg)

En algunas tiendas los productos son acomodados por tamaño los racers comúnmente
se mantienen en menores a 300mm. Esta es la distancia en diagonal de motor a motor.

- <200 (Micro)
- <300 (Mini)
- >300 (Others)

# Let us build

Construír un multirotor implica varias etapas, y es necesario tomarnos el tiempo
para hacer investigación sobre nuestro problema y las soluciones disponibles,
comprar entre plataformas comerciales o componentes individuales.

Es un **proceso iterativo**, es común que la selección de un componente limíte
las opciones en otro, ten en cuenta la combinación de piezas y la compatibilidad
entre ellas.

Para ejemplificar el proceso de construcción de un multirotor lo haremos con un
build para carreras ya que contiene las partes críticas de cualquier multirotor
y puede ser una plataforma para explorar otras posibilidades ajenas a fpv racing.

En este punto vamos a tomar unas desciciones inciales que harán más simple la
selección de componentes, nos concentraremos en quadcopters al ser la conficuración
más popular existe mucha más información, por costo y sencillez.

# Racing Componentes

En carreras la ingeniería de los crafts es bastánte accesible hoy en día, y comunmente
se empieza seleccionando un frame:

## Frame

EL chasis del build, donde colocarás todas las piezas, comúnmente fabricados de
fibra de carbono, hay muchas propuestas, desde los que favorecen el vuelo, la cámara,
la facilidad de armado, precio, etc.

Encuentra uno que apele a tus intenreses los más populares son:

### Blackout mini H
![blackout](/img/blackout.jpg)

### Lumineir QAV250
![qav250](/img/qav250.jpg)

### ZMR250 (v2)
![zmr250](/img/zmr250.jpg)

En un chasis un punto importante es el acceso a la electrónica, es común al
princio ajustar el interior y configuración de la nave, así que un acceso fácil
a los electrónicos ayuda en practicidad.

El peso y configuración debe soportar los rangos de experimentación que querramos
tener, por ejemplo, limitar el tamaño de los brazos, limitará nuestras opciones
de props, o la altura del fuselaje nuestras opciones de cámara FPV.

### Crash management (racing only)

![crashed-qav](/img/crashed-qav.jpg)

En carreras especificamente debes de pensar en el choque, y tu build debe de estar
listo para ello balanceando entre facilidad de reparación y resistencia al choque.

Prepara el quad para ser demasiado resistente a choques (sugetando con fuerza los
componentes, utilizando piezas de metal y fibra de carbono, etc.) harán el impacto
del choque más significativo en los componentes. En caso contrario si el frame es
de materiales menos rígidos y ciertas piezas son plásticas y el montado de los
componentes se hace con algún tipo de pegamento, el quad cederá al imapacto,
desarmandose en lugar de resistir y en dado caso romper algún componente.

## Power system

Engloba batería, ESC's, motores, sistema de distribución y regulación de poder.

### Motores

Existen 2 tecnologías dominantes en cuanto a motores

#### Brushed DC

![brushed-motor](/img/brushed-motor.jpg)
![brushed-diag](/img/brushed-diag.png)

La tecnología tradicional, utiliza un sistema de cepillos que alternan la polaridad
de los electromagnetos al interior del motor estos son repelidos/atraidos por los
magnetos al exterior del motor, esto genera torque y eventualmente movimiento.

Normalmente este tipo de motores puede ser conectado directamente a una fuente de
poder requieren menos electrónica para funcionar y son utilizados hoy en día en
`Micro class` por su relación peso/poder. [ref](https://www.youtube.com/watch?v=0-YXBxzKx7g)

#### Brushless (electronically commutated motors (ECM's) )

![cobra-motor](/img/cobra-motor.png)
![brushless](/img/brushless.gif)

Funcionan bajo el mismo principio de electromagnetos que switchean la polaridad
para atraer/repeler magnetos, sólo que estos no utilizan un sistema físico de
cepillos, estos necesitan un sistema de electrónica que los prenda y apague
de manera sincronizada y en orden. La prescición del controlador de velocidad es
el factor clave en este tipo de motores.

Tradicionalmente en multirotores los magnetos están montados en la campana que
rodea los electromagnetos que están controlados por el `ESC` que switchea
multiples veces por segundo su polaridad y hacen girar al arreglo de
neodimios que se encuentra a su alrededor montados en la campana que se encuentra
suspendida en un sistema de baleros.

Hay 3 factores importantes a la hora de escoger un motor:

- Tamaño, debemos encontrar motores que quepan físicamente en el frame, normalmente
por cada cláse, existen un rango de entre 1 y 5 tamaños que pueden ser compatibles
con el frame de dicho tamaño.

- Velocidad, dada en `Kv`s (las vueltas necesarias para generar 1v, Fun fact: los motores
son generadores conectados al revez), mientras más rápido el motor más pequeña
debe ser su prop. (props más grandes harán que el motor se esfuerce más en cambiar
la velocidad por la inercia del tamaño, haciendo que el motor consuma mas amperes
demandando más energía del ESC que debe de estar preparado para gobernar esa cantidad
de energía, si no lo está se quema)

- **Eficiencia, La parte esotérica de multirotores:**

### Eficiencia del motor

Cuando escoges un sistema de poder, lo que buscas es que tus motores operen con
la mayor eficiencia posible, esto es que la candidad de energía requerida por estos
sea la cantidad perfecta para levantar y mover el craft.

Tristemente es un sistema de balanzas donde al cambiar un componente o sus características
afecta al sistema completo.

El sistema es tán delicado que se ve afectado por cosas tán simples como la
altura con respecto al nivel del mar, el aire al ser más delgado afecta el desempeño
del craft. Cambiar de marca de prop, capacidad de la batería, etc.

Puedes comenzar verificando la tabla de desempeño provista por el fabricante, pero
no hay como hacer tus propias pruebas, y encontrar poco a poco la configuración
perfecta dada la situación.

Es común que en carreras el sistema de poder sea tan amable que te permita experimentar
con diferentes tipos de componentes y es aquí donde brilla la descicion de escoger
racing class como tu primer multirotor ya que el costo no es tán alto como el de
craft mas grande y su funcionamiento es el mismo.

Esto es lo que hace al hobby tán caro comprar sólo para experimentar.

### ESC's (electronic speed control)

![esc](/img/esc.png)
![esc-naked](/img/esc-naked.png)

Es una pieza de electrónica encargada de alternar la polaridad del sistema de
electromagnetos que se encuentra dentro de un motor brushless. Esto lo hace
variando la frequencia de switching the una red de transistores de efecto campo (jolines)
o `FET` que controlan la conductividad del canal, comeunmente los motores para
multirotor ocupan 3 canales.

Las caracteristicas que nos importan de un ESC es primero la cantidad de Amps que
puede gobernar y las funciones que soporta.

Los Amps está dado por los motores (podemos revisar esto en la tabla del fabricante)
debemos dejar un colchón de alrededor de 20% si los motores consumen 15Amp los
ESC's pueden ser de 18 o 20Amp.

Los ESC's corren un sistma operativo, y existen varios SimonK, BLHeli, etc. Y cási
todos soportan los features nuevos que nos interesan OneShot y Active Breaking. Es raro
que tengas que lidiar directamente con ellos, pero es importante mantenerlos al día.

## Batería

![lipo](/img/lipo.jpg)
![lipo-small](/img/lipo-small.jpg)

[Batteries](https://www.youtube.com/watch?v=CX84l5ZZHVg)
[How are they made](https://www.youtube.com/watch?v=MqywKcJ0J2M)
[How are they made 2](https://learn.sparkfun.com/tutorials/how-lithium-polymer-batteries-are-made)

La tecnología de baterias dominante en RC es LiPo (Polímero de Litio) que permite
stackear celdas para lograr mayor voltaje y mayor corriente al descargar. [ref](http://androidforums.com/threads/lithium-polymer-batteries-101.213618/)

![3s-lipo](/img/3s-lipo.jpg)

Fabricada bajo la tecnología de ion-Litio, utiliza un electrolito líquido mezclado
con un espesante plástico, lo cual permite crear un film seco y laminarlo entre
el anodo y cåtodo (aluminio cubierto de litio con cabono y placas de cobre) permitiendo
el intercambio de iones de litio (de ahí su nombre).

![lipo-unrolled](/img/lipo-unrolled.jpg)

[ref](http://www.rchelicopterfun.com/rc-lipo-batteries.html)

#EXPLODE!

## `lithium-salt`

El electrolito usado en las baterías LiPo es volátil, si en caso de daño físico,
sobrecarga o maldición los componentes internos del sandwich entran en contacto
y sucede un corto, la temepratura de la batería puede subir en cuestión de segundos
y encendiendo el electolito y estallando en llamas, la reacción es una violenta
ventilación de fuego alimentada de la química interna de la batería lo cual ocaciona
qie no pueda ser apagado al privarlo de oxigeno y el agua solo provocará que arda
más rápido. La arena puede contener la reacción hasta que esta se termine.

## PUFFY BATTERIES

![puffy-lipo](/img/puffy-lipo.jpg)

Cargar o descargar una batería por arriba de los niveles recomendados o por
algún tipo de daño físico puede calentar la mezcla interna de la batería, esto
puede llegar a generar un breakdown químico del electrólito que sucede en forma de
gas de hidrocarbono, si el breakdown ocurre en el cátodo la reacción liberará
oxigeno en su lugar. Ambos gases inflarán la batería y son señal de que claramente
hay algo mal con la quimica interna de la batería.

## Las delicadas flores de invernadero

Las baterias son la pieza mas delicada de un multirotor, dado que físicamente están
empaquetadas en un film de plástico este puede romperse muy facilmente. Y dado que
por lo regular estará volando a grandes alturas y velocidades rodeada de navajas
girando a más de 500rpm hay que tener bastánte cuidado al manejar una batería en
potencial riesgo de explosión.

Las baterias lipo funcionan mejor en cargas parciales, por eso es importante usar
un cargador especial para lipo, una celda tendrá su carga completa a 4.2v y su carga
mínima a 3.4v. Si descargamos una celda a menos de 3.3v~ corremos el riesgo de
dañarla y no poder hacer que cargue de nuevo.

Si no vas a utiilizar tus baterias por un periodo de 1 semana (polémico) es preferible
llevarlas a una `carga de storage` esto es poner cada celda alrededor de 3.8v considerado
el 50% de carga usable en una lipo, esto mantendrá la química interna en balance
lo cual permitirá cargar y descargar de manera correcta durante su vida util.

Comunmente los cargadores de LiPo tienen los seguros necesarios para detener la
carga/descarga al llegar al voltaje correcto, pero el mercado está lleno de
productos de mala calidad ya que cási todo el hardware es fabricado con muy bajos
costos así que hay que detener manualmente la carga/descarga al llegar a  3.4v
de descarga y 4.2 de carga.

Es importante utilizar ubn contenedor correcto para transportarlas, lo más práctico
es usar una bolsa para Lipos.

![lipo-bags](/img/lipo-bags.png)

## Battery rules

- Cargar a más de 4.2 cada celda
- Descargar a menos de 3.3v cada celda
- Dejar desatendida un cargador funcionando
- Usar baterias puffy
- Guardar una batería cargada
- Dejar descargadas las baterías con 3.4v por largo tiempo
- Operar con baterías muy calientes
- Operar con baterías muy frias
- Trasnportarlas sin un contenedor especial

## Los números

Cuanta energia necesitan mis motores?

![motor-current](/img/motor-current.png)

Pero será necesario hacer thrust tests para ver el desempeño real en nuestro
entorno con nuestros componentes.

Cuanta energía me da una batería

![1000-lipo](/img/1000-lipo.png)

```
1000mAh (milliAmp) = 1A (Amp)

35c índice de descarga

35 * 1 = 35Amps

35Amp / 4 = 8.75Amp disponibles para cáda motor (therefore underpowered)
```
Los motores no podrán funcionar a su máxima capacidad ya que la batería no puede
proveer suficiente amperaje.

![1300-lipo](/img/1300-lipo.png)

```
1300mAh (milliAmp) = 1.3A (Amp)

65c índice de descarga

65 * 1.3 = 84.5Amps

84.5Amp / 4 = 21.15Amp disponibles para cáda motor (therefore cool with it)
```
Debemos saber si nuestra batería puede proveer de suficiente aperaje a los motores
y así aprovechar ambos componentes de la manera más eficiente.

Por último, lás baterías suelen ser el componente más pesado del craft, por tanto
hay que considerarlas desde el principio cuando estemos decidiendo nuestros
componentes.



### Mounting options

### Reversive props

### Fuel powered

## Common Mods

Angled motors
Wider lens
Angle cameras

## Exotic stuff

Booster
Manned
Thrust only motors

Class (by size)