Gestione degli Attributi degli Aderenti
=======================================

L’Infrastruttura interoperabilità PDND registra gli Attributi degli 
Aderenti associati ad ogni singolo Aderente.

L’Infrastruttura interoperabilità PDND assicura la gestione delle seguenti 
tipologie di Attributi degli Aderenti:

- Certificati: associati agli Aderenti in maniera automatica dalla Infrastruttura 
  interoperabilità PDND a partire dalle informazioni contenute nelle banche 
  dati di interesse nazionale, in prima istanza l’Indice dei domicili 
  digitali delle pubbliche amministrazioni e dei gestori di pubblici 
  servizi (IPA) di cui all’articolo 6-ter del CAD, l’Indice nazionale 
  delle imprese e dei professionisti (INI-PEC) di cui all’articolo 6-bis 
  del CAD e l’Indice nazionale dei domicili digitali delle persone fisiche, 
  dei professionisti e degli altri enti di diritto privato, non tenuti 
  all'iscrizione in albi, elenchi o registri professionali o nel registro 
  delle imprese (INAD) di cui all’articolo 6-quater del CAD, nonchè le 
  ulteriori basi di dati di cui all’art. 60 del CAD o altre eventuali 
  fonti autoritative. Questa tipologia di attributi è immediatamente 
  spendibile ai fini dell’autorizzazione all’accesso agli e-service in 
  quanto certificata da una fonte autoritativa.

- Dichiarati: i Fruitori dichiarano di possedere sotto la loro responsabilità, 
  gli attributi richiesti al fine di soddisfare i Requisiti di Fruizione 
  degli e-service per cui richiedono la stipula di un Accordo di Interoperabilità. 
  L’Infrastruttura interoperabilità PDND registra gli Attributi Dichiarati 
  per singolo Aderente. Questa tipologia di attributi è immediatamente 
  spendibile ai fini dell’autorizzazione all’accesso agli e-service in 
  quanto la loro veridicità è garantita dal Fruitore sotto la sua esclusiva 
  responsabilità.

- Verificati: i Fruitori dichiarano gli attributi posseduti al fine di 
  soddisfare i Requisiti di Fruizione degli e-service per cui richiedono 
  la stipula di un Accordo di Interoperabilità. L’Infrastruttura interoperabilità 
  PDND registra gli Attributi Dichiarati per singolo Aderente in relazione 
  allo specifico Accordo di Interoperabilità e , a differenza degli attributi 
  Dichiarati, a valle del riscontro positivo  da parte dell’Erogatore 
  di uno degli e-service richiesti dal Fruitore che prevedano lo stesso 
  Attributo. L’Infrastruttura interoperabilità PDND assicura la memorizzazione 
  del momento temporale della registrazione degli Attributi degli Aderenti.

In merito agli Attributi Verificati si precisa che:

1. Un Fruitore NON DOVREBBE chiedere la verifica di un attributo Verificato 
   che sia stato precedentemente rifiutato da un Erogatore.

2. Un Erogatore PUÒ definire il periodo temporale di validità di un attributo 
   Verificato ai fini della fruizione dei propri e-service, scaduto il 
   quale l’attributo dovrà essere  verificato nuovamente. Alla scadenza 
   del periodo di validità individuato dall’Erogatore, l'attributo resta 
   valido salvo il caso di un esplicito riscontro negativo della verifica 
   fornito anche solo da un Erogatore.

3. Un Erogatore PUÒ ritenere valida la verifica degli attributi realizzata 
   da altri Erogatori in sede di stipula di un Accordo di Interoperabilità 
   per la fruizione dei propri e-service.

4. Nel caso in cui l’esito della verifica effettuata da un Erogatore 
   relativamente ad un attributo di un Fruitore contrasti con quanto in 
   precedenza constatato da un altro Erogatore per lo stesso Fruitore, 
   l’Infrastruttura interoperabilità PDND comunica la circostanza agli 
   Erogatori interessati invitandoli a dirimere l’ambiguità e a segnalare 
   l’eventuale volontà di sospendere gli Accordi di Interoperabilità per 
   i quali l’attributo risulta abilitante ai fini dell’accesso ai relativi 
   e-service.

L’Infrastruttura interoperabilità PDND DEVE inserire nel Registro degli 
Attributi:

1. gli attributi certificabili presenti nelle basi dati di interesse 
   nazionale, o in altre fonti autorevoli, ove integrate con la Infrastruttura 
   interoperabilità PDND;

2. gli attributi proposti dagli Erogatori al momento della definizione 
   dei Requisiti di Fruizione degli e-service pubblicati sul Catalogo API.

