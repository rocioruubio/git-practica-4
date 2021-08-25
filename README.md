# git-practica-2
Segunda práctica de git

Para esta segunda práctica vamos a hacer algunos merges que tendrán conflictos. Es decir, git no será capaz de resolver por sí solo los conflictos entre los cambios de dos ramas y tendremos que resolverlos nosotros. 

Una forma de hacerlo es via consola, pero tal y como habréis podido comprobar github nos obliga a introducir la contraseña cada dos por tres. Esto se debe al protocolo de seguridad que utiliza github, que es independiente de la herramienta git. 

Para resolver los conflictos se puede realizar por consola (os dejo la info más abajo) pero en nuestro caso los resolveremos con las herramientas visuales que nos proporciona IntelliJ. 

## Importar proyecto y añadir token a IntelliJ

En el primer uso del repositorio, nos pedirá un token para autorizar al IDE a acceder al repo. Para crear el token, vamos a las “Settings” de nuestro perfil de GitHub, pulsamos sobre “Developer Settings” -> “Personal access tokens”. En la siguiente ventana, le damos un nombre que lo identifique, elegimos el scope “repo” y pulsamos sobre “Generate token”.

Una vez generado el token, volviendo a IntelliJ, lo pegamos en el diálogo en el que nos quedamos y, si todo ha ido ok, veremos como nos sincroniza nuestra config y podremos ver el commit en el repositorio.

Según la versión de IntelliJ puede que el propio IntelliJ te solicite acceso a github para crear el token.

## Ejemplos guiados y explicados de merges y resolución de conflictos por consola
No es necesario que hagáis por consola. Al menos para estas pruebas. Pero será interesante que le deis un vistazo a los siguientes enlaces ya que os serán de utilidad.

### Merges

  https://www.atlassian.com/es/git/tutorials/using-branches/git-merge
  
### Conflictos

  https://www.atlassian.com/es/git/tutorials/using-branches/merge-conflicts

