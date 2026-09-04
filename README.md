# Dense LLM System Prompt
Un prompt di sistema compatto (~1200 caratteri) in formato compresso ad alta densità di token. È progettato per trasformare qualsiasi LLM in un assistente tecnico disciplinato, azzerando il rumore conversazionale e forzando l'autonomia logica.

Sviluppato in collaborazione con **Claude** e calibrato specificamente per correggere i tipici punti deboli di **Google Gemini** (prolissità, compiacenza verso errori dell'utente e cicli a vuoto nella programmazione), rimanendo pienamente compatibile con qualsiasi altro modello avanzato.

---

### Cosa fa concretamente:
* **Ciclo operativo autonomo (`AG`):** Impone la sequenza deterministica *raccogli info → pianifica → esegui → verifica*. In caso di errore blocca i loop infiniti: esegue al massimo 2 tentativi variando l'approccio, poi si ferma e riporta il blocco.
* **Disciplina nel codice e nel terminale (`EDIT/CODE`, `CMD`, `FILES`):** Obbliga a modifiche minime e mirate al codice esistente (`minDiff`), all'analisi preventiva dell'ambiente e all'invio di comandi terminale aggregati in un unico blocco eseguibile, proteggendo dati sensibili con placeholder.
* **Anti-Sycophancy e fact-checking (`RES`, `EVID`, `RSN`):** Impedisce al modello di dare ragione all'utente su premesse o calcoli errati. Dati temporali, quote, versioni o statistiche richiedono fonti reali e verifica autonoma; se mancano dati certi, ammette i limiti invece di inventare.
* **Priorità deterministica (`PRIO`):** Fissa una gerarchia vincolante: *Accuratezza > Fattibilità > Completezza > Formato > Sintesi > Token*. La correttezza tecnica vince sempre sulla brevità.
* **Sicurezza per azioni distruttive (`RISK/CPLX`):** Richiede sempre l'autorizzazione esplicita dell'utente prima di applicare piani ad alto impatto o eseguire modifiche irreversibili.
* **Zero rumore nell'output (`OUT`, `STY`):** Taglia saluti, formule di cortesia, parafrasi della domanda e conclusioni ovvie. La risposta parte direttamente con la logica e la soluzione utile fin dal primo carattere generato.
* **Rilevamento degrado contesto (`CTX`):** Se il contesto diventa troppo lungo o la coerenza scende, il modello si ferma e lo segnala attivamente anziché iniziare a degradare silenziosamente.

---

### Download e utilizzo

Il codice sorgente del prompt compresso è prelevabile direttamente nella sezione **[Releases]** e poi può essere messo in Gemini tramite la sezione “Contesto Personale”.
