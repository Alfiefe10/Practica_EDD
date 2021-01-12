# Continguts de la carpeta "Hola":

## hola.c:

Un programa senzill en C, de l’estil «Hola Món».

## Makefile:

El Makefile es el fitxer que s’inclou en la mateixa carpeta arrel del projecte, i li indica al programa make què ha de fer amb els fitxers font per tal de compilar-los per mitjà de regles.

En un principi, no importa l’ordre de les regles, més enllà del requeriment que si no indiquem objectiu, make construeix per defecte el primer que indiquem.

En aquest cas, el Makefile té les següents regles:

``hola:`` Obtindre l'executable hola en base al arxiu hola.c, mostrant també tots els Warnings durant la compilació.

``clean:`` Netejar el projecte, esborrant el arxiu executable "hola".

**Comprobació del funcionament dels targets:**

![Make hola](https://github.com/Alfiefe10/Practica_EDD/blob/master/Unitat_4/PAC_3/img/Make_hola.PNG?raw=true "Make hola")