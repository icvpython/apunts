



## 5.- Funcions i modularitat.



1.3. Funcions declaratives
Les funcions declaratives (o funcions definides per l’usuari) són aquelles que es creen explícitament en el nostre codi per fer una
tasca concreta. A diferència de les funcions integrades que ja venen amb Python (print(), len(), sum()...), les declaratives les
definim nosaltres mateixos, segons les necessitats del nostre programa.
És com escriure la teva pròpia "recepta" personalitzada per resoldre un problema. La sintaxi d'una funció és la següent:
• La paraula def serveix per indicar que estàs definint una funció.
• El nom de la funció ha de seguir les regles habituals dels noms (sense espais, començant per lletra...).
• Els paràmetres (entre parèntesis) són opcionals: poden haver-n'hi o no.
• El cos de la funció (les instruccions) s’escriu amb sagnat (indentació).


Ve a ser una plantilla, com en els documents de text evita repetir codi 

def nom_de_la_funcio(paràmetres):
    # instruccions que executarà



1.4. Cridar una funció
Un cop tenim una funció definida o volem utilitzar una funció integrada, cal cridar-la perquè s’executi. "Cridar" (invocar o llamar) una
funció vol dir dir-li a Python que executi aquella acció que hem definit o que ja existeix.
Imagina que tens una recepta que es diu fer_truita(). Aquesta recepta només es cuina si tu la tries. Doncs en programació és
igual: si no crides la funció, el codi que hi ha dins no s’executa.
Per cridar una funció en Python, simplement escrivim el seu nom seguit de parèntesis:

fer_truita()

En el cas de voler cridar una funció integrada el procediment és el mateix:

len("patates")


Si la funció necessita informació per funcionar (anomenada paràmetres o arguments), la posem dins els parèntesis:

fer_truita("patates", "ous", "sal")


1.5. Paràmetres

Quan creem una funció, sovint volem que pugui treballar amb diferents valors, en lloc de fer sempre el mateix. Els paràmetres
(també anomenats arguments) són com caixes que porten informació a la funció perquè pugui fer la seva feina.
Imagina una funció fer_truita(). Si volem que pugui fer truites diferents (de patates, de carbassó, de formatge...), li hem de dir
quin ingredient volem utilitzar.

def fer_truita(ingredient):
    print("Estic fent una truita de " + ingredient)

fer_truita("patates")
fer_truita("carbassó")


Aquí ingredient és un paràmetre, i "patates" o "carbassó" són els arguments concrets que li passem quan la cridem. Per
defecte, s'ha de cridar una funció amb el nombre correcte d'arguments. Significa que si la vostra funció espera 2 arguments, heu de
cridar la funció amb 2 arguments, no més, i no menys.



1.6. Què fa return dins d’una funció?
La paraula clau return serveix per retornar un valor des de dins d’una funció cap a fora. Això vol dir que, quan la funció s’executa,
ens "torna" un resultat que podem guardar, imprimir o utilitzar en una altra operació.
És com si la funció fos una màquina: li dones dades, fa uns càlculs o processos interns i, al final, et torna un resultat pel forat de
sortida.

def fer_truita(ingredient):
    truita = "Truita de " + ingredient
    return truita

plat = fer_truita("patates"):
print("He cuinat:", plat)


Aquesta funció ens retornarà la cadena de text que conté la variable truita, la qual es guardarà a la variable plat.



