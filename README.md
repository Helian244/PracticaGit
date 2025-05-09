# Clase 4
## GitHub
GitHub no es lo mismo que Git, GitHub es un servicio de alojamiento en la nube basado en Git y Git es el controlador de versiones.  
### ¿GitHub como único servicio?
No, existen mas servicios como Bitbucket, GitLab.
## Repositorios remotos
Son repositorios alojados en un servidor y estará sujeto a sincronización con el repositorio local.
## Características que ofrece GitHub
### Mi Perfil y mis repositorios
Estadísticas, contribuciones que hacemos a nuestros y otros repositorios.  
Visualización de la cantidad de repositorios propios (tienen un limite) y en los que participamos.
### Buscar otros perfiles y repositorios
Podemos ver las estadísticas de otros perfiles, su actividad, sus repositorios públicos, organizaciones a las que pertenece.
### Proyectos
Herramientas de gestión de proyectos, flujos de trabajo, creación y asignación de tareas a integrantes del proyecto.
### Repositorio > Actions
Nos ayuda con DevOps, deployment del repositorio, la seguridad, integración continua.  
Nos permite automatizar gran parte y diferentes areas del repositorio
### Organizaciones
Nos permiten tener una comunidad que comparte repositorios propios de la organización.
## Enlazar un repositorio local con uno remoto
Usamos el siguiente comando en git bash:  
***$ git remote add \<alias>*** (usualmente el alias es "origin") ***\<url del repositorio remoto>***
### Generar llaves SSH
Las llaves se usan para autenticar la identidad de un contribuyente, evitan las suplantaciones de identidad.  
#### Pasos:
Listado de nuestras llaves:  
***$ ls -al ~/.ssh***  
Crear llave SSH:  
***ssh-keygen -t rsa -b 4096 -C "tu.email@email.com "***  
***press enter***  
***passphrase***  
Poner en marcha la llave:  
***eval "$(ssh-agent -s)"***  
Añadir la llave:  
***ssh-add ~/.ssh/id_rsa***  
Copia en portapapeles:  
***clip < ~/.ssh/id_rsa.pub***  
Pegar en seccion "key":  
***https://github.com/settings/ssh/new***  