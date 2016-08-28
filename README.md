##Git rebase

En Git tenemos dos formas de integrar cambios de una rama en otra: la fusión (merge) y la reorganización (rebase). 

###Rebase utilizado como parámetro de pull
Cuando hacemos git pull, nos traemos los cambios del repositorio que elijamos o tengamos configurado, y uno de los parámetros que podemos utilizar es rebase:

*git pull --rebase*

**¿Qué hace esto?**
Al realizar un pull estamos haciendo un fetch y justo después un merge, pasándole la opción rebase, git intentará traer todos los cambios y después aplicar nuestras modificaciones encima en lugar de intentar hacer un merge desde el punto en el que estábamos, esto hará que nuestro histórico tenga mucho mejor aspecto.

![alt text](https://github.com/Oswaldofm17/Git-Rebase/blob/master/rebase.png "Rebase")

###Comando rebase

En lugar de enlazar las ramas con un commit de merge, el hacer rebase a una rama mueve completamente la rama con la nueva característica hacia la punta de master como se muestra abajo.

![alt text](https://github.com/Oswaldofm17/Git-Rebase/blob/master/rebase%20(1).png "Logo Title Text 1")

Esto sirve para el mismo propósito que git merge, la integración de commits de diferentes ramas. Pero hay dos razones por las que quisiéramos optar por un rebase sobre un merge:

*Resulta en una historia lineal del proyecto.
*Nos da la oportunidad de limpiar commits locales.


