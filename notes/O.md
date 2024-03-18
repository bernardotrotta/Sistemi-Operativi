# Struttura di I/O
- I registri sono gestiti dal compilatore.
- L'hardware gestisce il livello delle cache. 
- Il sistema operativo è responsabile per 3 livelli della gerarchia
  -  Memoria principale
  -  Memoria secondaria
-  
+

Un sistema operativo deve nascondere tutte le caratteristiche fisiche del sistema operativo astraendo senza dover conoscere la porta seriale. 


*Spooling:* utilizzare i dati raccolti in una periferica in contemporanea all'elaborazione
Esempio; la stampa non va alla periferica, viene salvata in un file dedicato per poter sincronizzare il trasfermiento con i tempo meccanici della stampante.


## Protezione e sicurezza
Un sistema programmato è spesso multiutente
- Accesso programmato per permettere agli utenti di accedere a determinate risorse
- Protezione: qualsiasi meccaniscmo di controllo dell'accesso dei processi o degli utenti alle risorse definite dal sistema operativo
- Sicurezza: difesa del sistema da a ttacchi interni ed esterni
  - Livello 1: Considerazione dell'identità dell'utente
    - ID Utenti: nei sistemi unix è un valore maggiore di 0 per utenti che non siano root
  Molti sistemi gestiscono in maniera temporanea un accesso occasionale a operazioni che richieddono un determinato livello di privilegio 

# Virtualizazione e emulazione
Consente ai sistemi operativi di eseguire applicazioni all'interno di altri sistemi operativi. 
- **Emula   zione:** utilizzata quando il tipo di CPU di origine è diverso da quello di destinazione (ad esempio da Intel x86/amd64 ad Arm)
  - Metodo generalmente più lento
  - Quando il linguaggio del computer non viene compilato in codice nativo - Interpretazione
- Virtualizzazione: Sistema operativo compilato in modo nativo per la CPU, che esegue sistemi operaivi guest anch'essi compilati in modo nativo
  - Si consideri VMware che esegue guest WIN10, ciascuno dei quali esegue applicazioni, il tutto su un sistema operativo host nativo WIN10
  - VMM (Virtual Machine Manager) fornisce servizi di virtualizzazione    

## Paradigma Client-Server
