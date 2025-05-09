# Curso Git
# Clase 1
## ¿Qué es un controlador de versiones?
Sistema que registra los cambios en el código fuente.
### Importancia de control de versiones
- Rendimiento
- Seguridad
- Flexibilidad
## Historia
- **1990:** Nace CVS precursor de controlador de versiones
- **2005:** Creación de Git
- **2008:** Creación de Github
- **2018:** Microsoft compra Github
- **2024:** Dominación del mercado por parte de Github
## ¿Qué es Git?
Herramienta de control de versiones, siendo un sistema distribuido aloja una copia del repositorio en cada máquina local.
## ¿Qué es un repositorio?
Carpeta donde se almacenan todas las versiones del proyecto.
## Iniciando un proyecto con git
### Uso del comando *git init*
El comando nos ayuda a crear un proyecto nuevo (repositorio local).  
#### Para crear el proyecto desde 0:
***$ git init nuevo-proyecto*** (iniciar proyecto)  
***$ cd nuevo-proyecto*** (ubicarse en el proyecto)  
#### Para iniciar el repositorio de una carpeta ya existente:
***$ cd &lt;directorio del proyecto&gt;*** (ubicarse en proyecto existente)  
***$ git init*** (iniciar el repositorio)
#### ¿Cómo saber si lo hice correctamente?
Nos mostrara la rama en la que estamos en el git bash:  
![git init correcto](imagenes/2025-05-02%2017_52_33-MINGW64__g_ProyectoGit.png)
### Uso de *git --help*  
Lista de comandos útiles  
![git --help](<imagenes/2025-05-02 18_00_31-MINGW64__g_ProyectoGit.png>)
# Clase 2
## Estados de Git
### Existen 3 estados de git:
- **Modified:** El archivo se creo, elimino o ha sido cambiado, este no tiene los cambios confirmados. 
- **Staged:** El archivo se marco como preparado para ser confirmado por el repositorio local.
- **Committed:** El archivo se graba en el repositorio local.
## Staging Area
Cuando añadimos archivos al repositorio local o modificamos los ya existentes, y queremos guardarlo, el primer paso es llevarlos a la staging area, un sector que nos permite confirmar los cambios que realizamos en el repositorio local.  
### ¿Cómo llevar mis cambios a la staging area?
Usamos el siguiente comando, para cada archivo que deseemos añadir a la staging area:  
***$ git add &lt;file name&gt;***  
Si queremos llevar todos los cambios producidos:  
***$ git add .***  
### *Git restore --staged &lt;file name&gt;* 
Nos ayuda a remover un archivo de la staging area.
## Commit y su importancia
Registra los cambios producidos en el repositorio  
Al tener la perspectiva de fotografías tenemos que:  
![commit como fotografía](<imagenes/2025-05-03 12_15_42-(667) Clase de Git_GitHub- Scesi - 2 - YouTube.png>)  
Tenemos un punto de restauración si es que nos equivocamos.
### Usando el commit
Para guardar los cambios de la staging area hacemos un commit con el siguiente comando:  
***$ git commit***  
Para añadir un mensaje al commit usamos:  
***$ git commit -m*** *"Mensaje descriptivo del commit"*  
Estos cambios se guardaran en el repositorio local hasta hacer nuevamente un commit con otros cambios.   
### Ver los commits que realize
Usamos el comando:  
***$ git log***  
El cual nos permite ver un registro de los commits que se realizaron hasta el momento.  
![git log](<imagenes/2025-05-06 19_31_31-MINGW64__g_ProyectoGit.png>)  
***$ git log --online*** nos muestra solo los mensajes de commits.  
![git log --oneline](<imagenes/2025-05-06 19_35_29-MINGW64__g_ProyectoGit.png>)  
### ***$ git commit --amend -m*** *"Nuevo mensaje de commit"*
Nos ayuda a "sustituir" el mensaje del ultimo commit realizado, considerar que "cambia" el identificador del ultimo commit.
## ¿HEAD qué es?
Es el puntero de referencia que nos indica el lugar actual en el que estamos dentro del repositorio.  
![HEAD](<imagenes/2025-05-06 19_59_44-● ApuntesDeClase.md - ProyectoGit - Visual Studio Code.png>)
## ¿Qué es una rama?
Bifurcación del punto actual en el que nos encontramos.  
Técnicamente es un nuevo apuntador hacia un commit distinto.  
![Branch](<imagenes/2025-05-06 20_06_27-Clase de Git_GitHub- Scesi - 2 - YouTube.png>)
### Propósito de las ramas
Permite el desarrollo colaborativo y no lineal.
### Creando una nueva rama
***$ git branch &lt;nombre de la rama&gt;***
### Cambiar de rama
***$ git checkout &lt;nombre de la rama&gt;***  
o  
***$ git switch &lt;nombre de la rama&gt;***  
También tenemos que para cambiar constantemente entre 2 ramas, una rama previa:  
***$ git switch -***  
### Para hacer los 2 anteriores pasos a la vez
***$ git switch -c &lt;nombre de la rama&gt;***  

