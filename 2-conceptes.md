


#  2.- Conceptes bàsics de programació: Variables i operadors

## 1. Variables

Les **variables i els operadors aritmètics** són la base de qualsevol recepta de codi.

Una variable és com un pot d’etiqueta clara on hi pots deixar ous, patates o el resultat d’un càlcul. Un operador és el ganivet, la batedora o la balança que transforma aquests ingredients. Si aprens a omplir els pots i a fer‐los interactuar amb els estris adequats, podràs demanar a l’ordinador que recalculi proporcions, sumi costos o multipliqui racions amb la mateixa precisió amb què escales una truita de patates de dues a vint persones.

Sense aquest duet essencial, pots i estris, no existirien els comptes enrere dels videojocs, les calculadores dels bancs en línia ni el simple “m’agrada” que actualitza un comptador en una xarxa social. Dominar variables (ous = 4) i operadors (ous *= comensals) és, doncs, el primer gran pas perquè el teu codi deixi de ser llista d’ingredients dispersa i es converteixi en una autèntica recepta executable.

En aquest capítol veurem com declarar variables amb sentit, canviar‐les al vol i aplicar els set operadors bàsics (+ - * / // % **) a exemples tan quotidians com ajustar el temps de cocció o repartir porcions. Deixarem l’ordinador batent, sumant i dividint per nosaltres, i tu, mentrestant, podràs concentrar‐te en l’olor de la truita acabada de girar.


## 1.1. Què és una variable?

Una variable és un espai de memòria amb un nom, un pot digital, que pot contenir un valor. A Python, crear-la és tan senzill com enganxar una etiqueta al pot i omplir-lo:

* els # s'utilitzen per donar comentaris al codi sense que afecti a la logica del programa.
```Python
ous = 4         # tenim quatre ous
papates = 3     # tres papates mitjanes
```

* ous i patates són els identificadors (els noms dels pots).
* El signe = és la cullera: posa el valor dins del recipient.
* El valor (4, 3, …) pot canviar quan vulguis: el pot és reutilitzable.





## 1.2. Constants: els ingredients “intocables”

En moltes receptes (i també en programació) hi ha valors que no haurien de canviar mai.

Imagina que sempre cuines la teva truita de patates amb una temperatura fixa al foc o que cada ració està pensada per contenir exactament 2 ous. Aquests són exemples de constants: valors que es mantenen igual tot el temps, perquè són part de la “norma” de la recepta o del sistema.

Una **constant** és una tipus de variable que no canvia durant l'execució del programa. Així funcionen els llenguatges que utilitzen constants. 

Amb Python totes les variables es poden modificar, però per convenció, es respecta que si el nom està en MAJUSCULES no es canvia el valor.

Pensa en una constant com en un ingredient fix de la recepta. No canvia cada vegada que la prepares:

```Python
OUS_PER_RACIO = 2
TEMPERATURA_FOC = 180
```

**Diferència entre variable i constant**

| Tipus | Es pot canviar? | Exemple en la truita de patates |
|--- |---|---|
|Variable|Sí|patates = 4 (segons els comensals)|
|Constant|No|OUS_PER_RACIO = 2 (sempre 2 ous per ració)|




## 1.3. Tipus de valors: mida i sabor dels ingredients

Python és un llenguatge dinàmic: el pot es fa a mida de l’ingredient que hi poses. Això vol dir que no cal declarar el tipus de variable
abans d’utilitzar-la. L’ordinador dedueix quin tipus de dada estàs utilitzant en funció del valor que li assignis.

|Tipus bàsic | Descripció | Exemple “truitaire” |
|---|---|---|
|int|Enter |sencerpatates = 3|
|float|Nombre |decimaloli_ml = 75.5|
|str|Cadena de text|chef = "Ada"|
|bool|Booleà (True/False)|vol_ceba = True|



```Python
patates = 3         # Python sap que això és un nombre sencer (int)
oli_ml = 75.5       # Aquí reconeix un número decimal (float)
chef = "Ada"        # Una cadena de text (str)
vol_ceba = True     # Un valor lògic, només pot ser True o False (bool)
```

Aquest comportament és molt flexible i útil: ens estalvia haver de dir explícitament quin tipus de dada és cada variable. Però, com a bons cuiners, cal vigilar què barregem a l’olla.

Recorda: una variable **pot canviar de valor i de tipus** 

```Python
oli_ml = 75.5       # float
oli_ml = "molt"     # ara és string!
```




## 1.4. Com escollir un bon nom de variable

Igual que no etiquetes un pot de sucre com "salsa picant", en programació posar bons noms a les variables és fonamental.
T’imagines llegir una recepta on en lloc de ous_batuts et posen ob? O pitjor encara: que et diguin que el pas 3 és "fer coses amb x1x2x3"?

Per això, aquí tens quatre regles d’or (amb gust de patata):

**1. Sigues significatiu:**
Bé:
```Python
ous_batuts = 3
```
Malament:
```Python
ob = 3      # Què dimonis és ob? Ous bullits? Origen Basc?
``` 
Si et cau el codi a terra d’aquí sis mesos, vols saber què fa sense haver de tastar-lo. Escriu com si t’ho haguessis d’explicar a tu mateix… del futur!

**2. No comencis per números:**
Bé:
```Python 
patates_2 = 2
```
Malament:
```Python 
2patates = 2
```

Python no entén noms que comencin per un número. Si ho fas, rebràs un “SyntaxError” que sona com una alarma de forn massa calent.



**3. Sense espais en blanc:**
   
En tots els llenguatges de programació, els espais en blanc no es poden fer servir dins del nom d’una variable. Per a fer-ho correcte podem utilitzar dos tipus d'accions:

CamelCase:

Consisteix a juntar les paraules sense espais però posant en majúscula la primera lletra de cada paraula, excepte la primera.

```Python
nomDelCuiner = "Ada"
tempsDeCoccio = 8
patatesTallades = 12
```

sanke_case:

Consisteix a substituir els espais per guions baixos (_), i posar totes les lletres en minúscules.

```Python
nom_del_duiner = "Ada"
temps_de_coccio = 8
patates_tallades = 12
```



## 1.5. Modificar variables

Una de les grans virtuts de les variables és que no són definitives. Pots canviar el seu valor tantes vegades com vulguis durant l’execució del programa.

És com tenir pots que es poden omplir, buidar o barrejar sense límits!

```Python
ous = 4
print(ous)      # 4
ous = ous + 2
print(ous)      # 6
```

# 2. Operadors

Operadors combinats: menys línies, mateixa força

Per fer els càlculs més àgils i nets, Python ofereix operadors abreujats que combinen l’assignació (=) amb una operació (+, -, *, /,
etc.):

```Python
patates = 4     # Nombre de patates
ous = 2         # Nombe d'ous
oli_ml = 50     # Quantitat d'oli en mil·lilitres

patates *= 2    # Múltiplica per dos; útil si dobles la recepta
ous -= 1        # Traiem un ou perquè un convidats'ha fet enrere 
oli_ml += 25    # Afegim més oli per evitar que s'enganxi
```



Aquestes formes són molt útils per receptes variables: quan cuines per un nombre de persones que pot canviar, o quan vols ajustar
quantitats segons el gust del cuiner (amb o sense ceba, per exemple).

