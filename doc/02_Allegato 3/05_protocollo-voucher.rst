Protocollo di emissione dei Voucher con API REST
================================================

L’Infrastruttura interoperabilità PDND DEVE assicurare l’emissione dei 
Voucher utilizzati dai Fruitori per accedere agli e-service degli Erogatori 
rendendo disponibile agli stessi delle API REST conformi alle 
[LG INTEROPERABILITÀ TECNICA].

I profili di emissione dei Voucher sono definiti come applicazione del RFC6749, 
assumendo che i Voucher sono gli Access Token indicati nell’RFC, prevedendo 
la seguente mappatura dei ruoli:

- Resource Owner: corrisponde all'Erogatore che, tramite le funzionalità 
  della Infrastruttura interoperabilità PDND per la definizione dei Requisiti 
  di fruizione degli e-service, individua le policy di accesso ai propri 
  e-service;

- Resource Server: è il sistema informatico dell’Erogatore che rende 
  disponibile l’e-service;

- Client: corrisponde al sistema informatico (di seguito Client Fruitore) 
  del Fruitore che, a valle della stipula di un Accordo di Interoperabilità 
  e l’indicazione delle finalità entro cui utilizzerà lo stesso accordo, 
  accede all’e-service erogato dal Resource Server;

- Authorization Server: corrisponde alla componente dell’Infrastruttura 
  interoperabilità PDND che emette, nel rispetto degli Accordi di 
  Interoperabilità stipulati dagli Aderenti, gli Access Token per 
  autorizzare l’accesso agli e-service degli Erogatori.

I passi previsti nel flusso base indicato in RFC6749 trovano la corrispondenza 
indicata di seguito.

- L'Authorization request ed il rilascio dell'Authorization Grant è 
  assicurato tramite la richiesta di stipula dell'Accordo di interoperabilità 
  da parte del Fruitore ed alla successiva conferma di accettazione da 
  parte dell’Erogatore. Il processo è realizzato per il tramite dell’Infrastruttura 
  interoperabilità PDND. Tali passi non sono oggetto dei profili indicati 
  di seguito ma sono garantiti dalle funzionalità per la stipula degli 
  Accordi di Interoperabilità assicurate dalla Infrastruttura interoperabilità 
  PDND;

- La Infrastruttura interoperabilità PDND DEVE erogare le funzionalità 
  di Authorization Server implementando il Token Endpoint per permettere 
  al Fruitore di dare seguito all’Access Token Request. L’Infrastruttura 
  interoperabilità PDND ricevuta l’Access Token Request di un Client 
  Fruitore autentica lo stesso e verifica la presenza e la validità 
  dell’Accordo di Interoperabilità, le finalità indicate nella richiesta 
  ed in caso di esito positivo rilascia l'Access Token in accordo con 
  quanto definito nello stesso accordo (ad esempio time-to-leave del 
  Access Token);
  
- Il Fruitore utilizza l'Access Token ricevuto dalla Infrastruttura 
  interoperabilità PDND per accedere all'e-service dell'Erogatore oggetto 
  dell’Accordo di Interoperabilità.

.. mermaid::

   sequenceDiagram
   alt Sottoscrizione Accordo di Interoperabilità
       Resource Owner (Erogatore)->>+AutorizationServer (interop PDND): Registratione E-Service
       Client (Fruitore)->>+AutorizationServer (interop PDND): Sottoscrizione E-Service    
       AutorizationServer (interop PDND)->>+Resource Owner (Erogatore): Notifica Sottoscrizione
       Resource Owner (Erogatore)->>+AutorizationServer (interop PDND): Accettazione Sottoscrizione
       AutorizationServer (interop PDND)-->>-Resource Owner (Erogatore): Accordo di Interoperabilità
   end
   alt Definizione Client
       Client (Fruitore)->>+AutorizationServer (interop PDND): Caricamento Materiale Crittografico
       Client (Fruitore)->>+AutorizationServer (interop PDND): Definizione Client
       Client (Fruitore)->>+AutorizationServer (interop PDND): Associazione Client e Materiale Crittografico
   end
   alt Accesso all'E-Service
       Client (Fruitore)->>+AutorizationServer (interop PDND): Authorization Grant
       AutorizationServer (interop PDND)-->>-Client (Fruitore): Access Token
       Client (Fruitore)->>+ResourceServer (Erogatore): Access Token
       ResourceServer (Erogatore)-->>-Client (Fruitore): Protected Resource
   end

[REST_JWS_2021_Bearer] Profilo di emissione dei Voucher JWS Bearer
------------------------------------------------------------------

Il presente profilo è definito assumendo che:

