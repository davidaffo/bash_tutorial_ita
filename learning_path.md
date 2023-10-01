## Imparare la riga di comando Bash: Checklist

### Livello 1: Principiante
=================

1.1 Navigare nelle directory
------------------------

- Controllare la directory di lavoro corrente con `pwd`
- Elencare il contenuto della directory corrente con `ls -la`
- Cambiare la directory corrente sia verso l'alto che verso il basso con `cd`
- Spiegare la differenza tra un percorso relativo e assoluto
- Digitare più velocemente con i tasti di scelta rapida `TAB` e `UPARROW`

1.2 Esaminare i file di testo
----------------------

- Elencare il contenuto di un file con `cat`, `less` o `more`
- Cercare parole all'interno di file di testo con `grep`
- Visualizzare le differenze tra file di testo con `diff`
- Modificare un file di testo con `nano` o `vi/vim`

1.3 Copiare e spostare file
-----------------------

- Copiare uno o più file con `cp`
- Rinominare o spostare un file o una directory con `mv`
- Rimuovere un file con `rm`
- Rimuovere una directory con `rmdir`

### Livello 2: Intermedio
=====================

2.1 Permessi
---------------

- Cambiare i permessi di un file con `chmod`
- Spiegare il significato dei 9 bit di permesso su un file
- Cambiare la proprietà di un file con `chown` o `chgrp`
- Ignorare i privilegi utente con `sudo`

2.2 Pipe
---------

- Reindirizzare l'output di un programma a un file di testo
- Reindirizzare l'output di un programma a un altro programma
- Filtrare, ordinare, deduplicare e contare righe/parole all'interno di una pipeline
- Separare i flussi `stdout` e `stderr`

2.3 Rete
--------------

- Accedere a un sistema remoto con `ssh`
- Copiare file tra un sistema remoto e locale con `scp`
- Scaricare un file dal Web con `curl` o `wget`

2.4 Controlli di sistema
-----------------

- Controllare l'utilizzo del disco con `df`
- Controllare le dimensioni delle directory con `du`
- Elencare i processi in esecuzione con `pwd` o `top`
- Terminare un processo con `kill` o `xkill`

2.5 Amministrazione di sistema
-------------------------

- Impostare una variabile d'ambiente con `export`
- Impostare una variabile d'ambiente in modo permanente nel file `.bashrc`
- Eseguire uno script bash con `source`
- Installare un programma con `apt` (Debian/Ubuntu) o `yum` (RedHat)
- Compilare un programma usando `make`
- Installare Linux sul tuo laptop
- Spiegare cosa contengono directory come `/bin`, `/usr`, `/etc` e `/boot`
- Aggiungere più utenti e gruppi

### Livello 3: Avanzato
=================

3.1 Amministrazione
-------------------

- Avviare un cronjob
- Configurare un servizio nella directory `/env`
- Conoscere le differenze tra le distribuzioni Linux
- Compilare un pacchetto da zero
- Caricare moduli del kernel o compilare un kernel Linux

3.2 Rete
--------------

- Eseguire strumenti per analizzare il traffico di rete
- Configurare una rete locale
- Installare Linux su più macchine remote contemporaneamente

3.3 Scripting
--------------

- Scrivere uno script di installazione per una macchina remota
- Scrivere script bash che contengono variabili, loop e dichiarazioni condizionali
- Elaborare i log di sistema automaticamente
- Enumerare più di 50 comandi bash
