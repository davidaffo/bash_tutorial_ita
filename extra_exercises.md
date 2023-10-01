## Esercizi Aggiuntivi

### Fruit Pipes

1. Crea una nuova directory `frutta/`
2. Crea 7 file di testo vuoti come `mela`, `banana` ecc.
3. Salva tutti i nomi dei file in un file di testo
4. Elenca tutti i nomi dei file che contengono la lettera `a`
5. Salva i nomi con `a` in un file di testo
6. Usa `diff` per trovare tutti i nomi dei file che non contengono una `a`

### Il Baule Chiuso

1. Crea una nuova directory `stanza_segreta/`
2. Crea un file di testo vuoto `baule` al suo interno
3. Usa una pipe per inserire la parola *tesoro* nel file baule
4. Chiudi a chiave il baule: rimuovi il permesso di lettura/scrittura per tutti
5. Esci dalla stanza alla directory superiore
6. Nascondi la stanza rinominandola in `.stanza_segreta/`
7. Leggi il contenuto del baule

### Salve Bash Script

1. Scrivi uno script bash `ciao.sh` che stampa 'Salve, Mondo'
2. Esegui il programma con `source ciao.sh`

### Salve Ambiente

1. Salva il percorso+nomefile di `ciao.sh` nella variabile d'ambiente `SALUTO`
2. Esegui il programma con `source $SALUTO`

### Salve 10 Volte

1. Modifica `ciao.sh` per stampare un messaggio dato come argomento da riga di comando (accessibile tramite `$1`)
2. Testa lo script con `source ciao.sh 'Salve, Mondo'`
3. Scrivi un altro script bash che avvia `ciao.sh` 10 volte con messaggi diversi
4. Esegui tutto

### Salve, Arrivederci

1. Modifica `ciao.sh` per ripetere il messaggio ogni 10 secondi
2. Avvia lo script
3. Usa i comandi bash per terminare il processo
4. Avvia lo script 10 volte
5. Usa bash per terminare tutti e 10 i processi