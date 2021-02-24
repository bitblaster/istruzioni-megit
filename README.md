# Cos'è MeGit
MeGit è un client Git basato sull'ambiente di sviluppo Eclipse, installando solo il numero minimo possibile di componenti necessari per la gestione di Git.
I vantaggi rispetto ad altri client Git sono:
1. è molto semplice da usare ma potente al tempo stesso
1. è open-source e gratuito
1. è abbastanza compatto e non usa molto spazio su disco

# Installazione di MeGit
Innanzitutto creare una directory (cartella) all'interno della quale andremo ad installare MeGit.
Ad es. potremmo installarlo nella nostra directory _home_ (Windows: C:\\Users\\\<username\>\\MeGit, Linux: /home/\<username\>/MeGit, Mac: /Users/\<username\>/MeGit) o in qualunque altra posizione in cui abbiamo i permessi di scrittura.

Da questo punto in avanti chiameremo questa directory **_\<MeGit_DIR\>_**

Dato che MeGit è un'applicazione Java, per funzionare ha bisogno di essere eseguita da una JVM (Java Virtual Machine). La distribuzione più essenziale di una JVM è il solo _runtime_ di esecuzione, detto JRE (Java Runtime Environment).

Per semplicità di installazione e configurazione andremo quindi a scaricare la JRE 11 da qui:
https://adoptopenjdk.net/archive.html

Scegliere la JRE 11 adatta al nostro sistema operativo (nota: i sistemi più diffusi sono architettura x86 a 64 bit, abbreviato con **x64**):
* Windows x64: https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.10_9.zip
* Linux x64: https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.10_9.zip
* Mac x64: https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.10_9.zip

Scompattare il contenuto dentro **_\<MeGit_DIR\>_** e rinominarlo in modo che si chiami **jdk11**. Verificare che all'interno siano subito presenti le directory **bin**, **conf**, ecc., come nell'immagine seguente:

![struct jdk](/images/struct_jdk.png)

Scaricare quindi MeGit, anche qui scegliendo la versione adatta alla propria piattaforma:
https://github.com/eclipsesource/megit/releases/tag/v0.0.2

Scompattare anche questo archivio dentro **_\<MeGit_DIR\>_**, in modo che la struttura finale sia simile all'immagine seguente:

![struct full](/images/struct_full.png)

Modificare con un editor di testo il file megit.ini e inserire all'inizio le seguenti righe:
```
-vm
jdk11/bin
```
Salvare il file, quindi lanciare il programma **megit** (o **megit.exe**)
