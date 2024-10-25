# Calcio01
Realizzare il database sulla gestione delle squadre di calcio.
Bisogna compilare uno stesso foglio di calcolo presente al seguente link

[foglio di calcolo del DB](https://docs.google.com/spreadsheets/d/1ufGat5lYOovOEFbwfDz0B6VMo46w1tJ137aRGzN29io/edit?usp=sharing)

Il foglio di calcolo è diviso in **5** fogli di lavoro in cui i primi 4 contengono già dei dati di esempio. Tuttavia, **controllare la correttezza dei dati ed aggiungerne degli altri**.

I fogli di lavoro contenuti nel foglio di calcolo sono

**Squadre, Giocatori, Squadre_giocatori, Procuratori, Gruppi_Studenti** 

Per la realizzazione del foglio di calcolo gli studenti si divideranno in **6 gruppi**. Scrivere i gruppi (funzione e componenti) nel foglio di lavoro **Gruppi_Studenti**.

Compiti dei gruppi:
* 4 gruppi (gruppo da 1 a 4) si occuperanno di compilare rispettivamente i fogli di lavoro Squadre, Giocatori, Procuratori, Squadre_Giocatori.
* 1 gruppo (il gruppo 5) si occuperà di creare la struttura del DB in istruzioni SQL da scrivere in un file testo e poi in MySQL
* 1 gruppo (il gruppo 6) si occuperà di supervisionare il lavoro degli altri gruppi assicurandosi della correttezza e del coordinamento.

Tre gruppi inizieranno a lavorare compilando i fogli di lavoro Squadre, Giocatori, Procuratori. Per il momento lasciare il campo `Id_procuratore` della tabella `Giocatori` **vuoto**

Una volta completato i fogli di lavoro `Squadre` e `Giocatori` il quarto gruppo potrà procedere a compilare il foglio di lavoro `Squadre_giocatori`. Notare che un giocatore può militare in squadre diverse in anni diversi (o anche nello stesso anno ma si può anche non considerare questo caso).

Cose a cui prestare **attenzione** per il gruppo 5 destinato a creare la struttura del DB

* Usare la convenzione che i nomi di tabelle sono tutti minuscoli, mentre i nomi dei campi hanno iniziale maiscuole anche di parole collegate dall'underscore (`_`) esempio `Id_Procuratore`.
* Per la tabella `squadre`
    - I campi `abbonati` e `budget` sono interi
* Per la tabella `Giocatore`
    - Tutti i campi sono obbligatori (`NOT NULL`) tranne `stipendio` e `Id_Procuratore` (che quindi hanno default `NULL`)
    - Il campo `data_nascita` di un calciatore sarà nel database di tipo `Date` e quindi nel foglio di calcolo va indicato nella forma `aaaa-mm-gg`, esempio `1994-03-28` e non `28-03-1994`
    - Per il campo capitano indicare `1` se nella sua carriera il calciatore è stato un capitano e `0` se non lo è mai stato.
* Per la tabella `squadre_giocatori`
    - i campi `Id_squadra` e `Id_giocatore` sono chiavi esterne
    - Il campo `Anno` è un intero che rappresenta l'anno in cui il giocatore ha militato in quella squadra; nel caso ad esempio della stagione `2021-2022` indicare solo il secondo anno ovvero `2022`
    - Aggiungere dei vincoli di chiave esterna che se si cancella o aggiorna una squadra o un giocatore si aggiornano anche le corrispondenti righe della tabella `squadre_giocatori` 
* Per la tabella `procuratori` 
    - tutti i campi sono non nulli