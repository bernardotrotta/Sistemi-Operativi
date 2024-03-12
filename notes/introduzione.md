# Sistema operativo
## Introduzione
È un insieme di programmi (software) che gestisce gli elementi fisici di un calcolatore (hardware)


Le applicazioni finali non possono gestire l'hardware del calcolatore, compito che spetta al sistema operatvio

I programmi per essere eseguiti hanno bisogno di risorse, queste ultime vengono gestite dal sistema operativo

- **Driver:** software che gestisce la comunicazione macchina-periferiche
- **Interfaccia:** costuituite dalle system call, denominate anche API, lo scopo essenziale è di fornire le giuste risorse agli applicativi degli utenti

## Cosa fa un sistema operativo 
Un sistema operativo controlla l'hardware di un sistema di elaborazione e ne coordina l'utilizzo da parte dei programmi applicativi per gli utenti, l'uso specifico dipende dal tipo di elaboratore su cui è installato. In generale deve garantire:
- **Esecuzione di programmi:** assicura l'esecuzione di programmi
- **Facilitù d'uso:** uso semplice e intuitivo del sistema informatico
- **Efficienza:** uso efficiente delle risorse
- **Accessibilità:** Le risorse possono essere utilizzate da più utenti
- Le risorse devono essere eseguite in un determinato ordine
- **Sicurezza:** controllo d'accesso con autenticazione degli utenti
- **Disaster Recovery:** Recupero dell informazioni in caso di disastro

- I sistemi embedded non hanno una interfaccia utente di sistema ma sono applicatica
- **Programma di controllo:** gestisce l'esecuzione dei programmi utenti in modo da impedire che si verifichino errori o che il calcolatore sia usato in modo scorretto.

## Generalità sui calcolatori
Un calcolatore è composto da
- Una o più CPU
- Una serie di controllori di dispositivi connessi attraverso un canale di comunicazione condiiso (bus) che garantisce l'accesso alla memoria condivisa del sistema.
  - Ogni controllore si occupa di un determinato dispositivo