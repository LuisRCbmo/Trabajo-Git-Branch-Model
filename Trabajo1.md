# Git Branch Model
El git branch model hace referencia a un modelo de desarrollo o estrategia de ramificacion, consiste en un conjunto de procedimientos que cada miembro del equioi debe seguir, con el objetivo de tener un proceso de desarrollo administrado.

La configuracion del repositorio que el metodo utiliza es el de un repositorio remoto quue recibe el nombrbe "origin", cada miembro del equipo podra empujar y tirar de origin.

El metodo de ramificaion trabaja con 2 tipos de ramas, las ramas principales y ramas de apoyo.
## Ramas Principales
Son las ramas unicas y de vida infinita, existen 2 ramas principales:
- Master
- Desarrollo
### Master
La rama master tambien llamada origin, contiene todo el codigo fuente de la aplicacion que ha sido liberado y consiredado estable para ponerlo a dispocision del usuario.
### Desarrollo
Tal como lo dice el nombre, el objetivo de esta rama es trabajar en el desarrollo de la siguiente version de la aplicacion, almacenando los cambios mas recientes y ocupandose del progeso de estos.

una vez el codigo contenido en la rama de desarrollo, debera de alguna manera incorporarse a la rama master, convirtiendose en nuevo contenido y modicando la etiqueta de version.
## Ramas de Apoyo
Las ramas de apoyo estan para ayudar permitiendo un desarrollo en paralelo, estas ramas tienen vida limitada por lo que eventualmente seran eliminadas, existen 3 tipos de ramas de apoyo:
- Ramas de caracteristicas
- Ramas de liberacion
- Ramas de revisión
### Ramas de Caracteristicas
Estas ramas se crean a partir de la rama de desarrollo y se utilizan para el desarrollo de nuevas caracteristicas que seran incluidas en versiones futuras de la aplicacion, no necesariamente en la siguiente.

una rama de caracteristica existe mientras la caracteristica objetivo se trabaje, ya terminada la caracteristica esta se incorporara a la rama de dasarrollo y el paso siguiente sea eliminar su rama de caracteristica correspondiente.
### Ramas de Liberacion
Este tipo de ramas surgen de la rama de desarrollo y se crean una vez se considere que el estado actual de la version en desarrollo, este lista para su liberacion a usuarios. 

En otras palabras estas ramas sirven para apoyar la nueva version de produccion, permite agregar puntos de ultima hora y hacer correcion de errores.

El contenido de la rama de liberacion se incorporara a la rama master, lanzando asi la nueva version y tambien se reincorporara a la rama de desarrollo para actualizarla con todas las correciones realizadas en la rama de liberacion.
### Ramas de Revision 
Se crean a partir de la rama master y surgen de la necesidad de actuar inmediatamente ante el estado actual de la version ya lanza de la aplicacion.

La rama debe corregir errores que se encuentre en las version disponible al usuario, una vez solucionado el problema en la rama de revision se reincorporara a la rama master lanzando asi una version mejorada, tambien debera modificarse la etiqueta de version pero debe ser a baja escala, por ejemplo de la version 1 a la version 1.1