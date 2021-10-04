Ciclo di vita degli e-service
=============================

Nel MoDI si individuano gli e-service come i servizi digitali realizzati 
da un Erogatore, attraverso l’implementazione delle necessarie API conformi 
alle [LG INTEROPERABILITÀ TECNICA] e alle [LG SICUREZZA], per assicurare 
l’accesso ai propri dati e/o l’integrazione dei propri processi ai Fruitori.

Di seguito sono individuate le funzionalità che l’Infrastruttura interoperabilità 
PDND DEVE rendere disponibili agli Aderenti per la gestione del ciclo di 
vita degli e-service.

Gestione dei descrittori degli e-service
----------------------------------------

Per descrittori degli e-service si intende l’insieme di dati registrati 
per un determinato e-service e il cui insieme  fornisce le informazioni 
sulle caratteristiche e il funzionamento del e-service stesso.

I descrittori degli e-service sono definiti dagli Erogatori attraverso 
la descrizione della natura dei propri e-service.

Gli e-service di un Erogatore sono resi disponibili ai Fruitori attraverso 
la pubblicazione sul Catalogo API dello specifico descrittore di e-service.

Un Erogatore DEVE definire per ogni e-service una delle tecnologie previste 
nel MoDI (quali REST, SOAP, ...).

Un Erogatore PUÒ deprecare la pubblicazione di un descrittore di e-service 
per esprimere la volontà di non accettare nuovi Fruitori per il relativo 
e-service.

Un Erogatore PUÒ pubblicare una nuova versione di un descrittore di e-service 
previa deprecazione della versione precedente. La nuova versione di un 
descrittore di e-service DEVE assicurare l’invarianza dei requisiti di 
fruizione e del modello di interoperabilità applicato per essa. Alla 
pubblicazione di una nuova versione di un descrittore di e-service, 
l’Infrastruttura interoperabilità PDND DEVE comunicare tale circostanza 
ai Fruitori che hanno stipulato un Accordo di interoperabilità per l’e-service. 

Un Erogatore NON PUÒ avere più di un descrittore di e-service in stato 
“attivo” per un dato e-service.

Gli Erogatori DEVONO prevedere un campo per l’inoltro, da parte dei Fruitori, 
del riferimento ai documenti informatici che possano provare la liceità 
dello specifico trattamento dei dati personali (ci si riferisce ad esempio 
al consendo dell’interessato nei casi di applicazione dell’articolo 6 
paragrafo 1 lettera del GDPR).

Nel caso in cui l’Erogatore preveda soggetti privati tra i Fruitori di 
un proprio e-service, lo stesso Erogatore DEVE definire per l’e-service 
una API che i Fruitori privati DEVONO implementare per assicurare il 
recupero dei documenti che attestano la liceità  dello specifico trattamento 
dei dati personali.

L’Infrastruttura interoperabilità PDND DEVE archiviare una versione di 
un descrittore di e-service deprecata dall’Erogatore nel caso in cui non 
siano stati sottoscritti Accordi di Interoperabilità per quello specifico 
descrittore di e-service.

Ciclo di vita
^^^^^^^^^^^^^

Un descrittore di un e-service è legato allo stesso e-service durante 
tutto il suo ciclo di vita.

Gli stati di un descrittore di e-service sono:

- “bozza”, l’Erogatore provvede a popolare gli attributi del descrittore 
  di e-service;

- “attivo”, l’Erogatore rende disponibile l’e-service agli Aderenti per 
  la stipula di Accordi di Interoperabilità;

- “deprecato”, l’Erogatore esprime la volontà di non accettare nuovi Fruitori 
  ma ne  assicura la disponibilità per i Fruitori che hanno già stipulato 
  un Accordo di Interoperabilità ;

- “archiviato”, le informazioni del descrittore di e-service sono conservate 
  dall’Infrastruttura interoperabilità PDND nel caso in cui non siano stati 
  sottoscritti Accordi di Interoperabilità relativi allo specifico descrittore 
  di e-service.

Le azioni realizzate dall’Erogatore per variare lo stato di un descrittore 
di e-service sono:

- SALVA, da “bozza” a “bozza”: l’Erogatore popola i dati e i metadati del 
  descrittore di e-service indicati in 4.1.2. Data model e registra quanto 
  popolato per completarlo successivamente

- PUBBLICA, da “bozza” a “pubblicato”: l’Erogatore pubblica il descrittore 
  di e-service a condizione che i dati e i metadati obbligatori siano 
  stati popolati;

- AGGIORNA, da “pubblicato” a “pubblicato”: l’Erogatore aggiorna i dati 
  e i metadati modificabili del descrittore di e-service;

- DEPRECA, da “pubblicato” a “deprecato”: l’Erogatore rende non più 
  disponibile l’e-service per la stipula di Accordi di Interoperabilità;

- CANCELLA, da “bozza”: l’Erogatore cancella il descrittore di e-service 
  quando ancora in bozza.

L’Infrastruttura interoperabilità PDND provvede a cambiare lo stato di 
un descrittore di e-service da “attivo” a “deprecato” quando l’Erogatore 
pubblica una nuova versione dello stesso descrittore.

L’Infrastruttura interoperabilità PDND effettua controlli periodici sui 
descrittori di e-service e provvede a cambiare lo stato dello stesso in 
“archiviato” di un descrittore di e-service nel caso in cui lo stato 
risulti “deprecato” e non sono presenti Accordi di Interoperabilità per 
lo specifico e-service notificando all’Erogatore il passaggio di stato.

