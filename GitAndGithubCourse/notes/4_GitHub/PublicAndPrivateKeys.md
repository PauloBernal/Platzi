# Llaves públicas y privadas

Uno de los problemas más grandes al momento de navegar por internet es la seguridad. Se crearon múltiples protocolos de cifrado para permitir que las conexiones sean seguras (como contraseñas), pero estas tienen un problema muy grande el cuál es enviar dicha contraseña de cifrado a otra persona para descifrar información. Es así que como una solución se crearon las llaves públicas y privadas (también se denominan cifrado asimétrico de un solo camino )


## ¿Como funcionan las llaves públicas y privadas?

Cuando uno quiere recibir un mensaje crea algo llamado llave pública y otra llamada llave privada. Las llaves se vinculan matemáticamente y lo que se cifre con la llave pública solamente se puede descifrar con la llave privada. Se le envía al otro usuario la llave pública, este crea una copia una versión personal de la misma y con esa cifra el mensaje que se quiere enviar. No importa que alguien intercepte la llave pública, ya que lo necesariamente importante para descifrar el mensaje es la llave privada que se creo junto a la llave pública (por esto NUNCA se debe compartir la llave privada con alguien)

## Configurando una llave pública y una llave privada con GitHub

Cuando uno crea un repositorio remoto introduce su usuario y contraseña para acceder a él. Sin embargo la seguridad no deja de ser un problema ya que si alguien accede a tu equipo el repositorio es vulnerable a password cracking y el posterior acceso a un proyecto, una forma muy común de hacer caer proyectos y sitios web completos. Para esto es necesario añadir una capa de seguridad mayor, donde entran las llaves públicas y privadas. Se crea una llave pública y se la envía a GitHub, mientras se mantiene en el equipo la llave privada, a la cual se le puede agregar una contraseña para incrementar la seguridad. Se conecta el repositorio local con el remoto por medio de un protocolo llamado SSH (Secure Shell), un protocolo de conexión seguro. Al enviar la llave pública a GitHub este automáticamente envía al usuario su llave pública cifada con la llave pública que se le envió. Gracias a esto hay una conexión de doble camino segura. Es importante saber que las llaves no son por repositorio ni por proyecto, sino por persona.

### Generar llaves

Se debe estar posicionado en el directorio del usuario (En linux está como `/home/username` y en Windows en `C://Usuarios/username`) por cuestión de buenas prácticas, aunque se puede estar posicionado en cualquier directorio. Se debe tener en cuenta que el email con el que se configuró Git debe ser el mismo con el que se creó la cuenta de GitHub antes de generar las llaves. Para generar las llaves se utiliza el comando
~~~
$ ssh-keygen -t rsa -b 4096 -C "example@email.dom"
~~~
Desglosando el comando esto sería `ssh-keygen` el comando para generar llaves ssh, `-t rsa` es para elegir el algoritmo a usar al momento de generar las llaves `-b 4096` es la complejidad de la llave y `-C "example@email.dom"` es para configurar a qué correo electrónico están ligadas las llaves ssh. Al colocar el comando se nos pide rellenar unas cuantas opciones:

- Ruta.- Se nos pide especificar en que directorio se almacenarán las llaves. Si no se coloca ninguno por defecto se almacenará en el directorio actual

- Passphrase.- Es una contraseña de texto que se coloca para brindar mayor seguridad a nuestras llaves. Después de colocarlo se nos pedirá confirmar la contraseña. Si no se coloca nada por defecto las llaves no tendrán protección extra

Con esto se muestra en pantalla el fingerprint de la llave al igual que un randomart para verificar que la llave es correcta (estos también se pueden usar como llaves públicas).

### Configurando llaves en el equipo local

#### Windows y Linux

Se debe ver que el programa de las llaves ssh esté corriendo coreectamente. Para esto se corre el comando:
~~~
$ eval $(ssh-agent -s)
~~~
Si es correcto debe aparecer una salida con un pid (Process ID) que significa que el programa se está ejecutando. Una vez hecho esto hay que dirigirse al directorio en el que se iniciaron las llaves e ingresar al directorio `.ssh`. Hay que añadir la llave privada al entorno con el comando
~~~
$ ssh-add ~/.ssh/id_rsa
~~~

#### Mac

Se debe ver que el programa de las llaves ssh esté corriendo coreectamente. Para esto se corre el comando:
~~~
$ eval $"(ssh-agent -s)"
~~~
Si es correcto debe aparecer una salida con un pid (Process ID) que significa que el programa se está ejecutando. Una vez hecho esto hay que dirigirse al directorio en el que se iniciaron las llaves e ingresar al directorio `.ssh`. Una vez en el directorio se debe crear un archivo llamado `config` (si es que no existe) y dentro colocar las siguientes configuraciones:
~~~
Host *
  AddKeystoAgent yes
  UseKeychain yes
  Identityfile ~/.ssh/id_rsa
~~~
Se debe guardar el archivo y volver al home. En el home se debe ejecutar el siguiente comando para añadir la llave privada al entorno:
~~~
$ ssh-add -K ~/.ssh/id_rsa
~~~

### Conexión a Github con SSH

Se debe ir a la cuenta de GitHub y una vez ahí acceder a configuraciones (Settings). En configuraciones debe haber una opción llamada 'SSH and GPG Keys', a la cuál se debe entrar. Ahí se añadirá el título de la llave pública y la llave, que deberá ser copiada del archivo `id_rsa` en el directorio `.ssh`. Una vez configurada la llave pública se debe ir a un repositorio y ahí a la sección de 'Clone or download'. Ahí hay una opción llamada 'SSH' o 'Use SSH' y se debe copiar la url. Para añadir el repositorio remoto con SSH se debe utilizar el comando:
~~~
$ git remote add url_ssh
~~~
Si ya se tenía un repositorio remoto configurado se puede cambiar la url de este. Para ver los repositorios remotos de forma detallada (con url) se puede utilizar el comando:
~~~
$ git remote -v
~~~
Para cambiar la url del repositorio existe un comando llamado `remote set-url`:
~~~
$ git remote set_url remote_repo_name <new_url>
~~~
Una vez hecho esto ya permite enviar cambios al repositorio por medio del protocolo SSH. 
