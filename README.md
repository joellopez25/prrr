# projecte M3


-Esquema principal del projecte:
-

  1. Primer l'usuari ha de crear un taulell buit(tindrem una array delimitada per columnes i files, i un for per les columnes que tindra un altre dins per les filas i printarem per cada posicio un 0) o crear un taulell que ja tingui malalts(tindrem una array delimitada per columnes i files, i un for per les columnes que tindra un altre dins per les filas i printarem per cada posicio un numero random del 0 al 50, Math.random) .
  
  2. Al usuari se li proporcionara un menu on pot triar la opció que vulgui, on li demanarem un numero i segons aquest numero escollira una opció o una altre, cada opcio estara enmagatzemada en un while, el usuari despres de cada opcio tindra la oportunitat de turnar de agafar l'opcio que vulgui i podra fer aixo tans cops com vulgui.
  
  3. Si posa el numero 2, agafa la opció de introduir malalts on, primer li pregunten que a quina posició del taulell vol afegir malalts(aquestes posicions seran dues variables(taulell[y][x])) y despres el numero de malalts vol que hi hagi en aquesta posició opcionalment l'usuari pot afegir malalts a la posició que vulgui del taulell.
  
  4. Si posa el numero 3, agafa la opció de transmitir  virus, primer li demanara quina tasa vol(variable de tipus float) que no sigui inferior a 0, posarem dos for per recorrer columnes i files i dins farem el calcul de la tasa.
  
  5. Si posa el numero 4, agafara la opció de curar malalts, li preguntara que si vol aplicar la cura glogalment o a una posició concreta, si posa globalment, li preguntara que si vol que el precenntage de curats vol que sigui random(Math.random) o especific, si en comptes de globalment posa concreta, li preguntara si vol un percentage o valor concret, si posa peercentage sera com abans pero a la posició del taulell que el usuari desitji(taulell[y][x]), i si posa valor concret se li demanara al usuari un valor de curats respecte a la posició abans demanada, el valor sempre ha de ser mes petit que el numero de malalts de la posició concreta.
  
  6. Si posa el numero 5, agafara la opció de desplaçar malalts, on primer li pregunten quina posició(y,x) de la taula vol escollir per desplaçar els malalts, a continuacio amb una varible int, demanarem cuants malalts de la posició vol desplaçar, sempre menor que els malalts que hi han a la posició, per ultim li demana que posi una de les següents lletres:q (dalt esquerra), w (dalt mig), e (dalt dreta), a (esquerra mig), d (dreta mig), z (baix esquerra), x (baix mig), c (baix dreta), segons la lletra que posi la a la 
  x = files , y = columnes, li restarem o sumaren la posició, en cas de la y si es dalt = y-1 i si es baix = y+1 i si es esquerra o dreta es queda igual i a la inversa amb la x,
  si es esquerra = x-1 i si es dreta= x+1, si es dalt o baix es queda igual, tota aixo en un if de que si la lletra que introdueixes es igual a alguna de les que hi hagi en el lletra.equals(), la posició cambiara respecte la lletra
  
7. Si poses el numero 6, mostrarà tota la informació del taulell. el primer que sortirà serà el total de malalts, desprès et donarà la informació dels malalts que no hi han complit el confinament, també et dirà el total de la gent que se ha escapat del confinament i per últim et proporcionarà la informació de tots els malalts que estan curats.

8. Per últim si poses el numero 7, sortirà un missatge el qual et dirà que és sortit del joc i desprès et preguntarà si vols jugar un altre cop o no. En el cas que vulguis tornar a jugar has de dir-li que (si) i et sortirà un altre cop el menú amb les opcions corresponents. En cas que diguis que (no) es finalitzarà el joc amb un missatge d'acomiadamen
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
-Explicació de decisions de disseny:
-

  -Primer de tot hem hagut de crear dos variables que es diuen files i columnes, per desprès utilitzar-les en un for per poder anar posició per posició del taulell.
  
  -Desprès hem hagut de crear un array per poder emmagatzemar les posicions del taulell que va regit per files i columnes.

  -Printem un menú on posem les opcions que hi ha i el numero corresponent per cadas cuna i desprès amb un while si la resposta de l'usuari és igual a x numero posem el seu codi corresponent dins del while.

-per fer la primera opció de carregar el taulell dins de la resposta de quina opció vols triar del menú és un 1 et farà una pregunta que si vols carregar el taulell de malalts o buit, segons la resposta carregarem un taulell ple de 0 en cas que la resposta sigui buit i amb randoms del 1 a 50 en el cas que sigui malalts.
  
  -Per introduir malalts hem hagut de crear dos for, un per les files i l'altre per les columnes i a cada posició igualar l'array taulell al número de persones que vol           l'usuari i després printar el taulell.
  
  -Per fe el punt de transmetre virus hem hagut de fer el càlcul i igualar les posicions del taulell a aquest càlcul, i així per cada posició del taulell el número que hi         hagi en aquesta canviarà amb el càlcul i desprès printarem el taulell amb els número nous.
  
  -Per curar malalts en el cas que sigui globalment solament pot ser percentatges, llavors hem hagut de fer dos if al qual si era random em fet un math.random de l'1 al 100,
    desprès amb aquest percentatge hem de fer el càlcul de transmissió de virus per cada posició. Aquest càlcul l'hem hagut d'igual a cada posició del taulell i en cas que el      percentatge sigui específic hem hagut de fer el mateix però en comptes que el percentatge sigui random en aquest cas l'usuari a de introduirlo a la consola. i en cas que      no sigui  globalment sinó posició concreta farem el mateix amb els percentatges però en comptes de fer-ho amb totes les posicions ho farem amb les que l'usuari      introdueixi a la consola: això un farem fem dos variables(x,y) i aquestes dos variables les introduirem a l'arry taulell, i desprès en un if posarem que si les dos arrays
    (taulell[x][y]==taulell[i][j]), així podem saber a quina posició vol curar al malalt, desprès farem el mateix càlcul com el globalment.

