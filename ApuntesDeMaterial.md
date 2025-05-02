# Apuntes del material 
## Capitulo 1: Introducción a Github
### ¿Qué es Github?
Herramienta de control de versiones, que nos ayuda visualizar los cambios producidos en un repositorio.
### Fundamentos de Git
- **Repositorios:** Carpeta que almacena diferentes versiones, mantienen al tanto el historial de cambios, estos pueden ser locales o remotos.  
Los repositorios nos permiten que otras personas puedan participar del proyecto.
- **Bifurcaciones:** Cambios en la rama principal u otra rama bifurcada, esta se puede puede combinar con la rama que deseamos por medio del proceso *merge*.
- **Actualización del repositorio remoto:** Ya confirmado el *merge*, el siguiente paso es *push*.
- **Actualización del repositorio local:** Usamos *pull* para "jalar" los cambios del repo remoto al local
### Configuración de nombre y correo
#### Git Config
Configurar por primera vez:  
*$ git config --global user.name &lt;Tu nombre&gt;*  
*$ git config --global user.email &lt;Tu email&gt;*  
Para cambiar la configuración, para un distinto repositorio:  
*$ cd &lt;directorio del repositorio&gt;*  
*$ git config user.name <"Tu nombre">*  
*$ git config user.email <"Tu email">*  
### Cambiar el editor de código que usa Git
Por defecto Git abre Vim, para cambiar esto debemos usar el siguiente comando:  
*$ git config --global core.editor "Code"* (Donde "Code" es el editor que queremos usar)  
### Comprobar Configuración de Git
*$ git config --list*
### Inicializar un proyecto Git
Si es nuevo:  
*$ git init nuevo-proyecto* (Crea el proyecto)  
*$ cd nuevo-proyecto* (Nos ubicamos en el proyecto nuevo)  
Si ya existe:  
*$ cd &lt;directorio del proyecto&gt;** (Nos ubicamos en el proyecto)  
*$ git init* (Inicializa el repositorio)