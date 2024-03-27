## Estructura del proyecto
link = https://www.youtube.com/watch?v=7vHzVN0EiQc&list=LL&index=23&t=2434s
En el POM.XML tiene todas als dependencias (Librerias) de Maven.
Version de Java, Pacacking;

src: // Codigo fuente
    - main //Codigo de proyecto
        -resources //Archivos de configuracion,HTML
            -static // Archivos publicos (Frontentd)
                -index.html
            -templates
            aplication.propierties // archivo de configuracion
        -java // Codigo fuente
    - test // Testing

Anotaciones:
    @Nombre
Indica funcionalidad

Para iniciar servidor, hay que ir a Maven.
nombre del proyecto / Plugins / spring-boot
y ahi estan los script par ejecutar

Si no esta en la version de java.
Ir al POM.XML y cambiar version de java por la quie aparece en java --version

File < Project Structure
Puedes agregar SDK, lo instala automaicamente

Si ya hay una aplicacion corriendo en el puerto 8080, hay que matarla

window: netstat -ano | findstr LISTENING | findstr 8080
linux: sudo netstat -anp | grep ':8080'
sudo kill -9 {id}

Controladores:
Sirven para manejar direcciones url
@RestController
public class UsuarioController {
    @RequestMapping(value = "prueba")
    public String prueba(){
        return "prueba";
}

Mediante las etiquetas defino objetos y metodos del framework

Plantilla para DB:
sb-admin-2

Para poder limpiar el cache, ejecuto el script de clean

### JSON XML
Se utiliza para comunicarse los servicios web (servicios).
Un servidor le hace una peticion a otro servidor y le retorna JSON o XML

### XML
~~~XML
<example>
    <atributo1>
        <atributo2>
        </atributo2>
    </atributo1>
    <atributo2>
    </atributo2>
</example>
~~~

### JSON
~~~JSON
[
  {
    "objeto": "dato",
    "objeto2": {
      "atributo1": "data",
      "atributo2": "stringSiempre"
    }
  
  }
]
~~~
JSON se utiliza mas porque pesa muchisimo menos, no usa espacios.

### Estructura de una URL y los metodos HTTP
#### Estructura de un link:

#### Ejemplo 

LINK:   https://waytolearnx.com/author/anime-kuis.html#posts

URL:https://waytolearnx.com/author/anime-kuis.html
URN: waytolearnx.com/author/anime-kuis.html#posts
URI:https://waytolearnx.com/author/anime-kuis.html#posts
Method/Esquema: https
Dominio: waytolearnx.com
Path/Ruta: /author/ (Categoria)
Elemento: anime-kuis.html#posts
Location: anime-kuis.html
Recurso: #posts

#### Otro ejemplo

URI: http://usuario:contrasenia@jarroba.com:80/articulos/unartiuclo/?id=123&busqueda=java#comment-12345

Scheme: http://
Authority: usuario:contrasenia@jarroba.com:80
    Authentication: usuario:contrasenia@
    Host: jarroba.com
    Port: :80
Path: /articulos/unarticulo/
    Seccion: /articulos/
    Subseccion: /unarticulo/
Query: ?/id=123&busqueda=java
    clave1,valor1 : id=123
    clave2,valor2 : busqueda=java
Fragment: #comment-12345

### Metodos HTTP:
- GET - CONSULTAR (Este pasa mediante la URL)
- POST - CREAR
- PUT - MODIFICAR
- PATCH - MODIFICAR (Pequenias modificaciones en una entidad)
- DELETE - ELIMINAR
- CONNECT,OPTIONS,TRACE,HEAD

Servidores antiguos solo usan GET y POST

### Arquitecturas MVC - REST
#### MVC - Modelo Vista Controlador
La estructura tiene diferentes capas:
- Controlador: se ocupa de recibir la peticion del cliente y la procesa
- Modelo: El modelo se ocupa de hacer consultas a las bases de datos
- Vista: genera el html para retornano al controlador y por ultimo al cliente

#### REST
No retorna HTML si no mas bien JSON
La peticion no se hace mediante un navegador web, si no mediante AJAX (JS asincronico)

REST es mucho mejor, ya que reotrna JSON, y al querer migrar la aplicacion o utilizarla es mas sencillo leer un JSON que un HTML

MVC es mas anitguo que REST.

Estructura:
- Controlador: recibe peticion AJAX/Fetch y deriba la consulta a la capa de Servicio
- Servicio: Logica del programa - Se comunica con Controlador y Repository
- Repository: Logica sobre Base de Datos - Se comunica con Servicio, Modelo y Base de Datos
- Modelo: solo guarda informacion de las entidades

### Frameworks que utilizan Arquitecturas de software