-Per desplaçar malalts, el primer que hem fet és d'emanar les coordenades i el número de malalts que volem desplaçar. El número de malalts té que sé inferior o igual que el taulell perquè el codi et deixi desplaçar malalts. una vegada introduit els malalts que vols desplaçar y les cordenadas et demanara les seguents lletres: q (dalt esquerra), w (dalt mig), e (dalt dreta),a (esquerra mig), d (dreta mig), z (baix esquerra), x (baix mig), c (baix dreta). Cada lletra que tu introdueixis cambia una posicio en cocncreta, si tu introdueixes una lletra que no es la demanada no fara res i et demanara un altre cop les lletres. un exemple seria si en la posicio 2 2 tenim 10 malalts y volem desplachar 5 malalts a la dreta el que tendriam que fer es que cuan et demani les lletres introduiras la d, aixo fara que a la posicio 2 2 es quedin 5 i a la posicio de la dreta del 2 2 es desplaçaran 5.

-Per mostrar informació en el cas del total de malalts fem dos for per recore les columnes i les files dins d'aquest dos for posarem que si la posició del taulell és diferent de 0 sumarem totes les posicions.Això ho fem gràcias a una variable inicialitzada a 0 i la sumem amb la posició que hi ha en aquell moment, en el cas del total de malalts que no an complit el confinament posem que cada cop que a l'hora de desplaçar malalts posem la quantitat de malalts que volem desplaçar, aquesta quantitat sumarà amb la variable inicialitzada a 0. Al final printarem aquesta variable. per calcular el total de malalts que se escapen cada cop que el ususari a la hora de desplaçar malaltposi unes cordenades que no estiguin dins del taulell la cuantitat de malalts que vulgui desplaçar es sumara amb una variable inicialitzada a 0 i al final en el apartat de mostrar informació la printem. Per calcular el total de curats haures de posar una variable inicialitzada a 0 i que després  a sota de cada calcul que fem a el apartat de curar malalts haurem de posar que la variable es igual a la variable mes el calcul i despres printar la variable en mostrar informació

-per sortir del joc farem una pregunta la cual es si vols seguir jugan o no. En el cas de introduir un si, hem fet que torni a sortir el menu amb totes les opions del programa i podras tornar a fer el joc de nou. En el cas de que introdueixis un no, et sortira un missatge d'acomiadament.
 el codi utilitzat seria
 
 -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 -Explicació del repartiment de les tasques entre tots dos integrants:
-

-El nostre grup està format per Rubèn i Joel:
Rubèn: S'ha encarregat de la codificació del projecte i d'ajudar amb el readme.md .
Joel:S'ha encarregat d'ajudar al company quan aquest ha tingut un problema i no la pogut resoldre per ell mateix i de fer el readme.md .

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Jocs de prova:
-
-Cas extrem de Desplaçar malalts:
En aquest cas he posat unes cordenades que que tenen joc en cap posició del taulell i en comtes de sortirme el error de Out of Bounds em surt un misatje de que esta fora de rang i haig de tornar a agafar una opció
![Captura de pantalla 2021-01-13 195156](https://user-images.githubusercontent.com/76974332/104496861-d3867280-55d9-11eb-91e0-e5212cf588a9.png)

-Cas normmal de Desplaçar malalts:
En aquest cas he posat unes coordenadas que coincideixen amb la posició del taulell i he desplaçat 20 malalts a la dreta
![cas normal](https://user-images.githubusercontent.com/76974332/104498596-311bbe80-55dc-11eb-9b8c-5b15726330a6.png)

-Cas extrem de Desplaçar malalts:
En aquest cas he posat unes coordenadas que coincideixen amb la posició del taulell peró com he desplaçat mes malalts dels que hi havia a la posició me ha posat el misatje que el valor es major i haig de tornar a agafar una opció 
![Cas extrem](https://user-images.githubusercontent.com/76974332/104499069-d33ba680-55dc-11eb-8a65-04bf13146c85.png)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Propostes de millora i Control d'errors:
-
Propostes de millora:
La primera millora seria fer l'apartat de les posicions bloquejades(x), ja que no hem pogut fer-lo. 
La segona protesta de millora seria simplificar el codi.

Control d'errors:
En els casos on l'usuari a da possar les cordenadas on vol afegir un malalt, curar, desplaçar etc. hem fet que les posicions que posa el usuari que estan fora del rang(fora del taulell) printem un misatge dient que la posicio que a posat el usuari esta fora de rang, i li turnem a demanar una opció del menu, en comptes de que apereixi un error de java i es pari el programa.
i en casos com per exemple el de desplaçar malalts si el valor que introdueix el usuari es major que el que hi ha a la posició apareixera un missatge dient que el valor concret es major, i li turnem a demanar una opció del menu, en comptes de que apereixi un error de java i es pari el programa.
