Definizioni
===========

Erogatore
---------

Un soggetto che rende disponibili e-service ad altri soggetti, per la 
fruizione di dati in suo possesso o l’integrazione di processi.

Fruitore
--------

Un soggetto che, tramite la sottoscrizione di un accordo di interoperabilità, 
utilizza gli e-service messi a disposizione da un Erogatore.

API
---

Un insieme di procedure/funzionalità/operazioni disponibili al programmatore, 
di solito raggruppate a formare un insieme di strumenti specifici per 
l’espletamento di un determinato compito. 

e-service
---------

I servizi digitali realizzati da un Erogatore, attraverso l’implementazione 
delle necessarie API conformi alle [LG INTEROPERABILITÀ TECNICA] e alle 
[LG SICUREZZA], per assicurare ai Fruitori l’accesso ai propri dati e/o 
l’integrazione di processi.

Pattern di interazione
----------------------

I Pattern di interazione, individuati nelle [LG INTEROPERABILITÀ TECNICA], 
che indicano le modalità tecniche per implementare i modelli di scambio 
telematico tra Erogatori e Fruitori tramite API.

Pattern di sicurezza
--------------------

I Pattern di sicurezza, individuati nelle [LG INTEROPERABILITÀ TECNICA] 
nel rispetto delle [LG SICUREZZA], che delineano le modalità tecniche 
per assicurare che i Pattern di interazione rispettino specifiche esigenze 
di sicurezza (autenticazione e autorizzazione delle parti, confidenzialità 
delle comunicazioni, integrità dei messaggi scambiati, ecc...).

Profili di interoperabilità
---------------------------

I Profili di interoperabilità, individuati nelle [LG INTEROPERABILITÀ TECNICA], 
sono combinazioni di Pattern di interazione e Pattern di sicurezza per 
risolvere esigenze di interazione specifiche tra Erogatori e Fruitori 
tramite API.

Aderenti
--------

I soggetti interessati in qualità di Erogatori e/o Fruitori che si sono 
accreditati sulla Infrastruttura interoperabilità PDND attraverso il 
Processo di accreditamento per usufruire delle funzionalità messe a disposizione 
dalla stessa infrastruttura e dare seguito alla erogazione e/o fruizione 
degli e-service.

Lettera di Adesione
-------------------

Il documento sottoscritto dal rappresentante legale di un Aderente o da 
un professionista o da un cittadino nel caso in cui questi siano l’Aderente 
stesso, al fine di accreditarsi sulla Infrastruttura interoperabilità 
PDND e utilizzare le funzionalità messe a disposizione sulla stessa. 

Utenti degli Aderenti
---------------------

Gli utenti registrati dagli Aderenti, tramite gli strumenti messi a disposizione 
dall’Infrastruttura interoperabilità PDND, e da questi delegati all’uso 
e alla gestione delle funzionalità rese disponibili dalla stessa infrastruttura.

Le funzionalità rese disponibili dall’Infrastruttura interoperabilità 
PDND agli Utenti degli Aderenti e i ruoli che questi possono ricoprire 
sono riportati nell’Allegato 2.

Attributi degli Aderenti
------------------------

Per Attributo si intende una caratteristica posseduta da un Aderente.

Sono individuate tre tipologie di Attributo:

- Attributi Certificati, ossia le caratteristiche possedute dall’Aderente 
  stesso e definite sulla base delle informazioni contenute nelle banche 
  dati di interesse nazionale e/o detenute da altre fonti autorevoli;

- Attributi Dichiarati, ossia le caratteristiche il cui possesso è stato 
  dichiarato dall’Aderente stesso sotto la propria esclusiva responsabilità;

- Attributi Verificati, ossia le caratteristiche il cui possesso è stato 
  indicato dall’Aderente stesso e verificato da almeno un altro Aderente, 
  nella veste di Erogatore, in sede di stipula di un Accordo di Interoperabilità.

L’Infrastruttura interoperabilità PDND DEVE associare a ciascun Aderente 
gli Attributi da questo posseduti e DEVE assicurare la gestione delle 
tipologie di Attributi degli Aderenti.

Per quanto concerne gli Attributi Verificati di un Aderente, gli Erogatori 
POSSONO accettare la verifica effettuata precedentemente da un altro Erogatore.

Registro degli Attributi
------------------------

Per Registro degli Attributi si intende la componente della Infrastruttura 
interoperabilità PDND in cui sono raccolti gli Attributi degli Aderenti. 

L’Infrastruttura interoperabilità PDND DEVE assicurare la gestione del 
Registro degli Attributi.

Requisiti di Fruizione
----------------------

I Requisiti di Fruizione, associati da ogni Erogatore a ciascun e-service 
pubblicato sul Catalogo API, indicano gli Attributi degli Aderenti che 
un Fruitore deve possedere per poter fruire dell’e-service.

Gli Erogatori utilizzano gli  Attributi degli Aderenti presenti nel Registro 
degli Attributi per definire i Requisiti di Fruizione degli e-service.

Catalogo API
------------

Il Catalogo API è la componente unica e centralizzata prevista dalle 
[LG INTEROPERABILITÀ TECNICA] che assicura agli Erogatori la registrazione 
e la pubblicazione dei propri e-service e ai Fruitori la consultazione 
degli e-service pubblicati.

L'Infrastruttura interoperabilità PDND integra il Catalogo API.


Il Catalogo API permette la conservazione e il recupero degli Accordi 
di Interoperabilità stipulati tra gli Aderenti. 

Accordo di Interoperabilità
---------------------------

