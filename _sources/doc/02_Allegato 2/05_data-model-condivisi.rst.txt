Data model condivisi
====================

In quanto segue sono riportati dei data model condivisi nelle differenti 
definizioni delle entità gestite dall’Infrastruttura Interoperabilità 
PDND riportate in precedenza.

INTERFACCIA
-----------
Rappresenta un attributo che deve essere associato ad un Erogatore ad 
un descrittore e-service, nella seguente tabella sono riportati i dati 
minimi dell’entità INTERFACCIA.

.. list-table::
    :header-rows: 1

    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id interfaccia
      -    identificativo univoco dell’interfaccia
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    idl
      -    specifica dell’interfaccia, dipendente dalla tecnologia, nello specifico per OpenAPI per REST e WSDL per SOAP
      -    text
      -    [1..1]
      -    SI
      -    SI
    * -    slo
      -    collezione degli SLO dell’interfaccia
      -    SLO
      -    [0..n]
      -    NO
      -    SI
    * -    pattern/profili
      -    collezione dei pattern/profili del MoDI utilizzati dall’interfaccia
      -    PATTERN/PROFILI
      -    [1..n]
      -    SI
      -    NO
    * -    documentazione
      -    documentazione accessoria e manualistica per l’utilizzo dell’interfaccia
      -    uri
      -    [0..n]
      -    NO
      -    SI
    * -    contatti tecnici
      -    contatti dell’Erogatore utili ai Fruitori per ricevere dettagli tecnici sull’interfaccia
      -    CONTATTO
      -    [0..n]
      -    NO
      -    SI
    * -    data registrazione
      -    data dell’ultima modifica dei dati dell’interfaccia
      -    date
      -    [1..1]
      -    SI
      -    SI
    * -    data completato
      -    data del completamento dell’interfaccia
      -    date
      -    [0..1]
      -    NO
      -    NO, l’attributo può essere valorizzato una sola volta all’esecuzione della transazione di stato COMPLETA
    * -    data archiviazione
      -    data dell’archiviazione dell’eservice
      -    date
      -    [0..1]
      -    NO
      -    NO, l’attributo può essere valorizzato una sola volta all’esecuzione dell'archiviazione

ATTRIBUTO
---------
Rappresenta un attributo che deve essere associato ad un potenziale Fruitore 
di un e-service, nella seguente tabella sono riportati i dati minimi 
dell’entità ATTRIBUTO.

.. list-table::
    :header-rows: 1

    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id attributo
      -    identificativo  univoco dell'attributo
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    tipo
      -    tipo attributo
      -    (‘certificato’, ‘dichiarato’, ‘verificato’)
      -    [1..1]
      -    SI
      -    NO
    * -    verifica obbligatoria
      -    indica se l’erogatore si riserva di effettuare la verifica dell’attributo
      -    boolean
      -    [1..1]
      -    SI
      -    NO
    * -    periodo validità verifica
      -    indica il numero di giorni per cui la verifica realizzata ha effetto
      -    number
      -    [0..1]
      -    NO
      -    NO
    * -    ultima verifica
      -    indica la data in cui è stata effettuata l’ultima verifica
      -    date
      -    [0..1]
      -    NO
      -    SI

“id attributo” DEVE essere popolato con i valori presenti nel registro 
degli Attributi degli Aderenti gestito dall’Infrastruttura interoperabilità 
PDND.

Il registro degli Attributi degli Aderenti gestito dall’Infrastruttura 
interoperabilità PDND registra per ogni attributo:

- l’identificativo univoco dell'attributo;

- la descrizione dell'attributo comprensiva delle condizioni per determinare 
  l’associazione da un Aderente;

- la tipologia (“certificato”, “dichiarato”, “verificato”) dell'attributo;

- la fonte collegata all’attributo la cui indicazione è obbligatoria per 
  attributi della tipologia “certificato”;

- l’eventuale riferimento specifico della fonte collegata.

CONTATTO
--------

Rappresenta un contatto reso dagli Erogatori, nella seguente tabella 
sono riportati i dati minimi dell’entità CONTATTO.

.. list-table::
    :header-rows: 1
	
    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id contact
      -    identificativo univoco di un contatto
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    nome
      -    nome della persona fisica 
      -    text
      -    [1..1]
      -    SI
      -    NO
    * -    cognome
      -    cognome della persona fisica
      -    text
      -    [1..1]
      -    SI
      -    NO
    * -    telefono
      -    telefono della persona fisica
      -    text
      -    [1..1]
      -    SI
      -    SI
    * -    email
      -    email della persona fisica
      -    text
      -    [1..1]
      -    SI
      -    SI

PATTERN/PROFILI
---------------
Rappresenta un pattern o un profilo definito dal MoDI, nella seguente 
tabella sono riportati i dati minimi dell’entità PATTERN/PROFILI.

.. list-table::
    :header-rows: 1
	
    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id pattern profilo
      -    identificativo univoco di un pattern o profilo
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    tipo
      -    tipologia di pattern o profilo
      -    (‘pattern interazione’, ‘pattern sicurezza’, ‘profilo’)
      -    [1..1]
      -    SI
      -    NO
    * -    name
      -    nome del pattern o profilo
      -    text
      -    [1..1]
      -    SI
      -    NO
    * -    descrizione
      -    descrizione del pattern o profilo
      -    text
      -    [1..1]
      -    SI
      -    NO

“id pattern profilo” DEVE essere popolato con il riferimento al pattern 
o profilo definito nel MoDI.

SLI
---

Riporta uno service level indicator, nella seguente tabella è riportato 
sono riportati i dati minimi dell’entità SLI.


.. list-table::
    :header-rows: 1
	
    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id sli
      -    identificativo univoco di uno slo
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    descrizione
      -    descrizione dello sli
      -    text
      -    [1..1]
      -    SI
      -    NO

SLO
---

Riporta uno service level objectives, nella seguente tabella sono riportati 
i dati minimi dell’entità SLO.

.. list-table::
    :header-rows: 1
	
    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id slo
      -    identificativo univoco di uno slo
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    id sli
      -    riferimento allo sli 
      -    SLI
      -    [1..1]
      -    SI
      -    NO
    * -    descrizione
      -    descrizione dello slo
      -    text
      -    [1..1]
      -    SI
      -    NO
    * -    funzione 
      -    funzione di calcolo dello slo
      -    text
      -    [1..1]
      -    SI
      -    NO

SLA
---

Riporta uno service level objectives, nella seguente tabella sono riportati 
i dati minimi dell’entità SLA.

.. list-table::
    :header-rows: 1
	
    * -    nome
      -    descrizione
      -    tipo
      -    cardinalità
      -    obbligatorio
      -    modificabile
    * -    id sla
      -    identificativo univoco di uno slo
      -    uri
      -    [1..1]
      -    SI
      -    NO
    * -    id slo
      -    riferimento allo sli 
      -    SLI
      -    [1..1]
      -    SI
      -    NO
    * -    descrizione
      -    descrizione dello sla
      -    text
      -    [1..1]
      -    SI
      -    NO
    * -    funzione 
      -    funzione di calcolo dello sla
      -    text
      -    [1..1]
      -    SI
      -    NO

.. forum_italia::
   :topic_id: 26431
   :scope: document
