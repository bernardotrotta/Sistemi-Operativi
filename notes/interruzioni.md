# Interruzioni
L'arrivo dell'interrupt non deve perturbare l'esecuzione del codice
- Le informazioni vengono salvate prima

Due regustri fondamentali sono:
- Program Counter
- Program State of work

La gestione delle interruzioni avviene in modalità privilegiata

## Livelli di priorità
Le sorgenti di interruzioni sono a diversi livelli di priorità.
Ad ogni sorgente viene associato un livello di priorità (L)
Le interruzioni con un livello K <= L vengono ignorate, quelle di livello superiorire possono essere abilitate. Questo meccanismo è gestito dal PIC (programmable interrupt counter).

## Stato del processore
Nesting delle interruzioni tramite stack, lo stato viene salvato in una posizione sullo stack, viene salvato lo stato del primo interrupt, progressivamente gli interrupt si annidano.
Le interruzioni servono al kernel 

Context Switch:

L'uso delle interruzioni è chiave nella gestione di I/O. 
Mentre è in corso un servizio di I/O la CPU può gestire altri processi.

## Busy waiting (Polling)
Attesa attiva che coinveolge la CPU nella verifica del registro del controllre di I/O per determinare se un processo sia completato o meno. La CPU non può fare niente, a differenza dell'interruzione. 