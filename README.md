# ERmes

Editor minimale per disegnare schemi **Entità/Relazione** nel browser, con la notazione dei libri di testo italiani (attributi a pallino).

**Provalo online: https://rawjute.github.io/ermes/**

È un'unica pagina HTML: non richiede installazione, server o account. Puoi usarlo dal link qui sopra, oppure scaricare `index.html` e aprirlo con un browser moderno, anche senza connessione.

## Cosa si può modellare

- **Entità** e **associazioni**, con le cardinalità `(0,1)`, `(1,1)`, `(0,N)`, `(1,N)` sui collegamenti.
- **Attributi** semplici, opzionali e multivalore: sono sempre collegati a un'entità o a un'associazione.
- **Identificatori**:
  - semplici (pallino pieno);
  - composti, con la linea che interseca i collegamenti degli attributi e un piccolo "ponte" sui collegamenti che non ne fanno parte;
  - esterni, per le entità deboli: includono la partecipazione `(1,1)` a un'associazione.
- **Generalizzazioni** con linee ad angolo retto e copertura `(T,E)`, `(T,S)`, `(P,E)`, `(P,S)`. Le entità figlie ereditano l'identificatore del padre e non possono averne uno proprio.

Le entità che non hanno ancora un identificatore sono evidenziate in arancione, ma solo sul foglio: l'evidenziazione non compare nelle immagini esportate.

## Come si usa

- Trascina **Entità** o **Associazione** dalla barra a sinistra sul foglio, oppure cliccale per inserirle al centro.
- Seleziona un elemento e trascina uno dei pallini **+** su un altro elemento per collegarli. Se rilasci nel vuoto, scegli cosa creare.
- Con un'entità o un'associazione selezionata compaiono **Attributo** e **Identificatore**.
- Seleziona con Ctrl più attributi della stessa entità, ed eventualmente il collegamento all'associazione, poi premi **Identificatore** per formare un identificatore composto o esterno.
- Doppio clic su un elemento per rinominarlo; doppio clic sul foglio vuoto per creare un'entità.
- Nella scheda **Note** del pannello di destra (tasto `N`) puoi scrivere le ipotesi aggiuntive e le note sullo schema: si salvano insieme allo schema.

### Mouse e tastiera

| Comando | Azione |
| --- | --- |
| Trascina con il tasto sinistro sul vuoto | Seleziona più elementi |
| Tasto destro o rotella premuta | Sposta il foglio |
| Ctrl + rotella | Zoom |
| `E` / `S` / `A` / `I` | Entità / Associazione / Attributo / Identificatore |
| `C` / `G` | Collega / Generalizzazione |
| `Canc` | Elimina |
| `Ctrl+Z` / `Ctrl+Y` | Annulla / Ripeti |
| `Ctrl+D` | Duplica |
| `Ctrl+S` / `Ctrl+O` | Salva / Apri |
| `P` | Mostra o nasconde il pannello laterale |
| `N` | Apre le note e ipotesi |

## File

- **Salva** crea un file `.ermes`, cioè JSON, che si riapre con **Apri**.
- **PNG** e **SVG** esportano l'immagine dello schema su sfondo bianco.
- Il **PNG** contiene anche lo schema, in un blocco di testo `iTXt` con chiave `ermes` che i visualizzatori ignorano. Si può quindi riaprire con **Apri** come un file `.ermes`.
  Lo schema però si perde se l'immagine viene ricodificata: copia e incolla, app che comprimono le immagini (per esempio WhatsApp), ritagli o salvataggi da un programma di grafica. Per un archivio sicuro conviene tenere anche il file `.ermes`.
- Il lavoro in corso resta anche nel browser, tra una visita e l'altra.

Il tema chiaro è quello predefinito; quello scuro si attiva con il pulsante in alto a destra.
