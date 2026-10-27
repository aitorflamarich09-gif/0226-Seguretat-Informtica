## Fase 1: Anàlisi i Justificació (Document d'Informe)
Heu de redactar un informe que justifiqui tècnicament la decisió de la Direcció i comparin les opcions. Aquest informe ha d'incloure:

1. Introducció i Justificació:

- Explicació de perquè les contrasenyes febles o reutilitzades són un risc crític per a l'empresa (atac de diccionari, credential stuffing, etc.)

**Tenir contrasenyes febles o reutlitzades es un risc, perque si son reutlizitades, el primer que fan nomes troben una contrasenya teva es probar aquesta contraseña en tots els llocs hon tu estas registrat, pero si les contrasenyes son febles el problema es que en un atack que li fan al servidor, poden treure la teva contrasenya d'una manera molt rapida i facil, ya que no es cumplicada, en un atac de diccionari si la contrasenya es feble tarda segons en ser crackegada, i si a aixo li posem que l'utilizes per tots els llocs, ya poden entrar hon ells vulguin**

- La funció crucial d'un gestor de contrasenyes per mitigar aquests riscos.

**Un gestor de contrasenyes és una eina que serveix per guardar i crear contrasenyes de manera segura ja que normalment solen ser mold extranyes. És molt útil perquè permet tenir una contrasenya diferent per a cada compte sense haver de memoritzar-les totes.**


2. Comparativa Tècnica: Realitzeu una taula comparativa detallada entre:
- **Bitwarden (Alternativa Online / Núvol): Analitzeu la sincronització, el model de seguretat (xifratge end-to-end), la facilitat d'accés des de múltiples dispositius i el cost/model freemium.**

- **KeePassX / KeePassXC (Alternativa Offline / Escriptori): Analitzeu l'emmagatzematge local de l'arxiu (KDBX), la independència del núvol, el model open source i la portabilitat de l'arxiu.**

# Comparativa tècnica: Bitwarden vs KeePassXC

| Característica | Bitwarden (núvol) | KeePassXC (local) |
|---|---|---|
| Sincronització | Automàtica entre dispositius. | Manual o amb serveis externs. |
| Seguretat | Xifratge d'extrem a extrem. | Base de dades xifrada amb AES-256 o altres algoritmes compatibles. |
| Accés | Ordinadors, mòbils i navegadors. | Cal disposar del fitxer de contrasenyes i de l'aplicació compatible. |
| Emmagatzematge | Núvol amb dades xifrades. | Fitxer local `.kdbx`. |
| Dependència del núvol | Sí, per a la sincronització habitual. | No, funciona sense Internet. |
| Codi obert | Sí. | Sí. |
| Cost | Versió gratuïta i plans de pagament. | Gratuït. |
| Portabilitat | Accés des de diferents dispositius amb el mateix compte. | El fitxer es pot copiar a un USB o transferir a altres dispositius. |
| Avantatge principal | Comoditat i sincronització automàtica. | Control local de les dades. |
| Inconvenient principal | Depèn del servei al núvol. | Cal gestionar les còpies de seguretat i la sincronització. |




3. Avantatges i Inconvenients: Resumiu els principals pros i contres de cada model (online vs. offline) des del punt de vista de seguretat, usabilitat i continuïtat del negoci.


### Bitwarden (Online / Núvol)

**Avantatges:**
- Sincronitza les contrasenyes automàticament entre dispositius.
- Utilitza xifratge d'extrem a extrem per protegir les dades.
- És fàcil d'utilitzar i permet accedir a les contrasenyes des de qualsevol lloc amb Internet.
- Facilita la continuïtat del negoci si un dispositiu es perd o es canvia.

**Inconvenients:**
- Depèn del servei al núvol per sincronitzar les dades.
- Cal protegir bé el compte principal.
- Algunes funcions són de pagament.

### KeePassXC (Offline / Local)

**Avantatges:**
- Les contrasenyes es guarden localment i no depenen del núvol.
- Permet tenir més control sobre les dades.
- És gratuït i de codi obert.
- Es pot utilitzar sense connexió a Internet.

**Inconvenients:**
- La sincronització entre dispositius és més complicada.
- Si es perd o es fa malbé el fitxer sense tenir una còpia de seguretat, es poden perdre totes les contrasenyes.
- Requereix més gestió manual i pot ser menys còmode per treballar en equip.


4. Recomanació: Concloeu l'informe escollint l'eina que considereu més adequada per al personal tècnic de l'empresa i justifiqueu la vostra elecció.

**La meva recomanació és utilitzar Bitwarden, ja que és una eina fàcil d'utilitzar i permet sincronitzar les contrasenyes entre diferents dispositius. A més, utilitza xifratge d'extrem a extrem i permet compartir credencials de manera controlada amb les funcions adequades.**

