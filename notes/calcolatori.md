# Generalità sui calcolatori
Un calcolatore è composto da
- Una o più CPU
- Una serie di controllori di dispositivi connessi attraverso un canale di comunicazione condiiso (bus) che garantisce l'accesso alla memoria condivisa del sistema.
  - Ogni controllore si occupa di un determinato dispositivo
  
CPU e controllori operano in parallelo, contendendosi l'accesso in memoria, quest'ultimo supervisionato dal controllore di memoria. 


## Avvio di un sistema
<!--Il processo di avvio di un sistema di elaborazioni è il seguente: 
1. Avvio del firmware: insieme di istruzioni per il controllo dell'integrità hardware e avvio del sistema operativo tramite il *bootstrap* 
2. Avvio del *bootstrap*: software memorizzato in apposite memorie di sola lettura o in memorie programmabili e cancellabili elettronicamente (EEPROM). Il suo compito è caricare in memoria il sistema operativo partendo dal kernel -->

1. Avvio del firmware:

    - Il firmware è un insieme di istruzioni memorizzate in una memoria non volatile (come la ROM o la EEPROM) che viene eseguito all'accensione del sistema.
    - Il firmware esegue un' serie di test diagnostici per verificare l'integrità dell'hardware, come la memoria, la CPU e i dispositivi di archiviazione.
    - Se i test hanno esito positivo, il firmware carica il bootstrap in memoria.

2. Avvio del bootstrap:

    - Il bootstrap è un piccolo programma memorizzato nella stessa memoria del firmware o in una memoria separata.
    - Il compito del bootstrap è caricare il sistema operativo in memoria.
    - Il bootstrap carica il kernel del sistema operativo, che è la parte centrale del sistema operativo che gestisce le risorse del sistema e fornisce i servizi di base per l'esecuzione dei programmi.
    - Una volta caricato il kernel, il bootstrap cede il controllo al sistema operativo.
 
3. Avvio del sistema operativo:
   - Il kernel del sistema operativo inizializza i dispositivi hardware e carica i driver necessari per il loro funzionamento.
   - Il kernel carica quindi i file di sistema necessari per l'esecuzione dell'interfaccia utente e delle applicazioni.
   - Una volta completata l'inizializzazione, il sistema operativo è pronto per l'utilizzo.

4. Avvio dei daemon:

   - I daemon sono programmi che vengono eseguiti in background e che forniscono servizi al sistema operativo o ad altre applicazioni.
   - I daemon vengono avviati automaticamente durante il processo di avvio del sistema operativo o possono essere avviati manualmente in un secondo momento.
   - Esistono diversi tipi di daemon, tra cui:
     - Daemon di sistema: forniscono servizi essenziali per il funzionamento del sistema operativo, come la gestione della memoria, la gestione dei processi e la gestione della rete.
     - Daemon di utilità: forniscono servizi utili per gli utenti, come la gestione della posta elettronica, la stampa e la gestione dei file.
     - Daemon di applicazioni: forniscono servizi per specifiche applicazioni, come un server web o un databa

## Interrupt
Appunti sugli interrupt
Introduzione

Un interrupt è un segnale che interrompe temporaneamente l'esecuzione del programma principale per far fronte a un evento esterno o interno. L'evento può essere generato da un dispositivo hardware, come un timer o un sensore, o da un software, come un'eccezione.

Gestione degli interrupt

La gestione degli interrupt è un processo complesso che richiede la collaborazione di diversi componenti hardware e software. Ecco i passi principali:

Generazione dell'interrupt: Il dispositivo o il software che genera l'interrupt invia un segnale alla CPU.
Riconoscimento dell'interrupt: La CPU riceve il segnale e determina la sua priorità.
Salvataggio del contesto: La CPU salva lo stato del programma in esecuzione, in modo da poterlo ripristinare in seguito.
Esecuzione della routine di interrupt: La CPU carica e esegue la routine di interrupt associata all'evento.
Ripristino del contesto: La CPU ripristina lo stato del programma in esecuzione e riprende l'esecuzione dal punto in cui era stata interrotta.
Tipi di interrupt

Esistono due tipi principali di interrupt:

Interrupt hardware: generati da dispositivi hardware.
Interrupt software: generati da software.
Gli interrupt hardware possono essere further suddivisi in:

Interrupt esterni: generati da dispositivi esterni al sistema.
Interrupt interni: generati da dispositivi interni al sistema.
Priorità degli interrupt

Ogni interrupt ha una priorità che determina l'ordine in cui viene gestito dalla CPU. Gli interrupt con priorità più alta vengono gestiti prima di quelli con priorità più bassa.

Disattivazione degli interrupt

È possibile disattivare gli interrupt per evitare che interrompano l'esecuzione di un programma critico. Tuttavia, è importante riattivare gli interrupt al termine del programma critico, in modo da poter gestire gli eventi esterni.

Esempi di interrupt

Pressione di un tasto: un interrupt hardware generato dalla tastiera.
Scadenza di un timer: un interrupt hardware generato da un timer.
Errore di divisione: un interrupt software generato da un'eccezione di divisione per zero.