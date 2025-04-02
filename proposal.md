# Propuesta TP DSW

## Grupo
### Integrantes
* 52867 - Mazalan, Ariel Ignacio
* 52831 - Pacheco, Santiago Tomas
* 52309 - Ribotta, Tomas Nicolas

### Repositorios
* [frontend app](http://hyperlinkToGihubOrGitlab)
* [backend app](http://hyperlinkToGihubOrGitlab)


## Tema
### Descripción

Una aplicacion web de "Fantasy Fubtol" en la cual cada usuario puede construir su propio equipo de 11 jugadores adquiridos desde un mercado basado en la Liga Argentina de Fubtol y afiliarse a una liga con otros usuarios. Estos jugadores iran sumando puntos semanalmente en funcion de su rendimiento en la vida real, que luego seran usados para determinar que usuario conformo el mejor equipo. Cada usuario comenzara con 11 jugadores al azar (que no excedan un market cap especifico) y un pequeño presupuesto. Cada jugador tiene un precio establecido el cual variaria dependiendo de sus ultimas actuaciones en partidos oficiales y tambien dependiendo de su demanda en el mercado. Los usuarios pueden adquirir estos jugadores en un mercado que se actualizara diariamente con jugadores aleatorios, tambien pueden comprarselos a otros usuarios pagando una clausula de rescision. Sumado a esto cada usuario puede vender sus jugadores en el mercado al precio que el mismo tenga en el momento. Al final de la semana se conformara un podio entre los usuarios de una misma liga dependiendo de la cantidad de puntos que tengan, y en base a ese podio se repartiran los distintos premios (diferentes sumas de dinero para la mejora del equipo).

### Modelo
![imagen del modelo]()

*Nota*: incluir un link con la imagen de un modelo, puede ser modelo de dominio, diagrama de clases, DER. Si lo prefieren pueden utilizar diagramas con [Mermaid](https://mermaid.js.org) en lugar de imágenes.

## Alcance Funcional 

### Alcance Mínimo

*Nota*: el siguiente es un ejemplo para un grupo de 3 integrantes para un sistema de hotel. El 

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Tipo Habitacion<br>2. CRUD Servicio<br>3. CRUD Localidad|
|CRUD dependiente|1. CRUD Habitación {depende de} CRUD Tipo Habitacion<br>2. CRUD Cliente {depende de} CRUD Localidad|
|Listado<br>+<br>detalle| 1. Listado de habitaciones filtrado por tipo de habitación, muestra nro y tipo de habitación => detalle CRUD Habitacion<br> 2. Listado de reservas filtrado por rango de fecha, muestra nro de habitación, fecha inicio y fin estadía, estado y nombre del cliente => detalle muestra datos completos de la reserva y del cliente|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Tipo Habitacion<br>2. CRUD Servicio<br>3. CRUD Localidad<br>4. CRUD Provincia<br>5. CRUD Habitación<br>6. CRUD Empleado<br>7. CRUD Cliente|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva<br>3. Realizar el check-out y facturación de estadía y servicios|


### Alcance Adicional Voluntario

*Nota*: El Alcance Adicional Voluntario es opcional, pero ayuda a que la funcionalidad del sistema esté completa y será considerado en la nota en función de su complejidad y esfuerzo.

|Req|Detalle|
|:-|:-|
|Listados |1. Estadía del día filtrado por fecha muestra, cliente, habitaciones y estado <br>2. Reservas filtradas por cliente muestra datos del cliente y de cada reserve fechas, estado cantidad de habitaciones y huespedes|
|CUU/Epic|1. Consumir servicios<br>2. Cancelación de reserva|
|Otros|1. Envío de recordatorio de reserva por email|