## Fase 2: Guia d'Ús Tècnica (Manual Operatiu)
Utilitzant l'eina que heu seleccionat a la Fase 1 (Bitwarden, KeePassX, o similar), heu de crear una Guia d'Ús per a l'Equip Tècnic. Aquesta guia ha de ser clara i basada en captures de pantalla i instruccions pas a pas.

La guia ha de cobrir els següents punts obligatoris:

1. Instal·lació i Configuració Inicial: Descàrrega, instal·lació i creació de la BBDD principal o compte mestre.

- Busquem la applicacio bitwarden
![](/NF1.AA3-Gestor-de-contrasenyes/img/Bitwarden%20google.png)

- PAra que ya estem dins de la web
![](/NF1.AA3-Gestor-de-contrasenyes/img/Dins.png)

- Aqui es descarega la app
![](/NF1.AA3-Gestor-de-contrasenyes/img/Guardar.png)

- Aqui ponem hon volem que es descaregui
![](/NF1.AA3-Gestor-de-contrasenyes/img/unnamed.png)

- Procés d’instal·lació del programa al sistema.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Descargan-se.png)

- Una vegada la app descaregada l'app la obrim.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Obrir.png)

- L’aplicació ja oberta, preparada per iniciar la configuració inicial, si no tens conte li dones a crear conte.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Obrir%20app.png)

- Pantalla de creació del compte mestre de Bitwarden.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Crear%20cuenta.png)

- Una vegada ja has fet el compte, t'arriba un correu.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Correo.png)

- Introducció de la contrasenya del compt, te que ser segura i tenir com a minim 12 caracters.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Contra.png)

- Inici de sessió al compte de Bitwarden després del registre.
![](/NF1.AA3-Gestor-de-contrasenyes/img/log.png)

- Ara posem la contra per iniciar sesio
![](/NF1.AA3-Gestor-de-contrasenyes/img/Contraseña.png)

2. Generació de Contrasenyes Segures: Explicació de com utilitzar el generador de contrasenyes de l'eina (paràmetres, longitud, caràcters especials).

- Generador de contrasenyes de Bitwarden, on es pot configurar la longitud, la complexitat i els caràcters especials perquè la contrasenya sigui segura i difícil de forçar.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Configurar%20contra%20gen.png)

3. Exemples d'Ús i Emplenament Automàtic:

- Prova del funcionament del gestor de contrasenyes amb un exemple, poses el nom de el que guardes, i es genera la contra, una vegada ja esta li donem a save.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Proba.png)

- Exemple d’una contrasenya de compte guardada per a un lloc web, posem el nom de la web, el nom d'usuari, i despres li donem al boto del cosatat en el apartat de contra y es genera la contra depenet del que nosaltres volem.
![](/NF1.AA3-Gestor-de-contrasenyes/img/web%20contra.png)

- Visualització de la contrasenya generada i emmagatzemada per a una pàgina web, tambe podem posar un authentificator key, per si perdem alc otnra, i l'enllaç a la web.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Contra%20web%202.png)

- Extensió de Bitwarden integrada al navegador per omplir credencials de manera automàtica.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Extension.png)

- Procés per afegir la extensió del navegador.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Agregar%20extension.png)

- Configuració de la extensió perquè s’integri correctament amb el navegador i el compte.

![](/NF1.AA3-Gestor-de-contrasenyes/img/Extension%20config.png)

- Inici de sessió des de la extensió de Bitwarden.

![](/NF1.AA3-Gestor-de-contrasenyes/img/Login.png)

- Introducció del correu electrònic dins de la extensió per autenticar-se.
![](/NF1.AA3-Gestor-de-contrasenyes/img/correo%20extension.png)

- Introducció de la contrasenya del compte des de la extensió.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Contra%20extension.png)

- Comprovació final que l’emplenament automàtic i l’autenticació funcionen correctament.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Proba%20extension.png)

4. Gestió de Còpies de Seguretat (Backup):

- Opció d’exportació de les dades del gestor de contrasenyes per crear una còpia de seguretat.

![](/NF1.AA3-Gestor-de-contrasenyes/img/Export.png)

- Pantalla de l’exportació del fitxer de còpia de seguretat.
![](/NF1.AA3-Gestor-de-contrasenyes/img/exportar%20j.png)

- Confirmació del procés d’exportació o backup abans de guardar-lo.
![](/NF1.AA3-Gestor-de-contrasenyes/img/COnfirmacios.png)

- Elecció de la ubicació on es guardarà la còpia de seguretat.
![](/NF1.AA3-Gestor-de-contrasenyes/img/Donde%20guardar.png)

### Recomanacio
Per guardar aquest arxiu on estan totes les contraseñas, ho podeu guardar en un disc dur extern, o en un USB xifrat.