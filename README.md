Festivals.js
============

Festivals.js és un prototpip d'aplicació que he creat com a projecte de final del Màster d'Enginyeria Informàtica de la UOC.

Consisteix en crear i desenvolupar l'arquitectura d'una aplicació web per trobar gent amb qui gaudir de concerts

#### Demo ONLINE allotjada a: https://festivals-js.herokuapp.com/

#### Memòria en format PDF, al repositori de la UOC: http://openaccess.uoc.edu/webapps/o2/handle/10609/59466

#### Instruccions instal·lació local:

1.   Instal·lar   node.js   des   de   la   pàgina   oficial.   La   recomanada   per   la   majoria
d’usuaris és suficient.
https://nodejs.org/en/

2.   Un   cop   instal·lat,   accedir   a   la   consola   de   Node.js,   anomenada   «Node.js  
command prompt» i accedir a la carpeta on es troba el projecte festivals-js

3.  Des  de la  mateixa  carpeta,  instal·lar  les  dependències (llibreries  externes;  
pex express) 
amb la comanda:
`npm install`

4. Després, executar el servidor node.js amb la comanda:
`node server.js`
Hauria de sortir per la consola el missatge:
Servidor iniciat pel domini i port 127.0.0.1:8080

5. Finalment, obrir l’adreça al navegador:
http://localhost:8080/
Per parar el servidor simplement pitjar Ctrl.+C dues vegades.
I per reiniciar-lo, introduir de nou:
`node server.js`


### Versió actual: alpha-2. Gener 2017.


### Les tecnologies usades són:
* Llenguatge Javascript i objectes JSON pel tractament de les dades.
* Node.js i Express.js al costat del servidor.
* HTML5, AngularJS(*) i Bootsrap al costat del client.

### Distribució del codi.

##### Carpeta app
Conté el back-end de l'aplicació; amb la gestió de rutes, la persistència de dades i un servei web REST.

##### Carpeta angular
El front-end de l'aplicació, amb AngularJS (presentació de les dades i comunicació amb el back-end), Bootstrap (llibreria estils responsive) i HTML5 (estructura).

##### festivals.json
Conté les dades de l'aplicació web.

##### festivals_init.json
Una còpia de les dades per tal de poder resetejar les dades de prova.

##### server.js 
Punt d'arrencada del servidor web amb els concerts.

##### package.json
Configuració del projecte back-end


(*)Nota: En el moment de desenvolupament, finals del 2016, no vaig veure prou madur Angular 2; i per això vaig optar de fer el front-end de l'aplicació en AngularJS (les versions 1.x) Aquest article explica molt bé les diferencies entre Angular i AngularJS:
[https://www.campusmvp.es/recursos/post/es-angular-2-angular-4-o-simplemente-angular.aspx]


### Futures versions:

Falten dues grans millores a l'arquitectura per a que l'aplicació sigui útil.
1. Gestionar les dades en una base de dades NoSQL com MongoDB; en comptes de fitxers JSON.
2. Autenticació i gestió de permisos pels usuaris. Ara mateix tothom pot crear concerts (sense registra-se), i encara més, editar i eliminar concerts que han creat altres usuaris. Aquest funcionament és inacceptable en una aplicació real, per això està en fase alpha.

### Història d'usuari en procés.

#### Versió beta1 (febrer 2018)
És innaceptable permetre a qualsevol usuari. Com que no preveig implantar-la inmediatament, vull tenir una versió de només lectura de l'aplicació. Només l'actualitzarà un tècnic amb accés al codi font modificant el fitxer JSON corresponent.
És a dir, la beta1 tindrà les següents històries, ja implementades:
* HU1. Com a visitant vull veure en que consisteix la pagina, qui l'esta fent, novetats,…
* HU2. Com a visitant vull veure un llistat de tots els pròxims concerts ordenats per data.
* HU8 Vull trobar festivals a la localitat que indiqui
* HU9 Vull filtrar els festivals que siguin gratuïts.
* HU16 Obtenir el llistat de concerts paginat si és llarg (pex de 10 en 10)

I les següents:
* HU18. Com a administrador vull gestionar els concerts editant el fitxer on estan allotjats actualment.
* HU19. Vull afegir a llista de concerts els que considero més interessants 2018.

### Històries d'usuari implementades.

#### Versió alpha2 (gener 2017)
Les noves històries d'ús que s'han completat en aquesta fase són aquestes,
que tenen una prioritat alta (entre 70 i 90):
* HU5 Fins i tot, anul•lar un concert abans que comenci.
* HU8 Vull trobar festivals a la localitat que indiqui
* HU9 Vull filtrar els festivals que siguin gratuïts.
* HU16 Obtenir el llistat de concerts paginat si és llarg (pex de 10 en 10)

#### Versió alpha1 (desembre 2016)
S'han afegit les les 4 primeres funcionalitats, que tenen una prioritat màxima (100); que són:
* HU1. Com a visitant vull veure en que consisteix la pagina, qui l'esta fent, novetats,…
* HU2. Com a visitant vull veure un llistat de tots els pròxims concerts ordenats per data
* HU3. Com a visitant/usuari vull crear una trobada a un concert
* HU4. I vull poder editar l'event abans que comenci

### Bugs i millores.

Per a gestionar els bugs i millores (usabilitat,evolutius) uso el gestor d'incidències de GitHub:
https://github.com/mamorosdev/festivals-js-alpha2/issues 

Hagués estat bé usar el mecanisme de releases que ofereix Github, en comptes de pujar directament la última versió.
