## 5.- Estructures de dades bàsiques.

Les estructures de dades bàsiques de Python, és a dir, les eines que ens permeten emmagatzemar, organitzar i manipular col·leccions de dades d'una manera eficient i senzilla.

Igual que a la vida real fem servir diferents contenidors per a diferents coses (una motxilla per portar llibres, una safata per portar menjar, un arxivador per guardar documents), en programació també necessitem estructures específiques per tractar les dades segons les seves característiques i usos.

L'objectiu d'aquest apartat és veure:
* Quines són les estructures de dades fonamentals de Python.
* Com s’utilitzen per guardar i accedir a la informació.



### 5.1.- Tipus d'estructures

Cadascuna de les estructures que hi ha tenen una sintaxi diferent i, per tant, també tenen unes característiques o propietats diferents, això ens permetrà escollir entre diferents opcions depenent de l'ús que vulguem fer-hi.

A continuació teniu els diferents tipus d'estructures de dades que podem utilitzar a Python per guardar dades seguides d'un exemple on podeu observar la sintaxi:

*  Llistes (list): Per guardar col·leccions ordenades d’elements (com una llista de noms, notes, o objectes).
    ```Python
    llista = ["Pau", "Roger", "Eva"]
    ```
* Tuples (tuple): Com les llistes, però immutables (no es poden modificar).
    ```Python
    tupla = ("dilluns", "dimarts", "dimecres", "dijous", "divendres", "dissabte", "diumenge")
    ```

* Diccionaris (dict): Per guardar dades amb una clau i un valor, com una agenda de contactes o les notes d’un alumne.
    ```Python
    diccionari = {"nom:": "Paco", "nota": 8.5}
     ```
* Conjunts (set): Per guardar col·leccions sense duplicats i fer operacions com unió o intersecció.
    ```Python
    conjunt = {1, 2, 3, 4}
    ```


#### 5.1.1.- Llistes
Les llistes són col·leccions ordenades i modificables d’elements. 

Poden contenir números, textos o qualsevol altre tipus de dades,
fins i tot barrejats. 

Algunes de les característiques de les llistes són les següents:
* Els elements es poden modificar, afegir o eliminar.
* Poden haver-hi elements repetits.
* Cada element té una posició (índex) que comença per 0.
* Es declaren entre claus quadrades [].

Exemple de llista:
```Python
ingredients = ["ous", "patates", "sal"]
print(ingredients[0])
ingredients.append("ceba") 
```


.insert


.reverse



Recordeu que el text escrit després de # són comentaris i, per tant, no afecten l'execució de les instruccions.



|Mètode | Descripció |  
|:---:|:--- |  
|.append(x) |Afegeix l’element x al final de la llista.|
|.remove(x) |Elimina la primera ocurrència de l’element x.|
|.sort() | Ordena la llista (numèricament o alfabèticament).|
|.pop([i]) | Elimina i retorna l’element a la posició i (o l’últim si no s’indica).|



#### 5.1.2.- Tuples

Les tuples són col·leccions ordenades però immutables, és a dir, no es poden modificar després de ser creades. Són útils per representar dades fixes (com coordenades o dies de la setmana). 

Algunes de les característiques de les tuples són les següents:
* No es poden modificar (ni afegir ni eliminar elements).
* També tenen índexs com les llistes.
* Es declaren entre parèntesis ().


Exemple de tupla:
```Python
dies = ("dilluns", "dimarts", "dimecres", "dijous", "divendres", "dissabte", "diumenge")

print(dies[1])             # Mostra "dimarts"
```



#### 5.1.3.- Diccionaris

Els diccionaris són col·leccions ordenades (a partir de la versió de Python 3.7), on cada element té una clau i un valor. Són molt útils per emmagatzemar informació relacionada, com per exemple les dades d’un alumne. Algunes de les característiques dels diccionaris són els següents:

* Cada element és una parella clau: valor.
* Les claus han de ser úniques.
* Es declaren entre claus {}.
* Són modificables


Exemple de diccionari:
```Python
alumne = {"nom:": "Paco", "edat":16, "nota": 8.5}
print(alumne["nom"])    # Mostra "Paco"
alumne["nota"] = 9.0    # Modifica la nota
Exemple de llista:
```


En aquest cas tenim una clau anomenada "nom" i un valor "Carla", el qual el podem mostrar i modificar.

|Mètode | Descripció |  
|:---:|:--- |  
|.get(clau) | Retorna el valor associat a la clau, o None si no existeix.|
|.keys() | Retorna una llista amb totes les claus del diccionari.|
|.values() |Retorna una llista amb tots els valors del diccionari.|
|.items() | Retorna una llista de tuples amb cada parella (clau, valor).|


#### 5.1.4.- Conjunts

Els conjunts són col·leccions no ordenades i sense elements duplicats. Són útils per fer operacions com la unió, intersecció o diferència entre col·leccions.

Algunes de les característiques dels conjunts són els següents:
* No permeten duplicats.
* L’ordre dels elements no és garantit.
* Es declaren entre claus {} (com els diccionaris, però sense claus:valors).

Exemple de conjunt:
```Python
colors ={"vermell", "blau", "groc"}
colors.add("verd")  # Afegeix un color nou
colors.add("blau")  # No passa res, ja existeix al conjunt
```

Quan diem que una estructura no està ordenada, volem dir que els elements no tenen una posició fixa ni un índex que puguem controlar o preveure. Això passa amb els diccionaris (fins a Python 3.6) i especialment amb els conjunts.

A diferència de les llistes o tuples, on podem accedir als elements per la seva posició (llista[0], llista[1]...), en una
estructura no ordenada, no podem accedir-hi per índex, sinó per el nom del conjunt. Per exemple, en el codi de sota on tenim un
conjunt anomenat colors, si volem mostra-ho farem un print de tot el conjunt.

```Python
colors ={"vermell", "blau", "groc"}
print(colors)
```
Això ens retornara el següent:

```text
>>> {'vermell', 'blau', 'groc'}
```


|Mètode | Descripció |  
|:---:|:--- |  
|.add(x) | Afegeix l’element x al conjunt (si no hi és ja).|
|.union(altre_set) | Retorna un conjunt amb tots els elements dels dos conjunts.|
|.intersection(altre_set) | Retorna un conjunt amb els elements comuns als dos conjunts.|
|.difference(altre_set) | Retorna els elements que hi ha en el primer conjunt però no en l’altre.|