- l’Access Token Request del Client Fruitore all’Infrastruttura interoperabilità 
  PDND è basata su JSON Web Token (JWT) Profile for OAuth 2.0 (RFC7523);

- l’autenticazione del Client Fruitore da parte dell’Infrastruttura interoperabilità 
  PDND è realizzata utilizzando il materiale crittografico registrato 
  sulla stessa infrastruttura;

- l’Infrastruttura interoperabilità PDND emette un Bearer Access Token 
  OAuth2 conforme all’RFC6750 veicolato tramite l'HTTP Header Authorization 
  definito in RFC7235;

- l’Access Token emesso dall’Infrastruttura interoperabilità PDND consiste 
  in un JWS conforme all’RFC7515 firmato dall'Infrastruttura interoperabilità 
  PDND.

Sulla base dell’Accordo di interoperabilità stipulato dagli Aderenti la 
validità temporale dell’Access Token emesso dall’Infrastruttura interoperabilità 
PDND PUÒ essere basata su un  time-to-live eventualmente definito dall'Erogatore 
ed entro cui lo stesso può essere utilizzato dal Client Fruitore per accedere 
all’e-service oggetto dello specifico accordo.

Access Token Request del Client Fruitore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Le informazioni contenute nell’Access Token Request del Client Fruitore 
DEVONO permettere alla Infrastruttura interoperabilità PDND di individuare 
le seguenti informazioni:

- l'indicazione del Client Fruitore per cui si richiede l’emissione 
  dell’Access Token;

- l’indicazione dell’Accordo di interoperabilità che abilità il Client 
  Fruitore all’accesso all’e-service dell’Erogatore;

- l'indicazione della finalità associata dal Fruitore all’Accordo di 
  interoperabilità entro cui il Client Fruitore si impegna ad utilizzare 
  la risposta dell’e-service dell’Erogatore.

Access Token
^^^^^^^^^^^^

Le informazioni contenute nell’Access Token emesso dall’Infrastruttura interoperabilità PDND DEVONO permettere all'Erogatore di individuare almeno le seguenti informazioni:

- l'indicazione del Client Fruitore per cui è stato emesso l’Access Token;
  
- l’indicazione dell’Accordo di interoperabilità verificata dall’Infrastruttura 
  interoperabilità PDND che abilità il Client Fruitore all’accesso 
  all’e-service dell’Erogatore;

- l'indicazione della finalità associata dal Fruitore all’Accordo di 
  interoperabilità verificata dall’Infrastruttura interoperabilità PDND 
  entro cui il Client Fruitore si impegna ad utilizzare la risposta 
  dell’e-service dell’Erogatore.

Inoltro dell’Access Token all’Erogatore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il Client Fruitore implementa la request all’e-service del Erogatore nel 
rispetto di quanto registrato da quest'ultimo sul Catalogo API e DEVE 
inserire nella richiesta l'Access Token emesso dall’Infrastruttura 
interoperabilità PDND nell'HTTP header Authorization come indicato in 
RFC6750.

Il Fruitore assicura il tracciamento delle richieste effettuate con 
l’Access Token emesso dall’Infrastruttura interoperabilità PDND.

Verifica del Voucher da parte dell'Erogatore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

L'Erogatore, ricevuta la richiesta del Client Fruitore, DEVE almeno 
verificare:

- la validità della firma dell’Access Token apposta dall’Infrastruttura 
  interoperabilità PDND mediante il materiale crittografico generato 
  dalla stessa infrastruttura a tal fine e le informazioni contenute 
  nel JWT;

- la scadenza dell'Access Token ed il time-to-live, ove presente, nel 
  rispetto di quanto stipulato nell’Accordo di interoperabilità con il 
  Fruitore.

In caso di esito positivo delle verifiche l’Erogatore DEVE dare accesso 
al Client Fruitore all’e-service oggetto dell’Accordo di interoperabilità.

Nel caso di fallimento delle verifiche l’Erogatore NON DEVE dare accesso 
al Client Fruitore all’e-service oggetto dell’Accordo di interoperabilità.

L’Erogatore assicura il tracciamento delle richieste ricevute dai Client 
Fruitore con gli Access Token emessi dall’Infrastruttura interoperabilità 
PDND.

Le specifiche tecniche delle API REST rese disponibili dall’Infrastruttura 
interoperabilità PDND per permettere ai Client Fruitori di dare seguito 
all’Access Token Request e il dettaglio del contenuto dell’Access Token 
emesso dalla stessa infrastruttura sono oggetto della documentazione 
tecnica predisposta dal Gestore.

[REST_JWS_2021_POP] Profilo di emissione dei Voucher JWS POP
------------------------------------------------------------

