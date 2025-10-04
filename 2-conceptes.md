#  2. Conceptes bàsics de programació: Variables i operadors

## 2.1. Variables

Les **variables i els operadors aritmètics** són la base de qualsevol recepta de codi.

Una variable és com un pot d’etiqueta clara on hi pots deixar ous, patates o el resultat d’un càlcul. Un operador és el ganivet, la batedora o la balança que transforma aquests ingredients. Si aprens a omplir els pots i a fer‐los interactuar amb els estris adequats, podràs demanar a l’ordinador que recalculi proporcions, sumi costos o multipliqui racions amb la mateixa precisió amb què escales una truita de patates de dues a vint persones.

Sense aquest duet essencial, pots i estris, no existirien els comptes enrere dels videojocs, les calculadores dels bancs en línia ni el simple “m’agrada” que actualitza un comptador en una xarxa social. Dominar variables (ous = 4) i operadors (ous *= comensals) és, doncs, el primer gran pas perquè el teu codi deixi de ser llista d’ingredients dispersa i es converteixi en una autèntica recepta executable.

En aquest capítol veurem com declarar variables amb sentit, canviar‐les al vol i aplicar els set operadors bàsics (+ - * / // % **) a exemples tan quotidians com ajustar el temps de cocció o repartir porcions. Deixarem l’ordinador batent, sumant i dividint per nosaltres, i tu, mentrestant, podràs concentrar‐te en l’olor de la truita acabada de girar.


## 2.1.1. Què és una variable?

Una variable és un espai de memòria amb un nom, un pot digital, que pot contenir un valor. A Python, crear-la és tan senzill com enganxar una etiqueta al pot i omplir-lo:

* els # s'utilitzen per donar comentaris al codi sense que afecti a la logica del programa.
```Python
ous = 4         # tenim quatre ous
papates = 3     # tres papates mitjanes
```

* ous i patates són els identificadors (els noms dels pots).
* El signe = és la cullera: posa el valor dins del recipient.
* El valor (4, 3, …) pot canviar quan vulguis: el pot és reutilitzable.


## 2.1.2. Constants: els ingredients “intocables”

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

| Tipus | Es pot canviar? | escrit | Exemple en la truita de patates |
|--- |---|---|---|
|Variable|Sí| minúscules |patates = 4 (segons els comensals)|
|Constant|No| MAJÚSCULES | OUS_PER_RACIO = 2 (sempre 2 ous per ració)|


## 2.1.3. Tipus de variables

Python és un llenguatge dinàmic: el pot es fa a mida de l’ingredient que hi poses. Això vol dir que **no cal declarar el tipus de variable** abans d’utilitzar-la. L’ordinador dedueix quin tipus de dada estàs utilitzant en funció del valor que li assignis.

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

|Tipus complexes | nom | Descripció | Exemple |
|---|---|---|---|
|Cadenas|	str	|String o cadena de caràcters | "Python", "Hola mundo"|
|Listas|	list	|Seqüències ordenades d'objectes | [1, 2, 3, "cuatro", True, [5, 6, 7]] |
|Tuplas **\***|	tuple|	Seqüències ordenadas inmutables d'objectes| ("tres", [23, 34], -89, False) |
|Conjuntos **\***|	set	|Coleccions sense duplicats no ordenadas d'objectes| {1, 2, "a", "b"} |
|Diccionarios **\***|	dict	|Pars ordenats atribut:valor | {"nom":"Juan", "cognom":"Pérez"} |
|binari| bin |Amb prefix 0b |binari = 0b1101|
|octal| 0o | Amb prefix 0o (zero i o minúscula) |octal = 0o10|
|hexadecimal| hex | Amb prefix 0x|hexadecinal = 0xA0F|

**\*** No els aprendràs aquest curs.

Podem transformar els tipus començant pels 3 símbols `>>>`, per exemple:
```Python
>>>hex(10)      # convertim el 10 decimal a hexadecimal
>>>bin(8)    # ara convertim de decimal a binari i ens retornarà '0b1000'
>>>int(0xb)  # convertim de hexadecimal a decimal
>>>int(0b1000)  # convertim de binari a decimal
```

Aquest comportament és molt flexible i útil: ens estalvia haver de dir explícitament quin tipus de dada és cada variable. Però, com a bons cuiners, cal vigilar què barregem a l’olla.

Recorda: una variable **pot canviar de valor i de tipus** 

```Python
oli_ml = 75.5       # float
oli_ml = "molt"     # ara és string!
```
## 2.1.4. Com escollir un bon nom de variable

Igual que no etiquetes un pot de sucre com "salsa picant", en programació posar bons noms a les variables és fonamental.
T’imagines llegir una recepta on en lloc de ous_batuts et posen ob? O pitjor encara: que et diguin que el pas 3 és "fer coses amb x1x2x3"?

Per això, aquí tens quatre regles d’or (amb gust de patata):

**1. Sigues significatiu:**

```Python
ous_batuts = 3   #Bé
ob = 3    # Què dimonis és ob? Ous bullits? 
```

Pensa en el programador que haurà d'entendre el codi després de tu, o tu d'aquí un temps, per això es recomana que les variables s'entenguin i també posar comentaris!
> Python i tots els llenguatges de programació són **Case-sensitive**, no és igual majúscules i minúscules, és a dir, la variable `var` és diferent de `Var`

**2. No comencis per números:**

```Python 
patates_2 = 2   # Bé
2patates = 2   # Malament
```

Python no entén noms que comencin per un número. Si ho fas, rebràs un “SyntaxError” que sona com una alarma de forn massa calent.


**3. Sense espais en blanc:**
   
En tots els llenguatges de programació, els espais en blanc no es poden fer servir dins del nom d’una variable. Per a fer-ho correcte podem utilitzar dos tipus d'accions:

*CamelCase*:

Consisteix a juntar les paraules sense espais però posant en majúscula la primera lletra de cada paraula, excepte la primera.

```Python
nomDelCuiner = "Ada"
tempsDeCoccio = 8
patatesTallades = 12
```

*sanke_case*:

Consisteix a substituir els espais per guions baixos (_), i posar totes les lletres en minúscules.

```Python
nom_del_duiner = "Ada"
temps_de_coccio = 8
patates_tallades = 12
```

## 2.1.5. Modificar variables

Una de les grans virtuts de les variables és que no són definitives. Pots canviar el seu valor tantes vegades com vulguis durant l’execució del programa.

És com tenir pots que es poden omplir, buidar o barrejar sense límits!

```Python
ous = 4
print(ous)      # 4
ous = ous + 2
print(ous)      # 6
```
## 2.1.6. Modificar variables de tipus string (cadena de text)

Les cadenes de text (strings) són molt utilitzades en programació. Les funcions més importants per treballar amb strings s'utilitzen per extraure subcadenes (substrings), eliminar espais sobressalents (fet que anomenem trim), i altres.

|Funció | Descripció | Exemple |
|---|---|---|
|substring|	Extracció de subcadenes	| text[0:4]|
|trim|	Eliminar espais en blanc. Es poden utilitzar strip(), lstrip() o rstrip() 	|text.strip() |
|majúscules| upper() canvia a tot majúscules, lower() a minúscules i title() a tipus títol | text.upper() |
|buscar text| find() busca un text, in s'utilitza en condicionals| text.find("Python")  print("món" in text)|
|separar | split() divideix una cadena de text i retorna una llista | text.split()
|unir | join() uneix dos strings que estan en una llista | frase = " ".join(llista)

Ara s'expliquen amb més detall

### Extracció de subcadenes (substrings)
Una de les operacions més comunes és obtenir parts d'una cadena. Per fer-ho, a Python s'usa la indexació i el tall (slicing).

Exemple:

```Python
text = "Hola món"
substring = text[0:4]  # Extraure des de la posició 0 fins a la 3 (4 no inclòs)
print(substring)  # Sortida: Hola
```
Aquí text[0:4] diu: "Agafa els caràcters des de la posició 0 fins abans de la 4". Les posicions comencen a comptar des de 0.


### Eliminar espais en blanc (trim)
És habitual que una cadena tingui espais abans o després que volem eliminar. Per això, Python té mètodes per treure aquests espais:

strip() elimina espais a l'inici i final.

lstrip() només elimina espais a l'inici.

rstrip() només elimina espais al final.

Exemple:

```Python
text = "   hola món   "
print(text.strip())   # Sortida: "hola món"
print(text.lstrip())  # Sortida: "hola món   "
print(text.rstrip())  # Sortida: "   hola món"
```
### Canviar majúscules/minúscules
Python permet canviar totes les lletres a majúscula o minúscula amb:

upper() passa tot a majúscules.

lower() passa tot a minúscules.

title() posa en majúscula la primera lletra de cada paraula.

Exemple:

```Python
text = "hola món"
print(text.upper())  # Sortida: "HOLA MÓN"
print(text.lower())  # Sortida: "hola món"
print(text.title())  # Sortida: "Hola Món"
```
### Buscar una subcadena
Per saber si una paraula o caràcter apareix dins d’una cadena, utilitzem:

in per comprovar si hi és.

find() retorna la posició de la primera aparició o -1 si no hi és.

Exemple:

```Python
text = "Hola món"
print("món" in text)       # True
print(text.find("món"))    # 5
print(text.find("Python")) # -1 (no hi és)
```
### Reemplaçar text
Pots substituir parts d’una cadena amb replace():

```Python
text = "Hola món"
nou_text = text.replace("món", "Python")
print(nou_text)  # Sortida: Hola Python
```

### Dividir i unir cadenes
split() separa una cadena en llista de paraules o elements segons un separador.

join() uneix elements d'una llista en una cadena separada per un text.

Exemple:

```Python
text = "un dos tres"
llista = text.split()  # ['un', 'dos', 'tres']
print(llista)

frase = " ".join(llista)
print(frase)  # Sortida: "un dos tres"

frases = ["Bon dia", "com", "estàs", "avui?"]
resultat = " *** ".join(frases)
print(resultat)   # Sortida:  Bon dia *** com *** estàs *** avui?
```
En aquest exemple, el mètode join() uneix totes les cadenes de la llista frases separant-les amb la cadena " *** ". Pots posar qualsevol text com a separador.

# 2.2. Operadors

## 2.2.1 Operadors aritmètics

|Operador | Descripció | Exemple |
|---|---|---|
|+	|Suma	|4 + 3 (= 7)|
|-	|Resta |	10 - 5 (= 5)|
|*	|Multiplicación	| 3 * 4 (= 12)|
|/	|División	| 5 / 2 (= 2.5)|
|//	|División entera	|5 // 2 (= 2)|
|%	|Módulo |	5 % 2 (= 1)|
|**	|Exponenciación	|2 ** 3 (= 8)|

## 2.2.2 Operadors relacionals

| Operador | Descripció | Exemple |
|---|---|---|
|==|Igual|(3 + 1) == (2 ** 2)|
|!=| Diferente| 0 != 1|
|> |Mayor que| 3 > 2|
|< |Menor que| 2 < 3|
|>=|Mayor o igual que|3 >= (2 + 1)|
|<=|Menor o igual que|2 <= 5 |


## 2.2.3 Operadors lògics

|Operador | Descripció | Exemple |
|---|---|---|
|and	|Retorna True si ambos operandos son verdaderos y False en caso contrario	|(1 < 2) and (4 > 3) [= True]|
|or	|Retorna True si al menos uno de los operados es verdadero y False en caso contrario	|(10 > 20) or (40 < 30) [= False]|
|not	|Retorna True si el operando el falso y False en caso contrario	|not (4 > 2) [= False]|


**Operadors combinats**: menys línies, mateixa força

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

---

<div style="justify-content: space-between;">
<p style="display:inline; display: flex; justify-content: space-between; width: auto;">
       <span><a href="/apunts/1-introduccio.html">← 1. Introducció</a></span>
       <span><a href="/apunts">Índex</a></span>
       <span><a href="/apunts/3-control_flux.html">3. Control de flux: Condicionals i bucles →</a></span>
</p>
</div>
