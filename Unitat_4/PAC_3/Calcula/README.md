# Continguts de la carpeta "Calcula":

## calc.c:

El fitxer calc.c es el fitxer de implementació de la llibrería de la nostra calculadora(diu com es fan les funcions de la llibreria). Aquest fitxer no implementarà cap funció main, i té implementades les funcions:

`` suma, resta, multiplica, divideix. ``

## calc.h:

El fitxer calc.h es el fitxer de capçalera de la llibrería de la nostra calculadora, i conté les capçaleres d’aquestes funcions, per tal de ser utilitzades per altre programa.

Este fitxer conté les definicions de les funcions, sense cap detall de la seua implementació (diu què és el que fan les funcions de llibrería)

A banda de les funcions, hi ha tres línies que indiquen les directives del preprocessador #ifndef, #define i #endif. Aquestes directives actúen com a guarda. Amb açò evitem un problema bastant habitual que consisteix en importar una llibrería diverses vegades. Aquestes directives s’encarreguen de no importar el codi si aquest ja ha
estat importat.

Amb aquest mecanisme de definir macros de guarda a les directives del preprocessador, aconseguim que, si diversos fitxers font inclouen les mateixes llibreríes (com podría ser bé aquesta amb les funcions de calculadora, o bé una llibreria estàndard com stdio.h), aquesta només siga carregada una vegada.

## calcula.c:

Aquest fitxer defineix quatre funcions (a banda de la funció principal main):

`` suma, resta, multiplica, divideix. ``

La finalitat de les funcions és ajudar-nos a fer un codi més
modular, i que algunes parts es puguen reutilitzar.

## Makefile:

El Makefile es el fitxer que s’inclou en la mateixa carpeta arrel del projecte, i li indica al programa make què ha de fer amb els fitxers font per tal de compilar-los per mitjà de regles.

En un principi, no importa l’ordre de les regles, més enllà del requeriment que si no indiquem objectiu, make construeix per defecte el primer que indiquem.

En aquest cas, el Makefile té les següents regles:

``calcula:`` Obtindre l'executable calcula en base als arxius calcula.c i calc.o.

``calc.o:`` Obtindre calc.o en base a calc.c i calc.h.

``clean:`` Netejar el projecte, esborrant els arxius innecesaris.

``dist:`` Prepara la distribució del programa.

``targz:`` Comprimeix alguns arxius, i esborra els arxius innecesaris.

``install:`` Instala el programa al sistema.

**Comprobació del funcionament dels targets:**

![Comprobacio Makefile](Unitat_4/PAC_3/img/Comprobacio_Makefile.PNG "Comprobacio Makefile")