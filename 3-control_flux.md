


## 3.- Estructures de control de flux.

1. Introducció general al control de flux en Python
Quan cuinem, no seguim sempre una recepta estricta. Observem què tenim a la nevera, prenem decisions sobre la marxa i adaptem
la preparació segons els ingredients, el temps o el gust del moment. En programació, fem exactament el mateix: prenem decisions i
repetim accions segons les condicions i les dades disponibles.

Aquest procés de decidir què fer i quan fer-ho és el que anomenem control de flux. En Python, tenim unes eines molt potents per
fer això: estructures condicionals i bucles. Aquestes ens permeten que el programa s’adapti, que prengui decisions, i que
repeteixi accions quan calgui.


Podem veure el flux d’un programa com un cuiner que segueix una recepta oberta:

* Si té ous, fa una truita.
* Si no en té però té pa, fa torrades.
*  Si no té res, es fa un cafè.

Això, en codi, és un if - elif - else.


També, quan ha de barrejar la massa durant 10 voltes, això és un bucle for.
I si ha d’esperar fins que l’aigua bulli, això seria un bucle while.

Vegem ara, pas a pas, aquestes estructures de control de flux en Python amb analogies culinàries.


1.1. Condicionals: if, elif, else

Aquesta estructura permet prendre decisions. El programa revisa si es compleix una condició (if) i, segons el cas, executa un bloc
de codi. Si la primera condició no es compleix, pot mirar altres opcions (elif), i si cap condició es compleix, hi ha una última acció per
defecte (else).

És com quan entres a la cuina i decideixes què fer:

“Si tinc ous, faig truita; si no, però tinc pa, faig torrades; i si no tinc res, faig un cafè.”

```Python
tinc_ous = True
tinc_pa = False

if tinc_ous:
    print("Faig una truita.")
elif tinc_pa:
    print("Faig torrades.")
else:
    print("Faig un cafè.")
```

Explicació detallada:
* if comprova la primera condició: tens ous?
* elif (abreviació de “else if”) ofereix una segona opció: no tens ous, però tens pa?
* else és el cas per defecte: no tens ni ous ni pa? Fes el que puguis.

Això permet al programa actuar de manera flexible segons el context.





1.2. match: selecció estructurada (com un switch modern)

La instrucció match és una característica més nova de Python (disponible des de la versió 3.10). Permet comprovar múltiples valors possibles d’una sola variable, d’una manera molt llegible. És molt útil quan tens moltes opcions a triar segons un sol
element.

És com tenir un menú i decidir què cuinar segons el plat escollit.

“Segons el plat que em demanis, prepararé una recepta diferent.”

```Python
plat = "paella"

match plat:
    case "truita":
        print("Bato els ous i faig una truita.")
    case "entrepà":
        print("Poso el pernil al pa")
    case "paella":
        print("Començo a sofregir l'arròs i afegeixo marisc")
    case _:
        print("No conec aquest plat, improviso una amanida")
```


Explicació detallada:
* match plat: obre la comparació.
* Cada case és una possible opció del valor.
* _ representa qualsevol altre cas (com else).

Aquesta estructura és ideal quan una sola variable pot tenir molts valors diferents.






1.3. Bucle for

El bucle for s’utilitza per repetir una acció un nombre determinat de vegades. No cal que tinguem una llista; simplement podem dir:

“Remeno la sopa 5 vegades.”

Això ho podem fer fàcilment amb range() en Python.

```Python
for volta in range(5):
    print(f"Remeno la sopa - volta {volta + 1}")
```

Explicació detallada:
* range(5) genera els nombres del 0 al 4 (és a dir, 5 voltes).
* A cada volta, la variable volta conté el número actual de la repetició.
* Sumem +1 perquè als humans ens agrada comptar des de l’1, no des de l’0.





1.4. Bucle while

El bucle while repeteix una acció mentre una condició sigui certa. És ideal quan no saps exactament quantes vegades hauràs de
repetir una acció. Com remenar una salsa fins que quedi espessa.

“Segueixo remenant la salsa fins que espesseixi.”

```Python
espessor = 0

while espessor < 5:
    print(f"Remenant la salsa... nivell d'espessor: {espessor}")
    espessor += 1

print("La salsa ja està llesta.")
``` 

Explicació detallada:
* El bucle continua mentre espessor < 5.
* Cada volta, augmentem el valor d’espessor amb espessor += 1.
* Quan espessor arriba a 5, el bucle s’atura i es passa a la següent línia.

Aquest tipus de bucle és molt útil quan volem esperar una “condició real”, com un temporitzador, una acció de l’usuari o un estat físic.





1.5. Conclusió

Les estructures de control de flux són fonamentals per escriure programes intel·ligents, adaptables i útils. Igual que un bon cuiner sap
improvisar i adaptar-se al que té, un bon programador sap com fer que el seu codi prengui decisions i repeteixi accions de manera
eficient.

Python ens proporciona estructures senzilles però molt potents per fer això:

* if / elif / else per prendre decisions
* match per gestionar múltiples opcions de manera clara
* for per repetir accions sobre col·leccions o un nombre fix de vegades
* while per repetir accions segons condicions dinàmiques

Amb aquests ingredients, pots cuinar qualsevol recepta digital.