# 4. Entrades i sortida per pantalla: les funcions input() i print()

## 4.1 Entrada de teclat en Python: la funció `input()`

No hi ha molts programes sense cap entrada. L'entrada pot venir d'una base de dades, una altra computadora, clics i moviments del ratolí o des d'Internet. Tot i així, en la majoria dels casos, l'entrada prové del teclat. A aquest efecte, Python proporciona l'entrada de la funció `input()`.

Si es crida a la funció `input()`, el flux del programa es detindrà fins que l'usuari hagi donat una entrada i hagi finalitzat l'entrada amb la tecla de retorn. El text del paràmetre és opcional i serà imprès a la pantalla. L'entrada de l'usuari serà retornada com una cadena. Si aquesta cadena s’ha de transformar en un altre tipus de dada, podem utilitzar una funció de càsting o la funció `eval`.

## Exemple bàsic d'ús

```Python
nom = input("Escriu el teu nom: ")
print("Hola " + nom + "!")
```


## Entrada numèrica

La funció `input()` retorna sempre una cadena de text (`str`). Si vols treballar amb nombres, cal transformar la cadena al tipus adequat amb `int()` o `float()`:

```Python
edat = int(input("Introdueix la teua edat: "))
print("Tens ", edat, " anys.")
```


## Operacions matemàtiques amb l'input

Si l’usuari introdueix un nombre i després el vols utilitzar per càlculs, has de transformar-lo:

```Python
nombre = input("Introdueix un nombre: ")
mitat = float(nombre) / 2
print("La meitat és:", mitat)
```


## Exemple combinat

```Python
nom = input("Quin és el teu nom? ")
print("Encantat de conèixer-te " + nom + "!")
edat = input("Quina edat tens? ")
print("Encara tens " + edat + " anys, " + nom + "!")
```



# 4.2 Sortida per pantalla amb la funció print ()
La sortida estàndard d’un programa és la pantalla, i python te una instrucció per a imprimir per 
pantalla que és `print` i com a funció anirà acompanyada de parèntesi i esperarà un o més arguments.
Aquesta funció pot imprimir números, cadenes, caràcters,...
També permet donar-li format a la sortida.

**Exemples**

```Python
nom = "Eva"
edat = 20
alcada = 1.75
Print(f"Te llamas {nom}, tens {edat} anys i mesures {alcada} metres.")
# Te llamas Eva, tens 20 anys i mesures 1.75 metres.
print(f"Te llamas {nom}, tens {edat:4d} anys i mesures {alcada:8.3f} metres.")
# Te llamas Eva, tens 20 anys i mesures 1.750 metres.
# Si indiquem la quantitat de caràcters que volem imprimir com a mínim,
# aquest sistema per defecte utilitzarà una alineació esquerra, em canvi l’anterior amb
# "%" (o per defecte) dreta.
# Per canviar aquest comportament utilitzem els caràcters «<" (esquerra) i ">» (dreta).
for nom in ("Joan", "Pere", "Francesc", "Oscar", "Rafa"):
 print(f"{nom:>9}")

 a=453
 p=59.058
 print(f"Art: {a}, Price: {p}")
#'Art: 453, Price: 59.058'
 print(f"Art: {a:5d}, Price: {p:8.2f}")
#'Art: 453, Price: 59.06'
 print(f"Art: {a:10d}, Price: {p:.1f}")
#'Art: 453, Price: 59.1'
```

**Exemples de print amb el paràmetre END**

```Python
print ("hola ",end=" +") # imprimirà hola + i acaba amb un espai

 
print("Benvinguts a" , end = ' ') 
print("la classe de programació", end = ' ')
# La sortida serà una frase (sense salt de línia)  : "Benvinguts a la classe de programació"
```


## Resum

- **input()** recull text des del teclat i l’assigna a una variable.
- Si vols utilitzar l’entrada com a nombre, cal convertir la cadena amb **int()** o **float()**.
- Pots mostrar un missatge a l’usuari directament com a paràmetre de **input()**.