Il successivo diagramma di stato riporta gli stati di un descrittore di 
e-service e per essi le relative transizioni caratterizzate dall’azione 
realizzata dall’Erogatore e dai vincoli per la loro esecuzione, separati 
da “:”. Si precisa che in assenza di azioni indicate si assume che 
l’Infrastruttura interoperabilità PDND esegue in automatico la transizione 
al presentarsi della condizione abilitante la stessa.


.. mermaid::

   graph TD
   avvio((start))
   b[bozza]
   p[attivo]
   np[deprecato]
   e[archiviato]
   fine((end))
   avvio --> b
   b --> |CANCELLA| fine
   b --> |PUBBLICA: tutti i campi obbligatori sono valorizzati | p    
   b --> |SALVA| b
   p --> |AGGIORNA| p
   p --> |DEPRECA| np   
   np --> |: nessun accordo di interoperabilità presente| e
   e --> fine

L’Infrastruttura interoperabilità PDND DEVE assicurare la possibilità 
agli Erogatori di utilizzare i dati e metadati di un descrittore di e-service 
registrati per definire e pubblicare una nuova versione dello stesso descrittore 
di e-service o un nuovo e-service.

L’Infrastruttura interoperabilità PDND DEVE assicurare le funzionalità 
agli Utenti degli Aderenti, tramite interfacce web, per la gestione dei 
descrittori di e-service che assicurano quanto descritto in precedenza.

L’Infrastruttura interoperabilità PDND DEVE assicurare le funzionalità 
agli Aderenti, tramite API REST, per la gestione dei descrittori di e-service 
che assicurano quanto descritto in precedenza.

Data model
^^^^^^^^^^

Nella seguente tabella sono riportati i dati minimi del descrittori di e-service.

.. list-table::
    :header-rows: 1

    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id eservice
      -    identificativo univoco dell’eservice
      -    uri
      -    [1..1]
      -    SI
      -    NO 
    * -    nome
      -    nome dell’e-service
      -    text
      -    [1..1]
      -    SI
      -    NO
    * -    descrizione
      -    descrizione dell’e-service
      -    text
      -    [0..1]
      -    NO
      -    SI
    * -    versione
      -    versione dell’e-service
      -    number
      -    [1..1]
      -    SI
      -    NO
    * -    versione
      -    versione dell’e-service
      -    number
      -    [1..1]
      -    SI
      -    NO
    * -    contatti amministrativi
      -    contatti dell’Erogatore utili ai potenziali Fruitori per avviare le interazione in merito all’e-service
      -    CONTATTO
      -    [1..n]
      -    SI
      -    SI
    * -    tecnologia
      -    tecnologia dell’interfaccia 
      -    (‘REST’,’SOAP’)
      -    [1..1]
      -    SI
      -    NO
    * -    id erogatore
      -    identificativo univoco dell’erogatore
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    id capofila
      -    identificativo univoco del capofila
      -    uri
      -    [0..1]
      -    NO
      -    NO
    * -    requisiti di fruizione
      -    requisiti di fruizione per l’accesso all’e-service
      -    ATTRIBUTO
      -    [0..1]
      -    SI
      -    NO
    * -    modello accordo di interoperabilità
      -    modello di accordo di interoperabilità utilizzato per l’e-service
      -    uri
      -    [0..1]
      -    NO
      -    NO
    * -    interfaccia
      -    interfaccia  che descrive la modalità di accesso al servizio
      -    INTERFACCIA
      -    [1...1]
      -    SI
      -    NO
    * -    interfaccia retrive
      -    interfaccia che descrive la modalità di accesso al servizio che il Fruitore privato deve implementare per assicura all’Erogatore la possibilità di recuperari i documenti che attestano la legittimità dello specifico trattamento dei dati personali
      -    INTERFACCIA
      -    [0...1]
      -    NO
      -    NO
    * -    data registrazione
      -    data dell’ultima modifica dei dati dell’eservice
      -    date
      -    [1..1]
      -    SI
      -    SI
    * -    data pubblicazione
      -    data della pubblicazione dell’eservice
      -    date
      -    [0..1]
      -    NO
      -    NO, l’attributo è valorizzato una sola volta all’esecuzione della transazione di stato PUBBLICA dall’Infrastruttura Interoperabilità PDND
    * -    data revoca
      -    data della revoca dell’eservice
      -    date
      -    [0..1]
      -    NO
      -    NO, l’attributo è valorizzato una sola volta all’esecuzione della transazione di stato REVOCA dall’Infrastruttura Interoperabilità PDND
    * -    data archiviazione
      -    data dell’archiviazione dell’eservice
      -    date
      -    [0..1]
      -    NO
      -    NO, l’attributo è valorizzato una sola volta all’esecuzione dell'archiviazione dall’Infrastruttura Interoperabilità PDND

I metadati minimi associati ai descrittori di e-service dagli Erogatori 
rispettano le indicazioni fornite dal Gestore nella documentazione tecnica 
da esso definita per attuare quanto disposto nel presente Allegato.

L’Infrastruttura interoperabilità PDND gestisce i dati di servizio necessari 
ad assicurare l’implementazione delle funzionalità per la gestione dei 
descrittori di e-service coerentemente quanto descritto in precedenza.
