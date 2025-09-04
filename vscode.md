# VS Code


## 1\. Instal·lar VS Code a Ubuntu

La forma més senzilla i recomanada d'instal·lar VS Code a Ubuntu és mitjançant el gestor de paquets Snap. Això assegura que sempre tindràs la versió més recent i actualitzada.

1.  **Obre el terminal:** Pots fer-ho prement `Ctrl + Alt + T` o buscant "Terminal" al menú d'aplicacions.

2.  **Instal·la VS Code via Snap:** Escriu la següent comanda i prem Enter. Se't demanarà la teva contrasenya d'usuari.

    ```bash
    sudo snap install --classic code
    ```

      * `sudo`: Executa la comanda amb privilegis d'administrador.
      * `snap install`: Comanda per instal·lar un paquet Snap.
      * `--classic`: VS Code necessita accés a parts del teu sistema que normalment estan restringides per als Snaps, per això usem aquesta opció.
      * `code`: El nom del paquet de VS Code.

3.  **Verifica la instal·lació (opcional):** Un cop finalitzada la instal·lació, pots verificar que VS Code s'ha instal·lat correctament executant:

    ```bash
    code --version
    ```

    Això et mostrarà la versió de VS Code instal·lada.

Ja pots tancar el terminal. Ara podràs trobar VS Code al teu menú d'aplicacions i obrir-lo com qualsevol altre programa.

-----

## 2\. Preparar VS Code per a Markdown (Extensions Essencials)

Un cop VS Code estigui instal·lat, el següent pas és afegir les extensions que milloraran la teva experiència amb Markdown i et permetran crear diapositives, PDFs i pàgines web.

Per instal·lar extensions:

1.  **Obre VS Code.**
2.  Fes clic a la icona de les **Extensions** a la barra lateral esquerra (sembla un quadrat amb un altre quadrat sortint). Alternativament, pots prémer `Ctrl + Shift + X`.
3.  A la barra de cerca que apareix, escriu el nom de cada extensió i fes clic al botó **Instal·lar** que apareix al costat de cada una.

-----

### **Extensió 1: Markdown All in One (Indispensable per escriure Markdown)**

  * **Cerca a l'apartat d'extensions:** `Markdown All in One`
  * **Per què:** Aquesta extensió és bàsica per a qualsevol que escrigui Markdown. Et facilitarà la vida amb:
      * **Autocompletat** per a la sintaxi Markdown.
      * **Dreceres de teclat** per aplicar format ràpidament (negreta, cursiva, etc.).
      * **Millores a la previsualització** de Markdown de VS Code, incloent desplaçament sincronitzat.
      * **Generació de taules de continguts** automàtiques.

-----