Considerar que al crear una nueva rama esta tendrá los cambios del ultimo commit que se hicieron.  
Considerar que las ramas serán visibles en el ultimo commit que se hicieron  
![PUNTERO](<imagenes/2025-05-06 20_31_30-ApuntesDeClase.md - ProyectoGit - Visual Studio Code.png>)  
# Clase 3
## Ramas
### Fusión de ramas
Las bifurcaciones tienen 2 destinos: El olvido o la fusion con otra rama.  
Al decir fusión nos referimos a la integración de cambios de una rama a otra, para que los cambios de una rama se asimilen con otra rama.
#### ***$ git merge &lt;nombre de la rama&gt;***  
Usamos este comando para incorporar cambios de otra rama en la que estamos actualmente.  
![git merge](<imagenes/2025-05-08 18_51_31-Clase de Git_GitHub- Scesi - 3 - YouTube.png>)  
Al hacer ***git merge*** por defecto se hace un nuevo commit con todos los cambios de la rama de origen a la rama actual.
#### Otros comandos útiles:
***$ git merge &lt;nombre de la rama&gt; --edit :*** Abre un editor antes de hacer commit  
***$ git merge &lt;nombre de la rama&gt; --no--commit :*** Evita que se realize un commit automáticamente.  
***$ git merge &lt;nombre de la rama&gt; --no-ff :*** Evita que se realize un fast forward y fuerza el commit de merge de ramas.  
### Eliminación de ramas
La razón principal es que es una buena practica, las ramas tienen un tiempo de vida acorde a la realización de su objetivo.
#### Comando: ***$ git branch --delete &lt;nombre de la rama&gt;*** 
Usamos este comando para eliminar ramas sueltas y que ya cumplieron su propósito (o unirse a otra rama), también podemos abreviar el comando con:  
***$ git branch -d &lt;nombre de la rama&gt;***  
Si la rama ya hizo merge con otra no habrá problema, sin embargo si no ocurrió esto ultimo nos devolverá un error:  
Podemos forzar la eliminación usando el siguiente comando:  
***$ git branch -D &lt;nombre de la rama&gt;***  
### ***$ git rebase &lt;nombre de la rama objetivo&gt;***
Rebase es un comando que nos ayuda a reubicar la secuencia de commits de la rama actual a una rama objetivo para reescribir el historial de commits.
### Conflictos en Git
Suceden cuando queremos fusionar cambios en las mismas lineas de un fichero de diferentes ramas, esto se da ya que Git no sabe que cambio prevalecerá en la fusion y nos pedirá que resolvamos este.  
![Conflictos](<imagenes/2025-05-09 09_11_08-Clase de Git_GitHub- Scesi - 3 - YouTube.png>)