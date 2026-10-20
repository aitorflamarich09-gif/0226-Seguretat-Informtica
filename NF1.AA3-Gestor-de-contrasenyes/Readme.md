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
*

4. Recomanació: Concloeu l'informe escollint l'eina que considereu més adequada per al personal tècnic de l'empresa i justifiqueu la vostra elecció.

**La meva recomanació és utilitzar Bitwarden, ja que és una eina fàcil d'utilitzar i permet sincronitzar les contrasenyes entre diferents dispositius. A més, utilitza xifratge d'extrem a extrem i permet compartir credencials de manera controlada amb les funcions adequades.**

## Fase 2: Guia d'Ús Tècnica (Manual Operatiu)
Utilitzant l'eina que heu seleccionat a la Fase 1 (Bitwarden, KeePassX, o similar), heu de crear una Guia d'Ús per a l'Equip Tècnic. Aquesta guia ha de ser clara i basada en captures de pantalla i instruccions pas a pas.

La guia ha de cobrir els següents punts obligatoris:

1. Instal·lació i Configuració Inicial: Descàrrega, instal·lació i creació de la BBDD principal o compte mestre.
2. Generació de Contrasenyes Segures: Explicació de com utilitzar el generador de contrasenyes de l'eina (paràmetres, longitud, caràcters especials).
3. Exemples d'Ús i Emplenament Automàtic:
- Com desar una credencial d'un compte de correu electrònic.
- Com desar una credencial d'una aplicació o servei web.
- Com fer servir l’extensió del navegador per emplenar automàticament les dades.
4. Gestió de Còpies de Seguretat (Backup):
- Explicació detallada de com fer una còpia de seguretat de l'arxiu de contrasenyes (KDBX en KeePass o Exportació en Bitwarden).
- Recomanació de la millor pràctica per emmagatzemar aquesta còpia de seguretat de forma segura (clau USB xifrada o emmagatzematge xifrat al núvol).