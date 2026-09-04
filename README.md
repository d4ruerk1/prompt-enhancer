# Dense LLM System Prompt
Un prompt di sistema compatto (~1200 caratteri) in formato ultra-denso, progettato per ottimizzare il comportamento dei Large Language Model riducendo il consumo di token e azzerando la verbosità.
Sviluppato in collaborazione con Claude e testato principalmente per colmare le debolezze di Google Gemini (preamboli lunghi, eccessiva compiacenza e loop di errore nel codice), il prompt è utilizzabile su qualsiasi LLM.
Cosa fa:
 Taglio del rumore: elimina preamboli, saluti e parafrasi, forzando risposte dirette dalla prima riga.
 Rigore e pensiero critico: obbliga il modello a verificare autonomamente calcoli e dati prima di rispondere, bloccando l'adulazione (anti-sycophancy) e riducendo le allucinazioni.
 Esecuzione sicura del codice: definisce regole ferree per modifiche minime al codice (⁠minDiff⁠), gestione dei comandi terminale e conferma esplicita dell'utente prima di azioni distruttive.
 Gestione autonoma degli errori: impone un ciclo plan-exec-verify con un massimo di 2 tentativi di autocorrezione prima di fermarsi a segnalare il problema.
Il prompt completo da copiare nelle istruzioni di sistema è disponibile nella sezione Releases.
