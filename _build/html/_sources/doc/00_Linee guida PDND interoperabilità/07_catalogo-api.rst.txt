Catalogo API nella Infrastruttura interoperabilità PDND
=======================================================

Il MoDI individua nelle [LG INTEROPERABILITÀ TECNICA] il Catalogo delle 
API quale componente, unica e centralizzata, che assicura alle parti 
coinvolte nel rapporto di erogazione e fruizione la consapevolezza sulle 
API disponibili e, per ognuna di esse, i livelli di servizio dichiarati.

Il Catalogo API è realizzato al fine di:

- favorire l’uso degli e-service grazie alla loro pubblicazione e la messa 
  a disposizione della relativa documentazione tecnica;

- agevolare la gestione del ciclo di vita degli e-service;

- mitigare la creazione di interfacce ridondanti e/o con semantica sovrapposta.

Il Catalogo API permette agli Erogatori la registrazione e pubblicazione 
degli e-service.

La registrazione degli e-service è realizzata dagli Erogatori che DEVONO:

- assicurare l’utilizzo delle tecnologie e l’applicazione dei pattern e 
  dei profili individuati dal MoDI, ed in particolare dalle [LG INTEROPERABILITÀ TECNICA];

- definire i Requisiti di Fruizione individuando gli attributi che devono 
  essere posseduti dai Fruitori per accedere allo specifico e-service.

La pubblicazione degli e-service è realizzata dagli Erogatori per rendere 
gli stessi disponibili agli Aderenti che soddisfano i Requisiti di Fruizione 
definiti.

Le informazioni presenti nel Catalogo API sono nella responsabilità degli 
Erogatori, che DEVONO provvedere alla gestione del ciclo di vita dei propri 
e-service per il tramite dei propri Utenti degli Aderenti oppure delegando 
questo compito a uno o più Capofila.

Il Catalogo API permette ai Fruitori di consultare l’elenco degli e-service 
pubblicati dagli Erogatori al fine di conoscerne le modalità di accesso 
e i Requisiti di Fruizione, nonché  verificarne l’utilità di utilizzo 
per il raggiungimento delle proprie finalità.

Ogni e-service pubblicato sul Catalogo API si compone delle seguenti parti:

- i descrittori dell’e-service, che definiscono le informazioni relative 
  alla natura dell’e-service e le informazioni tecniche per usufruire 
  dello stesso;

- di una interfaccia (idl) per usufruire dell’e-service;

- la documentazione accessoria e manualistica per l’utilizzo del e-service.

Gli Erogatori, relativamente ai singoli e-service registrati nel Catalogo 
API, DEVONO assicurare l’utilizzo di una delle tecnologie indicata dal MoDI 
e, in particolare, dalle [LG INTEROPERABILITÀ TECNICA] attraverso la 
definizione di interfacce.

Nella definizione dei propri e-service, gli Erogatori DEVONO prevedere 
un campo per l’inoltro da parte dei Fruitori del riferimento ai documenti 
informatici che possano provare la legittimità dello specifico trattamento 
dei dati personali effettuato in occasione di ogni singolo utilizzo degli 
e-service. In occasione di ogni singolo utilizzo degli e-service a seguito 
della stipula di un Accordo di Interoperabilità:

- il Fruitore DEVE assicurare il corretto popolamento del suddetto riferimento 
  sotto la propria completa responsabilità;

- l’Erogatore NON DEVE dare seguito alla richiesta da parte del Fruitore 
  in assenza del suddetto riferimento.

La raccolta e la memorizzazione dei riferimenti ai documenti informatici 
che possano provare la legittimità degli specifici trattamenti dei dati 
personali effettuati in occasione di ogni singolo utilizzo di un e-service
non avviene sulla Infrastruttura interoperabilità PDND.

Nel caso in cui il Fruitore sia un soggetto privato, gli stessi DEVONO 
implementare e assicurare la disponibilità di una API per recuperare i 
documenti che attestano la legittimità dello specifico trattamento dei 
dati personali a partire dal riferimento indicato dal Fruitore nel 
singolo utilizzo dell’e-service.

Contestualmente all’utilizzo degli e-service:

- il Fruitore DEVE memorizzare tutti i documenti che possono provare 
  la legittimità del trattamento, associati univocamente al suddetto riferimento, 
  assicurandone l’autenticità e l’integrità;

- l’Erogatore DEVE memorizzare la richiesta del Fruitore e associarla 
  univocamente al suddetto riferimento, assicurandone l'autenticità e 
  l’integrità;

- il Fruitore e l’Erogatore DEVONO assicurare, in qualsiasi momento, 
  l’accesso dell’interessato e degli organi di controllo alle informazioni 
  memorizzate.

Per la pubblicazione degli e-service sul Catalogo API, gli Erogatori DEVONO 
assicurare la disponibilità di un'interfaccia utilizzabile dai Fruitori.

Gli Erogatori DOVREBBERO: 

- metadatare gli e-service utilizzando il modello dati supportato 
  dall’Infrastruttura interoperabilità PDND, coerentemente ai vocabolari 
  controllati e le ontologie relative ai servizi pubblici afferenti gli 
  eventi aziendali e della vita definiti a livello europeo e a livello 
  italiano;

- utilizzare i vocabolari controllati e le ontologie definiti in attuazione 
  della “strategia  nazionale dati” di cui al comma 4 dell’articolo 50-ter 
  del CAD per la metadatazione dei dati oggetto dei propri e-service nelle
  modalità supportate dall’Infrastruttura interoperabilità PDND.

Relativamente agli e-service pubblicati, gli Erogatori NON POSSONO modificare 
elementi che impattano sui Fruitori e gli Accordi di interoperabilità 
già stipulati.

Gli Erogatori NON POSSONO dismettere una versione di e-service in presenza 
di un Accordo di Interoperabilità attivo che ne consente l’utilizzo da 
parte di un Fruitore.

L’Allegato 2 individua le modalità che gli Erogatori DEVONO attuare per 
registrare, pubblicare e aggiornare le informazioni relative ai propri 
e-service sul Catalogo API.

L’Allegato 2 individua le modalità che i Fruitori DEVONO attuare per 
consultare l’elenco degli e-service pubblicati sul Catalogo API.