Gli Erogatori, al momento della definizione dei Requisiti di Fruizione 
dei propri e-service, DEVONO verificare se nel Registro degli Attributi 
sono presenti gli Attributi degli Aderenti a loro necessari. Effettuata 
la predetta verifica, gli Erogatori DEVONO:

- in caso di riscontro positivo, utilizzare gli attributi di loro interesse 
  eventualmente modificando la tipologia da Dichiarati a Verificati.

- in caso di riscontro negativo, proporre la definizione di un nuovo 
  attributo specificando la relativa tipologia richiesta (Dichiarato o 
  Verificato). Gli Erogatori, nel proporre la definizione di un nuovo 
  attributo alla Infrastruttura interoperabilità PDND, DEVONO associare, 
  quando possibile, all’attributo in questione riferimenti unici presenti 
  nelle fonti autorevoli integrate sull’Infrastruttura interoperabilità 
  PDND (ad esempio, riferimento normativo gestito dal sistema Normattiva). 
  Ricevuta la proposta di definizione di un nuovo attributo formulata 
  da un Erogatore, l’Infrastruttura interoperabilità PDND provvederà ad 
  aggiungere l’attributo al Registro degli Attributi e comunicare tale 
  circostanza all’Erogatore. 

L'Infrastruttura interoperabilità PDND DEVE mettere a disposizione del 
soggetto competente gli strumenti necessari a supporto della ispezione 
periodica alla ricerca di eventuali attributi equivalenti all’interno 
Registro degli Attributi. Nel caso in cui il  soggetto competente constati 
la presenza di due o più attributi equivalenti, l’Infrastruttura interoperabilità 
PDND DEVE agevolare la comunicazione della circostanza agli Aderenti interessati 
coinvolti negli Accordi di interoperabilità che includono l’utilizzo dei 
suddetti attributi. Gli Aderenti interessati DEVONO comunicare le loro 
deduzioni sugli attributi equivalenti. In caso di riscontro positivo 
sull’equivalenza degli attributi a seguito dell’avallo dagli Aderenti, 
con l’obiettivo di ridurre lo sforzo di adeguamento degli aderenti, 
l’Infrastruttura interoperabilità PDND DEVE permettere agli Aderenti 
Erogatori: 

- la creazione di un nuovo e-service che, a partire dall’e-service con 
  attributi ridondanti all’interno del Registro degli Attributi, si 
  adegui alla normalizzazione degli attributi equivalenti; 

- la migrazione degli Accordi di interoperabilità precedentemente stipulati, 
  dagli e-service non normalizzati verso i nuovi e-service normalizzati, 
  prevedendo un’accettazione e conferma esplicita da parte dei Fruitori 
  coinvolti.
  
L’Infrastruttura interoperabilità PDND provvede a:

1. aggiornare l’associazione tra gli Aderenti e gli Attributi Certificati 
   dipendenti dalle variazioni registrate direttamente dalle basi dati 
   di interesse nazionale o altre fonti autorevoli utilizzate;

2. recepire le variazioni comunicate dalle fonti autorevoli integrate 
   sull’Infrastruttura interoperabilità PDND (ad esempio aggiornamento 
   del riferimento normativo ove segnalato dal sistema Normattiva), 
   determinare se gli Attributi associati ai riferimenti unici indicati 
   nelle variazioni ricevute sono Dichiarati o Certificati, e segnalare 
   agli Aderenti interessati la necessità di valutare l’impatto delle 
   variazioni sopravvenute.

Gli Aderenti DEVONO segnalare all’Infrastruttura interoperabilità PDND 
ogni variazione sopravvenuta di loro conoscenza in relazione agli attributi, 
e nello specifico:

- i Fruitori DEVONO segnalare le variazioni relativamente agli attributi 
  dichiarati associati ad essi;

- i Fruitori DEVONO segnalare le variazioni relativamente agli attributi 
  verificati da essi indicati;

- gli Erogatori DEVONO segnalare le variazioni relativamente agli attributi 
  verificati relativi ad Accordi di interoperabilità dei propri e-service.

L’Infrastruttura interoperabilità PDND, ricevute le segnalazioni di cui 
sopra, DEVE comunicare le circostanza agli Aderenti interessati che valutano 
l’impatto sugli Accordi di interoperabilità di loro interesse e comunicano 
alla Infrastruttura interoperabilità PDND le loro decisioni in merito 
agli stessi (mantenimento, sospensione o terminazione).

.. forum_italia::
   :topic_id: 26415
   :scope: document
