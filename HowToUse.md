## Cómo Utilizarlo por Primera Vez (Versión Regularidad)

1.  Entrar a la carpeta de la proposal, ahí encontrarás ambos links para el repositorio de backend como el de frontend. Dentro de cada uno de los repositorios, en la sección de *releases*, habrá una llamada **Lanzamiento para regularidad**. Descargar esa versión de cada uno de los repositorios.

2.  Dentro del repositorio de backend, en una carpeta llamada `db`, encontrarás un archivo `.txt` llamado `docker run`. Es recomendable descargarlo y ejecutarlo en Docker para crear la *run* necesaria en el puerto en el cual está en el código del proyecto. Otra opción es cambiar las credenciales de conexión a la base de datos dentro del proyecto de backend en la siguiente dirección: `shared/db/orm.ts`.

3.  Luego, dentro del repositorio del backend, habrá una carpeta llamada `db`. De ahí, descargar el archivo `.sql` con el nombre `db_DSW_Regularidad`. Primeramente ejecutar el comando `pnpm run db:update` con la base de datos encendida para poder generar las tablas necesarias y luego ejecutar el .sql en MySQL Workbench, ya que en este están precargados los datos necesarios para el correcto funcionamiento de la aplicación.

4.  Una vez con el backend y el frontend descargados, realizar un `pnpm install` en ambos para descargar las dependencias necesarias en el proyecto.

5. La aplicacion utiliza una API externa para obtener los datos de los partidos. Para utilizarla debemos: <br>
###  Obtener clave de API-Sports
1. Regístrate en [API-Football](https://www.api-football.com/)
2. Obtén tu clave API gratuita
3. Crear un archivo .env que contenga las siguientes lineas<br>APISPORTS_KEY=Pega_AQUI_TU_CLAVE<br>AFA_LEAGUE_ID=128<br>AFA_SEASON=2021

**Nota sobre límites del plan gratuito:**
- 100 peticiones por día
- 10 peticiones por minuto
- El código ya implementa rate limiting automático

6.  Correr el backend con el comando `pnpm run start:dev` y el frontend con el comando `pnpm run dev` al mismo tiempo. Realizando esto, se le abrirá en un navegador la página principal del login en el puerto `5173`. A partir de aquí podrá realizar lo que desee,hay ciertas recomendaciones indicadas abajo.

---

## Recomendaciones de Uso (Versión Regularidad)

### Si deseas loguearte como Administrador

Utilizar las siguientes credenciales:
> **Email:** `admin@admin.com`
> **Contraseña:** `admin123`

Dentro de la aplicación ya van a estar precargados los datos de los partidos, jornadas,clubes y jugadores, y va a estar preseteada como jornada activa la jornada 1. Dentro del lado de administrador podrás acceder a todos los CRUDs disponibles, así como al control de jornadas donde podrás elegir la jornada que está activa, habilitar y deshabilitar las modificaciones (lo cual permite o no que los usuarios puedan cambiar su equipo) y procesar jornadas (lo cual trae todos los datos para una jornada de cada uno de los jugadores que participaron de una API externa y calcula los puntajes para cada uno).

### Para loguearte como Usuario

Realizar el registro a través de la aplicación y luego hacer un login con las credenciales introducidas previamente.

Dentro del lado del usuario, lo primero que debemos realizar es darle un nombre a nuestro equipo y se creará un equipo aleatoriamente con 11 jugadores titulares y 4 suplentes. Luego, en nuestra sección de **Mi Equipo**, podremos modificar la alineación y jugadores a nuestro gusto, clickeando un jugador y cambiándolo por un suplente o por algún jugador obtenido a través del listado de jugadores con filtro que aparece en la pantalla. Luego, podremos también en la sección **Jornadas** ver el resultado de nuestro equipo en las jornadas en las que participó (es decir, en las jornadas donde ya existía el equipo antes de que el administrador procesara los datos de la misma).

### Flujo Básico

Crear varios usuarios, uno por cada amigo que quiera jugar, y elegir los jugadores para que jueguen esa jornada. Luego, antes de que la jornada comience en la vida real, el que ejecute el rol de administrador deberá deshabilitar las modificaciones. Una vez la jornada en la vida real terminó, el admin deberá procesar la jornada (lo cual tarda bastante tiempo por el número de peticiones que se pueden realizar a la API por minuto) y luego volver a habilitar las modificaciones.

Luego, del lado del usuario, cada una de las personas participantes podrán ver sus puntuaciones, comparar quién obtuvo mayor puntaje y prepararse para la siguiente jornada.


