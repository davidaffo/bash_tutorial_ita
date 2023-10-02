La riga di comando di Bash
=====================

![*Tux, il pinguino Linux*](tux.png)

Questo tutorial ti renderà familiare con **bash**, la linea di comando di Linux. Imparerai a:

- navigare nelle directory
- manipolare file
- eseguire programmi

Se non hai esperienza precedente con sistemi simili a Unix o conosci alcuni comandi ma vuoi saperne di più, questo tutorial è per te.

### Prerequisiti

*Questo tutorial è stato preparato per Ubuntu Linux, ma funziona anche su MacOS,
Cygwin e Git bash, a condizione che Python 3 sia installato nel
sistema.*

----

## Obiettivo

In questo tutorial, cercherai una parola di 22 caratteri:

![](solution.png)

Tutti i caratteri sono nascosti negli esercizi seguenti.

## Preparativi

* clona il repository o scarica il codice come file ZIP
* individua la cartella `exercises/`
* apri un terminale `bash`

![](preparations.png)

----

## 1. Directory e file


### 1.1. Navigare nelle directory

Il **primo carattere** è nascosto in un file da qualche parte nella struttura delle directory di *exercise1*.
Utilizza i comandi

```bash
cd <nome_cartella>
```

(non digitare le parentesi angolari, inserisci solo il nome della cartella) e

```bash
ls
```

