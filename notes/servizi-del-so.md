# Servizi di un sistema operativo
Un sistema operativo offre un ambiente in cui eseguire programmi e fornire servizi.
I servizi possono essere calssificati per categorie in base alle funzionalità offerte: 
- **Interfaccia utente:**
- **Esecuzione di un programma:** il sistema deve caricare un programma dalla memoria di massa in memoria principale ed eseguirlo. Il programma deve terminare la propria esecuzione in modo normale o anomalo, indicandone eventualmente l'errore
- **Operazioni di I/O:** 
- **Gestione del file system:**
- **Comunicazioni:**
- **Rilevamento degli errori:** errore SIGSEGV signal segment violation, strace, trus

Operazioni che assicurano il funzionamento efficiente del sistema operativo.
- **Allocazione delle risorse:**
- **Logging:**
- **Accounting delle risorse:**
- **Protezione e sicurezza:**

## Interfaccia con l'utente del sistema operativo
L'utente può comunicare con il sistema operativo in 2 modi principali:
1. Command Line Interface (CLI): man builtins
2. Graphic User Interface (GUI): 

## Chiamate di sistema o (API)
Interfaccia per i servizi resi disponibili dal sistema operativo. tali chiamate sono generalmente disponibili sottoforma di routine scritte in C o C++. 
La funzione libreria è un wrapper che avvolge la chiamata dell'interrupt software. Il programma chiama la funzione di libreria con un determinato standard (non chiamano direttamente l'interrupt software).
- Win32 per Windows.
- POSIX IEEE/ISO per un generico sistema UNIX
- Java API per JVM

Esempio di chiamata di sistema: copia di un file da una directory sorgente ad una di destinazione
1. Ottenere nome del file sorgente
2. Ottenere il percorso di destinazione
3. Aprire il file di input (se non esiste o non ci sono i diritti, abort)
4. Creare il file di output (se la directory specificata non esiste già)

Per ottenere tutte le informazioni sulle API è necessario invocare il comando , si consideri la generaca funzione read() man 2 read
Quando una syscall manda -1 vuol dire che restituisce un errore 

In linux tutte le system call stanno in libc
Un sistema operativo di tipo unix, 

Come passare parametri alla system call. In c viene fatto il push dei parametri sullo stack o direttamente nei registri della CPU (linux, macOS)
- Parametri memorizzati in un blocco o tabella di memoria. 
- Parametri messi o spinti sulllo stack dal programma

vDSO (virtualDynamic Shared Object)