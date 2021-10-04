Livelli di servizio della Infrastruttura interoperabilità PDND
==============================================================

Il rapporto tra l’Infrastruttura interoperabilità PDND e gli Aderenti 
è regolato dai livelli di qualità, oggetto della Lettera di Adesione, 
attesi nell’erogazione dei:

- servizi offerti agli Aderenti per la gestione degli e-service, Accordi 
  di interoperabilità e Voucher resi della Infrastruttura interoperabilità PDND;

- servizi di supporto agli Utenti degli Aderenti da parte della Infrastruttura 
  interoperabilità PDND.


In quanto segue si riportano gli indicatori di qualità utilizzati dalla 
Infrastruttura interoperabilità PDND e gli Aderenti per definire i livelli 
di qualità dei servizi che l’Infrastruttura interoperabilità PDND garantisce 
agli Aderenti, oggetto della Lettera di Adesione. 

Indicatori dei servizi/API realizzati
-------------------------------------

Tempo di risposta delle richieste su percentile
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il tempo che intercorre tra una request e la relativa response, è indice 
dell’efficienza di un servizio/API reso disponibile dall’Infrastruttura 
interoperabilità PDND. Nel dettaglio il tempo di risposta è calcolato, 
in esercizio, come il tempo intercorso tra il momento di ricezione della 
request e il momento di inoltro della relativa response. Le latenze 
determinate dal canale di comunicazione del servizio/API non sono oggetto 
del presente indicatore.

Il presente indicatore è determinato dalla media di un percentile fissato 
delle request pervenute nell’unità di tempo, dove il percentile e l’unità 
di tempo per la determinazione dell’indicatore sono individuate nella 
Lettera di adesione sottoscritta dall’Infrastruttura interoperabilità 
PDND e dagli Aderenti per singolo servizio/API, ad esempio tempo medio 
dell'85% delle richieste pervenute in 10 minuti.

La fonte per la determinazione dei tempi di ricezione delle request e 
il momento di inoltre delle relativa response è rappresentato dai log 
file tenuti dall’Infrastruttura interoperabilità PDND.

Numero di richieste per unità di tempo
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il numero di richieste soddisfatte da un servizio/API reso disponibile 
dall’Infrastruttura interoperabilità PDND è indice della capacità di 
carico gestibile dalla stessa. 

Il presente indicatore è determinato dal numero di request soddisfate, 
cioè a cui il servizio/API è riuscito a produrre response, nell’unità 
di tempo. L’unità di tempo per la determinazione dell’indicatore è 
individuata nella Lettera di adesione sottoscritta dall’Infrastruttura 
interoperabilità PDND e dagli Aderenti per singolo servizio/API, ad 
esempio numero di request soddisfatte in 10 minuti.

La fonte per la determinazione del numero di request soddisfatte è 
rappresentato dai log file tenuti dall’Infrastruttura interoperabilità 
PDND.

Numero di richieste con risposta di errore per unità di tempo
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il numero di richieste con risposta di errore di un servizio/API reso 
disponibile dall’Infrastruttura interoperabilità PDND è indice inverso 
della efficacia della stessa.

Il presente indicato è determinato del numero di request con error response 
nell’unità di tempo, escludendo gli errori imputabili agli Aderenti (ad 
esempio errata formattazione della richiesta o la irraggiungibilità dei 
servizi degli Aderenti). L’unità di tempo per la determinazione dell’indicatore 
è individuata nella Lettera di adesione sottoscritta dall’Infrastruttura 
interoperabilità PDND e dagli Aderenti per singolo servizio/API, ad esempio 
numero di request con error response in 10 minuti. Si evidenzia che tale 
indicatore è inversamente proporzionale all’efficacia del servizio/API.

La fonte per la determinazione del numero di request con error response 
è rappresentato dai log file tenuti dalla Infrastruttura interoperabilità 
PDND.

Indicatori dei servizi di supporto
----------------------------------

Tempestività di ripristino dell’operatività
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il presente indicatore si applica a non conformità funzionali e non funzionali 
rilevate dagli Aderenti ed è calcolato come la differenza in ore tra il 
momento dell’avvio del processo di risoluzione del malfunzionamento e 
il termine della risoluzione delle stesso da parte della Infrastruttura 
interoperabilità PDND.

La fonte per la determinazione dell’indicatore è rappresentato dal momento 
temporale delle comunicazione di merito realizzate tra l’Infrastruttura 
interoperabilità PDND e gli Aderenti (presa in carico del ticket da parte 
del Gestore).

Tempestività di risposta a segnalazioni di anomalie
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il presente indicatore si applica a non conformità funzionali e non funzionali 
evidenziate dagli Aderenti. L’indicatore è calcolato come la differenza 
in ore tra il momento della segnalazione e la presa in carico della stessa 
da parte della Infrastruttura interoperabilità PDND.

La fonte per la determinazione dell’indicatore è rappresentato dal momento 
temporale delle comunicazione di merito realizzate tra l’Infrastruttura 
interoperabilità PDND e gli Aderenti.
