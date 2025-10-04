# Exercicis resolts amb variables i print
### Exercici 1: Suma de dos nombres

Declara dues variables numèriques, es sumen amb + i es mostra el resultat.

Solució:
```Python
a = 5
b = 7
suma = a + b
print("La suma de", a, "i", b, "és:", suma)
```

### Exercici 2: Calcula l'àrea d'un cercle
Utilitza una variable per a π, una altra per al radi i l’operador de potència ** per calcular l’àrea.

```Python
PI = 3.14159
radi = 4
area = PI * (radi ** 2)
print("L'àrea del cercle és:", area)
```

### Exercici 3: Conversió Celsius a Fahrenheit

Utilitza variables i operadors aritmètics per transformar temperatures.

```Python
celsius = 25
fahrenheit = (celsius * 9 / 5) + 32
print(celsius, "graus Celsius són", fahrenheit, "graus Fahrenheit")
```

### Exercici 4: Operacions amb variables

Practica amb diversos operadors matemàtics d’assignació combinada (+=, -= etc).

```Python
x = 10
x += 5    # suma 5
x *= 2    # multiplica per 2
x -= 4    # resta 4
x //= 3   # divisió entera
print("Resultat final:", x)
```
### Exercici 5: Resta, multiplicació i mòdul
Es treballa amb resta (-), multiplicació (*) i mòdul (%).

```Python
num1 = 13
num2 = 4
resta = num1 - num2
multiplicacio = num1 * num2
modul = num1 % num2
print("Resta:", resta)
print("Multiplicació:", multiplicacio)
print("Mòdul:", modul)
```

# Exercicis amb condicionals i entrada i sortida per pantalla

### Exercici 6: Determinar si un nombre és parell o senar

```Python
num = int(input("Introdueix un nombre enter: "))

if num % 2 == 0:
    print("El nombre és parell.")
else:
    print("El nombre és senar.")
```
Explicació: Es llegeix un nombre, s’utilitza l’operador mòdul % i s’aplica la condició per saber si és parell o senar.

### Exercici 7: Major de dos nombres

compara dos variables amb operadors relacionals i es mostra quin nombre és més gran, o si són iguals.

```Python
a = int(input("Introdueix el primer nombre: "))
b = int(input("Introdueix el segon nombre: "))

if a > b:
    print(a, "és més gran que", b)
elif a < b:
    print(b, "és més gran que", a)
else:
    print("Els dos nombres són iguals.")
```


### Exercici 8: Classificar una nota

Utilitza condicionals múltiples per classificar la nota segons el seu valor.

```Python
nota = float(input("Introdueix la teua nota (0-10): "))

if nota >= 9:
    print("Excel·lent")
elif nota >= 7:
    print("Notable")
elif nota >= 5:
    print("Aprovat")
else:
    print("Suspès")
```


### Exercici 9: Comprovar si una persona és major d’edat

Demana una edat i utilitza una condició per mostrar el missatge adequat.

```Python
edat = int(input("Quina edat tens? "))

if edat >= 18:
    print("Ets major d'edat.")
else:
    print("Ets menor d'edat.")
```


### Exercici 10: Positiu, Negatiu o Zero

Permet classificar el nombre introduït segons el seu signe utilitzant condicionals.

```Python
x = float(input("Introdueix un nombre: "))

if x > 0:
    print("El nombre és positiu.")
elif x < 0:
    print("El nombre és negatiu.")
else:
    print("El nombre és zero.")
```



---
# Exercicis per practicar funcions de strings

### Exercici 11: Extraure un substring
Enunciat: Donada una cadena, extrau una subcadena des de l'índex 2 fins a l'índex 5 (sense incloure'l).

Solució:

```Python
text = "Python"
sub = text[2:5]  # Comença en posició 2 fins abans de 5
print(sub)  # Sortida: tho
```
### Exercici 12: Treure espais a les dues bandes
Enunciat: Donada una cadena amb espais al davant i darrere, elimina aquests espais.

Solució:

```Python
text = "   hola món   "
neteja = text.strip()  # Elimina espais a l'inici i final
print(neteja)  # Sortida: hola món
```
### Exercici 13: Pasar a majúscules i buscar
Enunciat: Passa una cadena a majúscules i comprova si conté la paraula "PYTHON".

Solució:

```Python
text = "M'agrada python"
text_up = text.upper()
print(text_up)  # M'AGRADA PYTHON
print("PYTHON" in text_up)  # True
```
### Exercici 14: Reemplaçar una paraula
Enunciat: Substitueix la paraula "dolor" per "alegria" en la frase donada.

Solució:

```Python
frase = "El dolór és fort"
nova = frase.replace("dolor", "alegria")
print(nova)  # Sortida: El alegria és fort
```
### Exercici 15: Unir una llista amb un separador (les llistes s'expliquen al tema 5)
Enunciat: Uneix una llista de paraules separades per un guió "-".

Solució:

```Python
paraules = ["un", "dos", "tres"]
resultat = "-".join(paraules)
print(resultat)  # Sortida: un-dos-tres
```

<div style="justify-content: space-between;">
<p style="display:inline; display: flex; justify-content: space-between; width: auto;">
       <span><a href="/apunts">Índex</a></span>
</p>
</div>
