# Clase 5
## GitFlow
Es el modo de trabajo colaborativo que adopta un equipo, siguiendo las pautas de GitFlow.  
Utiliza las siguientes ramas:  
1. **main :** Tiene el código de producción.
2. **develop :** Tiene el código de pre-producción que todavía no pasa por control de calidad.  
3.  **Feature :** Funcionalidades nuevas.
4.  **Release :** Cambios tardíos.
5.  **Hotfix :** Arregla errores pequeños.  
![GitFlow](<imagenes/2025-05-09 14_31_14-Clase de Git_GitHub- Scesi - 5 - YouTube.png>)
## GitHub Flow
Tiene la rama **main** como principal y otras ramas que seran integradas por una PR.  
Para hacer uso de este flujo es necesario tener conocimiento de CI/CD.  
![GitHub Flow](<imagenes/2025-05-09 14_37_25-Clase de Git_GitHub- Scesi - 5 - YouTube.png>)
## Trunk Based Development
Solo la rama **main** y ramas auxiliares temporales que seran integradas por un PR.  
![Trunk Base Development](<imagenes/2025-05-09 14_40_55-Clase de Git_GitHub- Scesi - 5 - YouTube.png>)
## Ship/Show/Ask
1. **Ship :** Se fusiona en la rama principal sin revision.
2. **Show :** Petición de cambios para ser revisados por medio de CI, la fusion se da inmediatamente.
3. **Ask :** PR para discutir los cambias antes de la fusion.  
  
Flujo de trabajo sugerido para expertos, que tengan seguridad de subir sus cambios y pleno conocimiento del proyecto.  
![ship/show/ask](<imagenes/2025-05-09 14_53_58-Clase de Git_GitHub- Scesi - 5 - YouTube.png>)
### Reglas para Ship/Show/Ask
1. Tener un buen sistema CI/CD
2. Confianza plena en el equipo, todos deben tener buenas practicas de desarrollo y responsabilidad.
3. No es requerimiento la revision de código.
4. Las ramas son pequeñas y de corto tiempo de vida, salen desde la rama principal.