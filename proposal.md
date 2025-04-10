# Propuesta TP DSW

## Grupo
### Integrantes
* 52867 - Mazalan, Ariel Ignacio
* 52831 - Pacheco, Santiago Tomas
* 52309 - Ribotta, Tomas Nicolas

### Repositorios
* [frontend app](https://github.com/TomasRibotta20/FrontEnd_fantasy)
* [backend app](https://github.com/TomasRibotta20/BackEnd_Fantasy)


## Tema
### Descripción

Una aplicacion web de "Fantasy Fubtol" en la cual cada usuario puede construir su propio equipo de 11 jugadores adquiridos desde un mercado basado en la Liga Argentina de Fubtol y afiliarse a una liga con otros usuarios. Estos jugadores iran sumando puntos semanalmente en funcion de su rendimiento en la vida real, que luego seran usados para determinar que usuario conformo el mejor equipo. Cada usuario comenzara con 11 jugadores al azar (que no excedan un market cap especifico) y un pequeño presupuesto. Cada jugador tiene un precio establecido el cual variaria dependiendo de sus ultimas actuaciones en partidos oficiales y tambien dependiendo de su demanda en el mercado. Los usuarios pueden adquirir estos jugadores en un mercado que se actualizara diariamente con jugadores aleatorios, tambien pueden comprarselos a otros usuarios pagando una clausula de rescision. Sumado a esto cada usuario puede vender sus jugadores en el mercado al precio que el mismo tenga en el momento. Al final de la semana se conformara un podio entre los usuarios de una misma liga dependiendo de la cantidad de puntos que tengan, y en base a ese podio se repartiran los distintos premios (diferentes sumas de dinero para la mejora del equipo).

### Modelo
![imagen del modelo](ModeloDeDominioV2Final.png)


## Alcance Funcional 

### Alcance Mínimo

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Usuario<br>2. CRUD Club<br>3. CRUD Posición|
|CRUD dependiente|1. CRUD Equipo {depende de} CRUD Usuario y CRUD Jugador<br>2. CRUD Jugador {depende de} CRUD Posisción y CRUD Club|
|Listado<br>+<br>detalle| 1. Listado de jugadores filtrado por club, muestra jugadores del club y posición del jugador => detalle muestra datos completos de jugador<br> 2. Listado de jugadores filtrado por posición, muestra nombre del jugador y equipo => detalle muestra datos completos de cada jugador|
|CUU/Epic|1. Modificar equipo<br>2. Calcular puntaje para cada jugador|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Usuario<br>2. CRUD Club<br>3. CRUD Posición<br>4. CRUD Equipo<br>5. CRUD Jugador<br>6. CRUD Precio<br>7. CRUD País<br>8. CRUD Jornada<br>9. CRUD Torneo<br>10. CRUD Partido<br>11. CRUD Mercado<br>12. CRUD Liga<br>13. CRUD Podio|
|CUU/Epic|1. Calcular puntaje para cada jugador<br>2. Crear torneo<br>3. Modificar equipo|

### Alcance Adicional Voluntario

|Req|Detalle|
|:-|:-|
|Listados |1. Listados de jugadores filtrados por precio, país, posición y equipo<br>2. Listado de usuarios de un torneo filtrado por jornadas|
|CUU/Epic|1. Realizar el login del usuario<br>2. Realizar transacción (Comprar/vender juador a otro usuario de ese torneo o al mercado)<br>3. Generar mercado diario<br>4. Asignar los premios a los jugadores<br>5. Modificar clausula de un jugador|


