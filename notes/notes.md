# Sistemi operativi
## Informazioni sul corso
### Programma del corso
#### Teoria
- Introduzione ai sistemi operativi
- Concetto di processo e multiprogrammazione
- Interazione tra processi; problema delle sezioni critiche
- Programmazione concorrente in ambiente globale
- Programmazione concorrente in ambiente locale
- Problemi di gestione risorse, deadlock
- Scheduling della CPU
- Trend dei sistemi operativi attuali
  
#### Laboratorio
- Introduzione a UNIX
- Interazione con l'utente: file system, shell e comandi
- Programmazione di sistemi UNIX
  - Primitive per la giestione di I/O e processi
  - Primitive per la sincronizzazione e comunicazione in UNIX nel modello a scambio di messaggi (segnali, pipe, FIFO, socket)
### Link utili
- [Pagina del corso](https://corsi.unipr.it/it/ugov/degreecourse/216746)

- [Pagina Elly](https://elly2023.dia.unipr.it/course/view.php?id=313)

### Bibliografia


## Cos'è un Sistema Operativo? 

## Aspetti fondamentali dei SO
Un sisema di elaborazione può essere visto come un insieme di:
- Hardware
- Sistema Operativo
- Programmi applicativi
- Utenti

Le applicazioni finali non possono gestire l'hardware del calcolatore, compito che spetta al sistema operatvio

I programmi per essere eseguiti hanno bisogno di risorse, queste ultime vengono gestite dal sistema operativo

- **Driver:** software che gestisce la comunicazione macchina-periferiche
- **Interfaccia:** costuituite dalle system call, denominate anche API, lo scopo essenziale è di fornire le giuste risorse agli applicativi degli utenti

### Cosa fanno i sistemi operativi?
La risposta sta nell'esigenza dell'utilizzatore finale e dalla macchina su cui questo viene seguito
- I sistemi embedded non hanno una interfaccia utente di sistema ma sono applicatica

## Definizione 1
Un sistema operativo è un intermediario tra utente e computer
- **Esecuzione di programmi:** Assicura l'esecuzione di programmi
- **Facilitù d'uso:** Rende il sistema informatico comodo da utilizzare
- **Efficienza:** Assicura un uso efficiente dell'hardware
- Le risorse devono essere eseguite in un determinato ordine
- Le risorse possono essere utilizzate da più utenti
- **Sicurezza:** controllo d'accesso con autenticazione degli utenti
- **Disaster Recovery:** Recupero dell informazioni in caso di disastro
- **Gestione semplice:** Delle risorse

Il sistema poperativo è un allocatore di risorse
- L'allocazione deve essere efficiente e eque
- Decide tra richieste in conflitto per un uso efficiente ed equo delle risorse, senza lasciare indietro nulla. Starvetion

Il sistema operativo controla le risorse
- Gestisce le anomalie e controlla le esecuzioni per prevenire errori e uso improprio

## Non c'è una definizione universalmente accettata
– Con il termine sistema operativo si intende quell'insieme di programmi
che provvedono alla gestione delle risorse Hw e Sw di un sistema di
calcolo.
– "Tutto ciò che viene fornito quando si ordina un Sistema Operativo"
- Una definizione alternativa (Tanenbaum, ricercatore):
un sistema operativo è un programma che controlla le risorse
di un calcolatore e fornisce ai suoi utenti un'interfaccia o
macchina virtuale più agevole da utilizzare della macchina
"nuda".
- L'unico programma che è sempre in esecuzione sul computer è il
kernel (nucleo) del SO.
Il resto è:
– un programma di sistema (fornito con il SO di cui costituisce una parte), 
– un programma applicativo

## Propriotà fondamentali 
- **Efficienza:** uso efficiente delle risorse
- **Affidabilità:** 
  - Sistema disponibile e pronto all'uso.
  - Gestione affidabile dei dischi di memoria.
- **Robustezza:** rispetto agli attacchi informatici

## Diversi tipi di controllori
Il lavoro del controllore centrale, CPU, nei sistemi più recenti, viene smaltito tra altri controllori.
- CPU
- Disk controller
- USB controller
- Adattatore grafico

- Processori(registri, unità aritmetiche (ALU), parallelismo interno)
- memorie (gerarchia di memoria)
- canali di comunicazione, bus che usano standard Universal Serial Bus (USB): comunica con dispositivi diversi
- Dispositivi di I/O e controllori dei dispositivi

## Funzionamento di una elaboratore
Il controllore ha la possibilità di interromere il processo di una CPU causando un **interrupt**, tramite una linea elettrica dedicata tra controllore e CPU. 
Gli interrupt handler è una tabella in memoria in cui sono presenti le informazioni su
viene salvato lo stato attuale e viene dato il controllo ad una routine di interruzione SPECIFICA per la sorgente di interruzione 
Le interruzioni TRAP sono generate dai programmi attraverso istruzioni speciali 
- Esterne; Asincrone
- Interne: Sincrone

- **Interrupt:** interruzione Hardware, causata da un dispositivo
- **Trap:** Interruzione Software, gestita allo stesso modo di quelle asincrone

## Sequenza temporale 
Il sistema operativo, nel momento di interruzione, salva le informazioni e i processi in corso al momento delle interruzioni. 

La memoria è fatta da diversi registri, come il program counter, tiene conto 
Ciclo di base della CPU si chiama Fetch and Exectute

## Gestione delle interruzione
- **Polling:** non si conosce la sorgente dell'interruzione, il SO deve verificare la sorgente
- **Interrupt vettorializzato:** ogni interrupt manda l'indice nel vettore della routine di interruzione da applicare relativa alla corrispondente routine di interruzione

Quando si avvia un processo I/O, viene mandata una richeista al sistema operativo, una system call, bisogna attendere che i dati vengano resi disponibili 

## Memoria
### Memoria principale
È la memoria ad acceso casuale dinamica (DRAM)
- Casuale perché non vi si accede in maniera procedurale
- Volatile perché il contenuto non persiste dopo l'aver rimosso l'alimentazione
### Memoria secondaria
Memoria non volatile che fornisce una amipia capacità di memorizzazione
- Dischi rigidi: piatti rigidi in metallo o vero ricoperti di materiale di registazione magnetico
  - Il controllore mappa le informazioni sui settori logici del disco
- Dischi a stato solido (SSD)/Non-volatile memory (NVM)

La memoria viene gestita in maniera gerarchica, con costi, dimensioni e veolcità diverse

### Caching
Processo in cui si tengono memorizzate in un sistema di archiviazione più veloce, parte di informazioni per un accesso più rapidp

### Sistemi Cluster


### Funzionamento del Sistema Operativo
Un SO è un software caricato all'avvio del calcolatore
Sequenza d'avvio:
- Controllo
- Bootstrap (incluso nel UEFI)
- Kernel
- Processi di sistema (Daeomn) 

**Nota:** Daemon vuol dire "in background". Sono programmi che non interagiscono con l'utente.

## Kernel
Serie di servizi, guidati (driven) dagli interrupt hardware e software. 
- Errore

## Multiprogrammazione e multitasking
I sistemi operativi moderni fanno uso moderno dell'hardware e dell'input output
i vecchi sistemi operativi potevano eseguire solo un programma alla volta: erano detti monoprogrammati, non sfrutta in maniera efficiente le risorse del sistema.
- Il tempo speso per l'input output viene impiegato dalla CPU per eseguire altri processi.
- La muktiprogrammazione di job (programmi non interattivi) viene gestita portando in memoria i dati dei vari job e ottimizzando i tempi di attesa svolgendo altri compiti. 
- Scheduling dei job, sceglie quali programmi eseguire nel caso in cui tutti i processi fossero già in esecuzione. 
- Operazione bloccante

Una evoluzione di questo concetto è il timesharing (multitasking).
- È previsto un tempo massimo di eseguzione per un processo, superato quel tempo il processo viene sospeso time slicing
- Round robin (algoritmo)
- Scheduler di mediotermine

Un sistema operativo multiprogrammato sfrutta la memoria per memorizzare codice dati dei diversi job

## Funzionamento in doppia modalità 
- Modalità kernel (privilegiata): tutte le istruzioni definite per la CPU possono essere eseguite
- Modalità utente (non privilegiata): 

**Bit di modalità:** registri, piccole memorie il cui accesso è molto rapido, tra questi c'è il processor state mode, questo contien il bit di modalità, 0 per modealità utente, 1 per modalità kernel 

Una system call (modelità utente) fanno in modo che il servizio utente possa essere eseguito in modalità supervisor

RTI (return from interrupt), RTE (return from exeption)

Nel 1980 i primi processori non avevano la doppia modalità, si poteva infatti modificare tutto


## Processo informatico 
Attività svolta dalla CPU per l'esecuzione di un programma
- **Programma:** Entità passiva costituita da un file presente nel file system, caratterizzato da una struttura specifica contentente il codice macchina per poter essere eseguito.
- **Processo:** Entità attiva, segue una determinata struttura dati, privilegi (accesso privilegiato, I/O) e risorse (memoria, CPU) per poter essere eseguito.
  - Un processo ha un suo ciclo di vita, in Linux viene chiamata una funzione exit per poterlo terminare, oppure la sua esecuzione viene forzata