# Estructura de un proyecto
Aquí podrás encontrar la organización de carpetas y archivos para estructurar tu proyecto de modding
de manera que cumpla con las características idóneas para facilitar tu desempeño en el modding.

Cuando tu proyecto de modding no contempla intervención alguna de código o algún patrón externo
al juego como scripting de Lua, generación de paquetes de Mercury, pertenecer a un repositorio de
GitHub o similar, la lista de carpetas a continuación debería de ser suficiente para cubrir tus
necesidades:

| Nombre de la carpeta |                                                                        Descripción |
| :------------------- | ---------------------------------------------------------------------------------: |
| data                 |                               Archivos fuente que generalmente se compilan en tags |
| tags                 |        Archivos que conforman un mapa netamente, modelos, sonidos, interfaces, etc |
| hek                  |         Carpeta que contiene las herramientas de legado HEK, Guerilla, Sapien, etc |
| maps (symlink)       | Enlace simbolico que simplifica el acceder a la carpeta de mapas destino del juego |


```{important}
El [enlace simbólico](https://es.wikipedia.org/wiki/Enlace_simb%C3%B3lico) a tu carpeta **"maps"** debe ser un enlace a tu carpeta de mapas ubicada en la
raíz de tu instalación de Halo Custom Edition.
``` 

De otra manera si tu proyecto está ligado a un repositorio de GitHub (cómo suelen hacer los grandes
proyectos) entonces deberás de seguir una estructura más o menos similar a esta, asumiendo que vas
a clonar el proyecto usando [Git](https://www.atlassian.com/es/git/tutorials/what-is-git):

```bash
git clone https://github.com/MasterChief117/SuperHaloProject
cd SuperHaloProject
```
| Nombre de la carpeta |                                                                        Descripción |
| :------------------- | ---------------------------------------------------------------------------------: |
| data                 |                               Archivos fuente que generalmente se compilan en tags |
| tags                 |        Archivos que conforman un mapa netamente, modelos, sonidos, interfaces, etc |
| hek                  |         Carpeta que contiene las herramientas de legado HEK, Guerilla, Sapien, etc |
| maps (symlink)       | Enlace simbolico que simplifica el acceder a la carpeta de mapas destino del juego |
| lua                  |          Contiene código fuente relacionado con Lua, scripts, modulos, tablas, etc |
| hsc                  |               Contiene código fuente relacionado con HSC (Halo Scripting Language) |


Algunos archivos opcionales que cumplen un proposito en el estándar de proyectos integrados con Git
son:
| Nombre del archivo |                                                                                             Descripción |
| :----------------- | ------------------------------------------------------------------------------------------------------: |
| .gitignore         |                                          Especifica que archivos del repositorio de Git serán ignorados |
| .gitkeep           |                       Permite conservar una carpeta que no contenga archivos para que Git no la elimine |
| build.yaml         |                             Describe cómo construir el proyecto en la nube para fines de automatización |
| bundle.json        | Describe cómo "compilar" un proyecto Lua con sus diferentes dependencias en un solo script distribuible |