(per spostarti da una directory all'altra). Esplora le sottodirectory
fino a trovarne una con il nome `solution_1.1` e elenca i suoi contenuti.
Se sei entrato in una cartella sbagliata, puoi tornare indietro di un livello digitando:

```bash
cd ..
```

oppure tornare alla tua cartella home:

```bash
cd
```

### 1.2. Mostra un file nascosto

Alcuni file non sono immediatamente visibili. Per vederli, hai bisogno del
comando

```bash
ls -a
```

Il **secondo carattere** è nella stessa directory del primo, ma
in un file nascosto.

### 1.3. Esegui un programma

Usa `cd ..` per tornare alla directory `exercise_1/directoryB/`. Quando
elencate i suoi contenuti, dovresti vedere un **file di script shell**
`program.sh`. Per trovare il **terzo carattere**, devi eseguire il
programma. In bash, ciò viene fatto digitando `source` e il nome del
programma:

```bash
source program.sh
```

### 1.4. Scopri quanto è grande un file

Vai alla cartella `exercise_1/directoryC/`. Per trovare **il quarto
carattere**, devi scoprire quanto è grande il file di testo nella cartella.
Questo si fa con il comando

```bash
ls -l
```

Nella tabella prodotta dal comando, troverai la dimensione del file in byte,
il proprietario del file, le autorizzazioni per leggerlo e modificarlo, e la data/ora
della sua ultima modifica.

Per ottenere il quarto carattere, cerca la dimensione del file nella [Tabella di
caratteri ASCII stampabili](https://en.wikipedia.org/wiki/ASCII#Printable_characters):

![](ASCII-Table-wide.svg)

*Tabella ASCII, Pubblico Dominio*

<div class="admonition hint">

Quando digiti nomi di directory o file, premi `[TAB]` dopo i primi
pochi caratteri. Unix cerca di indovinare ciò che stai digitando.

</div>

----

## 2. Modifica file di testo

Usa `cd ..` per tornare alla directory principale del materiale del tutorial.
Quindi, entra nella directory `exercise_2`.

### 2.1. Visualizza cosa c'è in un file di testo

Nella directory *exercise\_2/*, troverai un file di testo
*solution\_2.1.txt*. Il **quinto carattere** è all'interno di quel file. Per vederne
il contenuto, usa il comando

```bash
less <nomefile>
```

### 2.2. Modifica file di testo

Per ottenere il **sesto carattere**, dovrai creare un file di testo in
la directory `exercise_2`. Su Ubuntu, puoi farlo usando l'editor
`nano`. Puoi avviarlo digitando il nome del programma, o

```bash
nano <nomefile>
```

**Per uscire da nano, digita Ctrl-X**

Crea un file di testo con i caratter

i che hai trovato finora.

Il **sesto carattere** è quello che devi premere per salvare un file in
`nano`.

<div class="admonition hint">

Se vuoi saperne di più su un comando specifico, digita

```bash
man <comando>
```

Verrà mostrata una pagina di aiuto che puoi chiudere premendo 'q'.

</div>

----

## 3. Copia ed elimina file

Vai alla directory `exercise_3`.

### 3.1. Crea una directory e copia un file in essa.

Per trovare **i caratteri sette e otto**, devi creare una
sottodirectory chiamata *solution* in `exercise_3/` e copiare i file da
le cartelle `part1/` e `part2/` dentro di essa.

Per creare directory, usa il comando:

```bash
mkdir <nomedirectory>
```

Per copiare, puoi usare il comando

```bash
cp <nomefile_da> <nomefile_a>
```

Digita `ls -l solution/*` dopo per vedere la soluzione.

### 3.2. Rimozione file

Nella directory `data`, devono essere eliminati tutti i file con una `Y`. Per farlo,
usa il comando:

```bash
rm <nomefile>
```

Inoltre, ci sono altri file da eliminare nella directory *data*. Per
rimuovere più di un file alla volta, puoi usare `*` come carattere jolly, cioè
`rm ju*` eliminerà tutti i file `junk.txt, juniper.txt` e `june.docx`.

Per ottenere **i caratteri nove e dieci**, guarda i file che rimangono dopo
aver eliminato tutti quelli che contengono una `Y`.

<div class="admonition hint">

Per rimuovere una directory vuota, puoi usare

```bash
rmdir <nomedirectory>
```

Il comando

```bash
rm -r <nomedirectory>
```

elimina una directory e tutto ciò che contiene.

</div>

<div class="admonition warning">

Su Unix, non è possibile recuperare i file eliminati!

Questo rende la rimozione di file con il simbolo `*` **molto** pericolosa,
perché potresti cancellare tutto con un singolo comando (ad esempio, se sbagli
a digitare la directory per errore). Dopo aver imparato questo comando,
i backup diventano un'idea ancora migliore.

</div>

----

## 4. Elaborazione dati di testo

Vai alla directory `exercise_4`.

### 4.1. Confronto di due file

Ci sono due versioni diverse di una citazione, `ai.txt` e
`artificial_intelligence.txt`. Per scoprire come differiscono, Unix
fornisce il comando

```bash
diff <nomefile1> <nomefile2>
```

Naturalmente, puoi guardare il testo prima usando `less` o `nano`. Il
**11° carattere** della soluzione è il singolo carattere in cui i due
file differiscono.

### 4.2. Ordinamento di un file di testo

Unix ha un piccolo programma per ordinare file di testo in ordine alfabetico. È chiamato
usando

```bash
less <nomefile> | sort
```

Il simbolo '|' è chiamato pipe (tubo) ed è spesso usato per collegare programmi Unix
tra loro. Il **12° carattere** della soluzione è il primo carattere dell'ultima parola nel file
elephant.txt ordinato alfabeticamente.

<div class="admonition hint">

Per memorizzare le righe ordinate in un nuovo file, puoi aggiungere un file di output,
come

```bash
less <nomefile> | sort > risultato.txt
```

</div>

### 4.3. Trovare parole in un file di testo

Per cercare parole specifiche in un file di testo, usa il comando

```bash
grep <parola> <nomefile>
```

Esso mostra tutte le righe dal file dato che contengono la parola data.
Il comando `grep` è molto potente e può gestire le espressioni regolari.

Per trovare **il carattere 13°**, cerca la parola **fire** nel file
`datascience.txt` e prendi il **primo** carattere dell'output.

<div class="admonition hint">

Puoi cercare attraverso molti file contemporaneamente includendo un \* nel
nomefile.

</div>

<div class="admonition warning">

Le ultime due esercitazioni potrebbero non funzionare su Git Bash.

</div>

----

## 5. Scompattare file

Vai alla directory `exercise_5`.

### 5.1. Decomprimere archivi

Decomprimere file compressi è un compito molto basilare ed importante. Su Unix,
spesso si incontrano archivi WinZip, archivi .tar e file compressi .gz. Per scompattare file zip di Win,
usa

```bash
unzip <nomefile>
```

per file .tar e .tar.gz

```bash
tar -xf <nomefile>
```

e per file .gz,

```bash
gunzip <nomefile>
```

Il **14° e 15° carattere** della soluzione sono in un archivio multiplo
avvolto nella directory `exercise_5`.

<div class="admonition hint">

Per imballare una directory e tutto ciò che contiene, puoi usare il comando

```bash
tar -cf backup.tar <directory>
```

Per comprimerlo successivamente, usa

```bash
gzip backup.tar
```

</div>

----

## 6. Strumenti da riga di comando

Vai alla directory `exercise_6`.

### 6.1. Modifica dei diritti di accesso ai file

Ogni file su Unix ha permessi separati per la lettura 'r', scrittura 'w',
ed esecuzione 'x'. Visualizzarli con:

```bash
ls -l
```

C'è un tripletto di permessi per il proprietario del file, uno
tripletto per un gruppo di utenti e uno per tutti gli altri. Il comando `chmod`
permette di cambiare questi permessi, ad esempio

```bash
chmod a+x <nomefile>
```

concede a tutti gli utenti il permesso di eseguire un file, mentre `chmod u-w`
impedisce all'utente corrente (se stesso) di scrivere nel file (proteggendolo dall'eliminazione accidentale).

Per vedere **i caratteri 16 e 17** della soluzione, rendi il

 programma
`permissions.sh` eseguibile. Quindi eseguilo con:

```bash
./permissions.sh
```

<div class="admonition hint">

Puoi concedere i permessi per un'intera struttura di directory usando

```bash
chmod -R a+x <directory>
```

</div>

### 6.2. Quanto spazio su disco ho lasciato?

Per scoprire quanto spazio su disco ti resta, puoi usare il comando

```bash
df
```

`df` elenca tutte le partizioni del disco rigido, i CD-ROM, le pen drive e alcune
partizioni logiche che Unix utilizza. Tutti i numeri sono dati in kilobyte (1000
byte o un milionesimo di GB).

Per ottenere il **18° carattere**, controlla la versione del programma `df`.
Scoprilo con:

```bash
df --help
```

La soluzione è l'ultimo carattere del nome del primo autore.

### 6.3. Impostare una variabile d'ambiente

Per installare alcuni programmi, è necessario impostare le cosiddette variabili d'ambiente. Queste possono essere impostate usando il comando

```bash
export <nome-variabile>=<valore>
```

Puoi vedere tutte le variabili con il comando

```bash
env
```

Per ottenere il **19° carattere**, devi usare `export` per impostare la
variabile *GIVEME* al valore **SOLUTION**.

```bash
echo $GIVEME
```

Scopri la **posizione del carattere nell'alfabeto** con:

```bash
echo $GIVEME | wc -c
```

<div class="admonition hint">

Per impostare variabili d'ambiente solo per la finestra della console attuale, scrivi
il comando di esportazione nel file `.bashrc` nella tua directory home (è un
file nascosto).

</div>

### 6.4. Controllare se hai una connessione internet

Il modo più semplice per verificare dalla riga di comando di Unix se la connessione
a Internet funziona, è inviare una richiesta a un server conosciuto (ad es.
www.spiced-academy.com) usando il comando

```bash
ping <indirizzo-web>
```

Il comando riporta quanto tempo impiega un messaggio per andare e tornare dal
server dato. Per interrompere i messaggi, premi Ctrl+C. Puoi usare il
programma

```bash
./check_ping
```

Il **20° carattere** è l'opzione `ping` che imposta il numero massimo
di richieste inviate. Verifica la documentazione con:

```bash
man ping
```

### 6.5. Gestione dei processi

Per vedere quali programmi sono in esecuzione sulla tua macchina, digita

```bash
top
```

Mostra un elenco di tutti i programmi attualmente attivi. *Shift+P* li ordina per
il tempo della CPU che stanno utilizzando, *Shift+M* per la quantità di memoria
che stanno utilizzando (se non vedi nessun programma che consuma molta memoria,
avvia un browser web). Esci da `top` premendo *q*.

Gli **ultimi due caratteri** della soluzione sono i primi due caratteri
della seconda parola nella riga che contiene le etichette delle colonne.

<div class="admonition hint">

Se vuoi eliminare uno dei programmi che hai avviato (ad es. perché
si è bloccato), puoi farlo digitando

```bash
kill -s 9 <pid>
```

</div>

Trovi il numero pid nella prima colonna dell'output di *top*. Naturalmente,
puoi interrompere solo i tuoi programmi, non quelli di
*root*, l'amministratore di sistema.

----

### Licenza

**© 2010 Dr. Kristian Rother**

Questo tutorial è pubblicato sotto la Licenza Creative Commons Attribution
Condividi allo stesso modo 4.0

Puoi trovare tutte le fonti su
[<https://github.com/krother/bash_tutorial>](https://github.com/krother/bash_tutorial).

### Ringraziamenti

Ringrazio Janusz M. Bujnicki, Allegra Via, Pedro Fernandes e Joachim
Jacob per il loro aiuto con il testing e la revisione del materiale. Altri
ringraziamenti vanno al Servizio Tedesco di Scambio Accademico (DAAD) per il supporto finanziario.

### Contatti

Dr. Kristian Rother

[krother@academis.eu](krother@academis.eu)

[www.academis.eu](www.academis.eu)