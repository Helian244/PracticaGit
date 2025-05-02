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
$ git init nuevo-proyecto (iniciar proyecto)  
$ cd nuevo proyecto (ubicarse en el proyecto)  
#### Para iniciar el repositorio de una carpeta ya existente:
$ cd &lt;directorio del proyecto&gt; (ubicarse en proyecto existente)  
$ git init (iniciar el repositorio)
#### ¿Cómo saber si lo hice correctamente?
Nos mostrara la rama en la que estamos en el git bash:  
![git init correcto](imagenes/2025-05-02%2017_52_33-MINGW64__g_ProyectoGit.png)
### Uso de *git --help*
Lista de comandos útiles
![git --help](<imagenes/2025-05-02 18_00_31-MINGW64__g_ProyectoGit.png>)