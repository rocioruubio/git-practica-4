# git-practica-2
Segunda práctica de git. Configurar IntelliJ y hacer algunos merges con conflictos.

Para esta segunda práctica vamos a hacer algunos merges que tendrán conflictos. Es decir, git no será capaz de resolver por sí solo los conflictos entre los cambios de dos ramas y tendremos que resolverlos nosotros. 

Una forma de hacerlo es via consola, pero tal y como habréis podido comprobar github nos obliga a introducir la contraseña cada dos por tres. Esto se debe al protocolo de seguridad que utiliza github, que es independiente de la herramienta git. 

Para resolver los conflictos se puede realizar por consola (os dejo la info más abajo) pero en nuestro caso los resolveremos con las herramientas visuales que nos proporciona IntelliJ. 

## Merges y resolución de conflictos por consola
No es necesario que hagáis por consola. Al menos para estas pruebas. Pero será interesante que le deis un vistazo a los siguientes enlaces ya que os serán de utilidad.

### Merges

  https://www.atlassian.com/es/git/tutorials/using-branches/git-merge
  
### Conflictos

  https://www.atlassian.com/es/git/tutorials/using-branches/merge-conflicts


## Configurar IntelliJ para usar Git

Abrimos IntelliJ y vamos a Archivo -> Configuración  -> Control de versiones -> Git

Con atajo de teclado sería  Ctrl + Shift + s (Archivo -> Configuración) -> Control de versiones -> Git

Añadimos la Ruta al ejecutable de Git, seleccione el archivo git.exe instalado, haga clic en Prueba, la configuración de prueba debería ser exitosa.

Ahora veremos que tenemos un menú especial en IntelliJ dedicado solo a Git con un montón de opciones.

## Configurar GitHub en IntelliJ
Configure GitHub en IDEA, Archivo -> Configuración-> Control de versiones -> GibHub

　　Host：github.com

Token: haga clic en Crear token API, ingrese el nombre de usuario y la contraseña registrados en github para generar el token

Haga clic en Probar para probar si la conexión es exitosa.

Si no tenemos configurado el token en el primer uso del repositorio, nos pedirá un token para autorizar al IDE a acceder al repo. Para crear el token, vamos a las “Settings” de nuestro perfil de GitHub, pulsamos sobre “Developer Settings” -> “Personal access tokens”. En la siguiente ventana, le damos un nombre que lo identifique, elegimos el scope “repo” y pulsamos sobre “Generate token”.

Una vez generado el token, volviendo a IntelliJ, lo pegamos en el diálogo en el que nos quedamos y, si todo ha ido ok, veremos como nos sincroniza nuestra config y podremos ver el commit en el repositorio.

Estas configuraciones no tendremos que voler a hacerlas con ningún repositorio de nuestra cuenta.

## Ejemplo workflow de ramas 

En el siguiente gráfico veremos cómo desarrollar creando ramas según el workflow git flow

![workflow](./git_flow.jpg)

De la rama develop salen y se fusionan las ramas de las mejoras a implementar y las ramas de preparación de código a producción release-. Cuando hay un error en producción a corregir, crearemos una rama hotfix- que saldrá y se fusionará en master para desplegar a producción y en develop para continuar desarrollando las nuevas funcionalidades sin bugs.

Extension para automatizar GIT flow. https://github.com/nvie/gitflow. Ofrece comandos para facilitar la creacion de features, hotfix, etc…

En cuanto a los TAGS digamos que son marcas para encontrar más fácilmente ciertos momentos de un proyecto como puede ser una Release o un cambio importante a remarcar.

## Haz un fork del repositorio creado para la práctica 2 del taller
- Haz el fork de este proyecto
- Clona el proyecto (puedes hacerlo por consola o IntelliJ)
- Crea una rama nueva desde IntelliJ
  - Git -> Branches -> New branch -> le asignamos un nombre a nuestra nueva rama "develop"
  - Añade un fichero clientes.sql que tenga lo siguiente

   ```sql
      create table clientes(
         id int primary key auto_increment,
         nombre varchar(50),
         apellidos varchar(50),
         edad int,
         direccion varchar(50)
      );
   ```