Gli Accordi di Interoperabilità sono stipulati tra Erogatori e Fruitori 
e disciplinano le modalità - rispettivamente - di erogazione e di fruizione 
di un e-service. Gli Accordi di Interoperabilità possono disciplinare 
anche gli eventuali SLA condivisi tra Erogatori e Fruitori relativamente 
alla erogazione e fruizione di un determinato e-service.

Gli Erogatori e i Fruitori registrano nel Catalogo API gli Accordi di 
Interoperabilità tra essi stipulati.

Service Level Agreements
------------------------

Gli SLA POSSONO essere concordati tra Erogatore e Fruitore in sede di 
stipula di un Accordo di Interoperabilità per un determinato e-service 
al fine di stabilire la QoS. Gli SLA, che dovranno essere nel tempo coerenti 
con gli SLA dichiarati dal Gestore per l'operatività dell’Infrastruttura 
interoperabilità PDND,  sono applicati, misurati e gestiti da Erogatore e 
Fruitore senza alcun coinvolgimento della Infrastruttura interoperabilità 
PDND e le eventuali controversie sulla loro applicazione sono risolte 
fra questi ultimi senza che l’Infrastruttura interoperabilità PDND svolga 
alcun ruolo. 

Il Catalogo API, quale componente dell’Infrastruttura interoperabilità 
PDND, permette agli Erogatori di definire per i propri e-service gli SLI 
e gli SLO per la stipula degli SLA con i Fruitori. 

Voucher
-------

Un Voucher è la rappresentazione digitale degli elementi utili ad applicare 
i Requisiti di Fruizione richiesti per l’accesso ad ogni e-service pubblicato 
da un Erogatore.

L’Infrastruttura interoperabilità PDND, previa autenticazione del Fruitore, 
rilascia un Voucher in relazione ad ogni richiesta di fruizione di un 
e-service per cui è stato in precedenza stipulato un Accordo di Interoperabilità 
tra Fruitore ed Erogatore, registrato sulla stessa infrastruttura.

Il Fruitore presenta all’Erogatore il Voucher rilasciato dall’Infrastruttura 
interoperabilità PDND e quest’ultimo lo utilizza per verificare il soddisfacimento 
dei Requisiti di Fruizione per l’accesso all’e-service associato allo 
specifico Accordo di Interoperabilità.

Capofila
--------

I Capofila sono pubbliche amministrazioni di cui all’articolo 2, comma 2, 
lettera a) del CAD, Aderenti all’Infrastruttura interoperabilità PDND, 
che sono delegate da altra pubblica amministrazione Aderente a utilizzare 
per suo conto le funzionalità dell’infrastruttura medesima per la registrazione 
e modifica degli e-service sul Catalogo API.

Una pubblica amministrazione Aderente PUÒ candidarsi ad assumere il ruolo 
di Capofila registrando tale volontà sull’Infrastruttura interoperabilità 
PDND.

Le pubbliche amministrazioni Aderenti POSSONO delegare una o più Capofila 
tra quelle che si sono candidate a tal fine sulla Infrastruttura interoperabilità 
PDND.  

La delega alla Capofila ha effetto al momento dell’accettazione di quest’ultima 
e determina la possibilità, per i suoi Utenti degli Aderenti, di operare 
sulla Infrastruttura interoperabilità PDND per conto dell’Aderente delegante.

La delega da parte di un Aderente a un Capofila non include i poteri di 
sottoscrizione, con ruolo di fruitore, degli Accordi di Interoperabilità 
per conto dell’Aderente delegante.

Template e-service
------------------

L’Infrastruttura interoperabilità PDND favorisce i processi di co-design 
individuati nella Governance della Trasformazione del Piano Triennale 
per l’informatica nella Pubblica Amministrazione tramite il meccanismo 
dei Template.

Per Template e-service si intende la definizione di un modello dei descrittori 
di un e-service in cui restano liberi alcuni elementi operativi necessari 
alla reale operatività dell’e-service. In questa maniera il Template e-service 
resta un modello astratto a cui gli aderenti devono attenersi durante 
il processo di implementazione. 

Il Template e-service descrive quindi come un e-service DEVE erogare il 
servizio non entrando nel merito di come verrà implementato né indicando 
le tecnologie adottate per l’implementazione delle logiche di business.

Solo dopo il processo di implementazione del Template e-service si avranno 
una o più istanze di un e-service reale pronto alla pubblicazione sul 
Catalogo API.

Il co-design coinvolge:

- API Co-design Manager: è un Aderente, che all’interno del gruppo di 
  Pubbliche Amministrazioni interessate al co-design di un e-service, 
  progetta e registra il Template e-service sull’Infrastruttura interoperabilità 
  PDND provvedendo a: 

  - dichiarare, nel rispetto del MoDI, il Template e-service delle API 
    che implementa l’e-service;

  - definire quali informazioni sono necessarie per implementare il Template 
    e renderlo operativo, in questa maniera vengono definiti i margini 
    di libertà entro i quali può agire chi vuole implementare l’e-service.

- Implementatore: è un Aderente che decide di implementare l’e-service 
  descritto da un Template e-service e provvede a:

  - compilare il Template e-service definito dal API Co-design manager 
    nel rispetto dei margini di libertà previsti;     

  - prendersi carico dell’implementazione della logiche di business per 
    istanziare l’e-service. 

L’Infrastruttura interoperabilità PDND permette la ricerca e l’identificazione 
del riferimento del Template e-service registrato dall’API Co-design manager 
a tutte le Aderenti.

L’Infrastruttura interoperabilità PDND promuove e comunica la pubblicazione 
di nuove versioni di Template e-service e supporta la pubblicazione sul 
Catalogo API delle istanza implementate dagli Aderenti.

.. forum_italia::
   :topic_id: 26413
   :scope: document