Considerata la possibile esigenza che in alcuni scenari sia richiesto 
un grado di protezione aggiuntivo nel dominio di sicurezza del Fruitore, 
in base al quale un Client Fruitore, necessita di una proof-of-possession 
del materiale crittografico utilizzato per l’Access Token Request, in 
modo tale che lo stesso sia l’unico a potere utilizzare il relativo 
Access Token emesso dall’Infrastruttura interoperabilità PDND per l’accesso 
ad un determinato e-service.

Il presente profilo estende il profilo REST_JWS_2021_Bearer sopra definito 
affinché l’Access Token emesso dall’Infrastruttura interoperabilità PDND 
per l’accesso ad un determinato e-service non costituisca un token di 
accesso al portatore, e quindi utilizzabile da qualunque parte ne entri 
in possesso, ma sia resa possibile la verifica da parte dell’Erogatore 
del Client Fruitore che ha richiesto l’emissione del token e per il quale 
il token è stato emesso.

Access Token Request del Client Fruitore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Le informazioni contenute nell’Access Token Request del Client Fruitore 
DEVONO permettere alla Infrastruttura interoperabilità PDND di individuare 
le seguenti informazioni:

- l'indicazione del Client Fruitore per cui si richiede l’emissione dell’Access Token;

- l’indicazione dell’Accordo di interoperabilità che abilità il Client 
  Fruitore all’accesso all’e-service dell’Erogatore;

- l'indicazione della finalità associata dal Fruitore all’Accordo di 
  interoperabilità entro cui il Client Fruitore si impegna ad utilizzare 
  la risposta dell’e-service dell’Erogatore;

- Un proof-of-possession del materiale crittografico privato corrispondente 
  al materiale crittografico pubblico a cui l’’Access Token richiesto 
  deve essere collegato.

Access Token
^^^^^^^^^^^^

Le informazioni contenute nell’Access Token emesso dall’Infrastruttura 
interoperabilità PDND DEVONO permettere all'Erogatore di individuare 
almeno le seguenti informazioni:

- l'indicazione del Client Fruitore per cui è stato emesso l’Access Token;
  
- l’indicazione dell’Accordo di interoperabilità verificata dall’Infrastruttura 
  interoperabilità PDND che abilità il Client Fruitore all’accesso all’e-service 
  dell’Erogatore;

- l'indicazione della finalità associata dal Fruitore all’Accordo di 
  interoperabilità verificata dall’Infrastruttura interoperabilità PDND 
  entro cui il Client Fruitore si impegna ad utilizzare la risposta 
  dell’e-service dell’Erogatore;

- l’indicazione della proof-of-possession ricevuta nell’’Access Token 
  Request per cui il token è emesso.

Inoltro dell’Access Token all’Erogatore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il Client Fruitore implementa la request all’e-service del Erogatore nel 
rispetto di quanto registrato da quest'ultimo sul Catalogo API e DEVE 
inserire nella richiesta l'Access Token emesso dall’Infrastruttura 
interoperabilità PDND nell'HTTP header Authorization come indicato in 
RFC6750 e la relativa proof-of-possession collegata.

Il Fruitore assicura il tracciamento delle richieste effettuate con 
l’Access Token emesso dall’Infrastruttura interoperabilità PDND.

Verifica del Voucher da parte dell'Erogatore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

L'Erogatore, ricevuta la richiesta del Client Fruitore, DEVE almeno 
verificare:

- la validità della firma dell’Access Token apposta dall’Infrastruttura 
  interoperabilità PDND mediante il materiale crittografico generato 
  dalla stessa infrastruttura a tal fine e le informazioni contenute 
  nel JWT;

- la scadenza dell'Access Token ed il time-to-live, ove presente, nel 
  rispetto di quanto stipulato nell’Accordo di interoperabilità con il 
  Fruitore;

- la validità della proof-of-possession collegata all’Access Token.

In caso di esito positivo delle verifiche l’Erogatore DEVE dare accesso 
al Client Fruitore all’e-service oggetto dell’Accordo di interoperabilità.

Nel caso di fallimento delle verifiche l’Erogatore NON DEVE dare accesso 
al Client Fruitore all’e-service oggetto dell’Accordo di interoperabilità.

L’Erogatore assicura il tracciamento delle richieste ricevute dai Client 
Fruitore con gli Access Token emessi dall’Infrastruttura interoperabilità 
PDND.

Le specifiche tecniche delle API REST rese disponibili dall’Infrastruttura 
interoperabilità PDND per permettere ai Client Fruitori di dare seguito 
all’Access Token Request e il dettaglio del contenuto dell’Access Token 
emesso dalla stessa infrastruttura sono oggetto della documentazione 
tecnica predisposta dal Gestore.

.. forum_italia::
   :topic_id: 26437
   :scope: document
