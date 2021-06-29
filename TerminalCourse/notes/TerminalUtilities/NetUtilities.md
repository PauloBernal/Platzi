# Utilidades de red
Son usos que se le puede dar a la terminal al momento de determinar la estabilidad de una red, si se puede conectar a un sitio web, etc.

## Comandos Útiles
- `ifconfig`.- Este comando muestra características y configuración de la red.
~~~
$ ifconfig
~~~
- `ping`.- Este comando envía y recibe paquetes de bytes para ver el tiempo de respuesta de una dirección ya sea una IP de red o un sitio web.
~~~
$ ping www.domain.dom
~~~
- `curl`.- Este comando trae un archivo de texto (html, markdown, csv, etc) de la ruta o sitio web especificados.
~~~
$ curl www.domain.dom
~~~
- `wget`(web get).- Este comando trae un archivo desde internet de forma similar a `curl`, sin embargo, en este caso descarga sirectamente el archivo.
~~~
$ wget www.domain.dom
~~~
- `traceroute`.- Este comando es interesante debido a que traza la ruta de las direcciones IP por las que pasa la información para llegar hasta nosotros.
~~~
$ traceroute www.domain.dom
~~~
- `netstat`.- Con el flag `i` muestra todos los dispositivos a los que se puede conectar.
~~~
$ netstat -i
~~~

---

[Anterior](./EditorInTerminal.md)

[Siguiente](./ProcessManagement.md)

[Índice del curso](../Index.md)
