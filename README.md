# Alkalmazások Fejlesztése 3. beadandó

## Követelményanalízis

###Feladat:
 + Tennivalók felvételének és listázásának szimulálása.

####Funkcionális elvárások:
+ Legyen egy felhasználó és egy tennivalók model, köztünk 1..N kapcsolattal. Egy felhasználóhoz tartozhat több tantárgy.
+ A tennivalókat meg lehet tekinteni, leírásukat szerkeszteni és törölni

####Szerepkörök:

Felhasználó
+ Tennivalók listázása
+ Tennivalók feltöltése, törlése, szerkesztése
+ Új felhasználó hozzáadása az egyes kurzusokhoz


1. Architektúra terv
  +  Oldaltérkép
    + Főoldal
      +Leírás
      + Tennivalók Lista
        + Új tennivaló hozzáadása

  + REST API végpontjai
     + GET
     + POST
     + PATCH
     + DELETE


2. Felhasználóifelület-modell
  + Oldalvázlat
    ![Oldalvázlat](https://cloud.githubusercontent.com/assets/14542234/12258095/352e2d36-b90c-11e5-9c1b-9b14147c95c3.png)

3. Adatmodell
   + ![adatbázis diagram](https://cloud.githubusercontent.com/assets/14542234/12257874/5cfe6cba-b90a-11e5-85c1-81c015cdab94.png)

##Implementáció

+ Fejlesztői környezet
  + Cloud9 IDE
+ Könyvtárstruktúra
+ bead2
  + app: app.js alkalmazás, router.js-ben található hogy az oldalak milyen címen legyenek elérhetőek
    + pods: ember.js podok
      + components: üzleti logika
      + index: kezdőlap 
      + signup: felhasználó regisztrációja
      + todo: tennivalók modellje
      + todos: tennivalók szerkezete
      + user: felhasználó modellje
    + styles: stíluslapok
  + bower_components: bower elemei
  + config: ember.js konfiguráció 

##Felhasználói Dokumentáció
+ Követelmények
  + 2GB memória
  + 1GB HDD
+ Az alkalmazás használata:
  + A főoldalról elérhető a tennivalók listája
    + Regisztráció
      + A regisztrációval tudunk új felhasználót felvenni
    + Tennivalók listája
      + Hozzáadás: 'Új munka felvitele' gombbal.
        + Itt meg kell adni a tennivaló leírását, helyszínét, határidejét, illetve hogy melyik felhasználó adja hozzá. A submit gombbal mentjük.
      + Tennivalók törlése és szerkesztése a sorban megfelelő gombra kattintva végezhető el.
+ Először érdemes egy felhasználót létrehozni, hogy lehessen hozzá tennivalót kapcsolni.
