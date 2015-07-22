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

# Let us build

Construír un multirotor implica varias etapas, y es necesario tomarnos el tiempo
para hacer investigación sobre nuestro problema y las soluciones disponibles,
comprar entre plataformas comerciales o componentes individuales.

Es un **proceso iterativo**, es común que la selección de un componente limíte
las opciones en otro, ten en cuenta la combinación de piezas y la compatibilidad
entre ellas.

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

### Crash management (only racing)


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