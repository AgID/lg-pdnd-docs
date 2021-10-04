Trust degli Aderenti alla PDND
==============================

La Infrastruttura Interoperabilità PDND DEVE fornire agli Aderenti le 
funzionalità necessarie ad assicurare l’autenticazione e autorizzazione 
dei Fruitori al fine di accedere agli e-service messi a disposizione 
degli Erogatori.

L'identificazione degli Aderenti, assicurata dal processo di accreditamento 
all’Infrastruttura interoperabilità PDND, determina un insieme definito 
di partecipanti (“sistema chiuso”). 

Si assume come prerequisito per la comunicazione tra Erogatori e Fruitori 
che:

- gli Erogatori DEVONO registrare sul Catalogo API gli e-service che mettono 
  a disposizione dei Fruitori e i relativi Requisiti di fruizione che 
  questi ultimi devono soddisfare per accedere agli e-service;

- gli Erogatori e Fruitori DEVONO stipulare sulla Infrastruttura interoperabilità 
  PDND un Accordo di interoperabilità per gli e-service a cui il Fruitore 
  ha intenzione di accedere;

- il Fruitore DEVE dichiare le finalità entro cui utilizzerà gli e-service 
  oggetto degli Accordi di interoperabilità stipulati.

Il trust realizzato tra l’Infrastruttura interoperabilità PDND e gli Aderenti è fondato sul:

- materiale crittografico registrato sull’Infrastruttura interoperabilità 
  PDND dai Fruitori;

- la certezza della fonte per la verifica dello stesso materiale crittografico 
  realizzata dall’Infrastruttura interoperabilità PDND.

I Fruitori DEVONO registrare sulla Infrastruttura interoperabilità PDND 
i loro sistemi informatici (di seguito Client Fruitore) che utilizzeranno 
gli e-service pubblicati sul Catalogo API dagli Erogatori.

Fatta salva la necessità di registrare almeno un Client Fruitore per potere 
fruire degli e-service pubblicati sul Catalogo API dagli Erogatori, i 
Fruitori POSSONO registrare più Client Fruitore sull’ Infrastruttura 
interoperabilità PDND.

Per ogni Client Fruitore DEVE essere associato il materiale crittografico 
generato dal Fruitore stesso.

Per garantire la continuità della fruizione in caso di aggiornamento degli 
algoritmi (si veda RFC7696 Algorithm Agility sezione 2.3) l’Infrastruttura 
interoperabilità PDND DEVE permettere di associare più istanze di materiale 
crittografico ai Client Fruitore .

I Fruitori relativamente al materiale crittografico associato ai Client 
Fruitore registrati sulla Infrastruttura interoperabilità PDND DEVONO 
assicurare i necessari aggiornamenti in caso di compromissione del materiale 
crittografico.

L’Infrastruttura interoperabilità PDND DEVE assicurare l’integrità e 
l'immodificabilità del materiale crittografico associato ai Client Fruitore. 

I Fruitori per ogni Accordo di interoperabilità stipulato per il tramite 
dell’Infrastruttura interoperabilità PDND e per ogni finalità registrata 
per lo stesso accordo DEVONO associare i Client Fruitore che accederanno 
agli e-service oggetto dell’accordo per dare seguito alla specifica finalità. 
Un Fruitore PUÒ associare uno stesso Client Fruitore a più Accordi di 
interoperabilità e così anche per le finalità.

L’Infrastruttura interoperabilità PDND DEVE realizzare la funzione di 
Registry per il materiale crittografico registrato dagli Aderenti.

La Infrastruttura interoperabilità PDND DEVE rendere disponibili agli 
Utenti degli aderenti le funzionalità per permettere agli:

- Operatori Amministrativi di registrare un Client Fruitore e associarlo 
  ad un Operatore Sicurezza;

- Operatori di Sicurezza di registrare il materiale crittografico pubblico 
  dei Client Fruitore a cui è associato.

L’Infrastruttura interoperabilità PDND DEVE tracciare le operazione 
realizzate dagli Utenti degli Aderenti relative alla: 

- registrazione dei Client Fruitore;
  
- associazione del materiale crittografico ai Client Fruitore;
  
- registrazione dei Client Fruitore che accedono agli e-service oggetto 
  di Accordi di interoperabilità.

L’Infrastruttura interoperabilità PDND DEVE rendere accessibile il 
materiale crittografico pubblico registrato dagli Aderenti. L'accesso 
DEVE essere garantito tramite API REST conformi alle [LG INTEROPERABILITÀ TECNICA] 
applicando il pattern sicurezza [ID_AUTH_CHANNEL_01] con l’utilizzo di 
certificati qualificati ai sensi del [eIDAS] e delle [LG SICUREZZA].

Gli Erogatori DEVONO utilizzare sui propri sistemi informatici che 
implementano gli e-service registrati sul Catalogo API certificati X.509, 
nel rispetto delle [LG SICUREZZA], per assicurare almeno l’applicazione 
del pattern di sicurezza [ID_AUTH_CHANNEL_01] individuato nelle 
[LG INTEROPERABILITÀ TECNICA]. Gli Erogatori si dotano dei suddetti 
certificati X.509 al di fuori della Infrastruttura interoperabilità PDND.

Sulla base della tipologia dei dati oggetto delle comunicazioni realizzate 
per il tramite degli e-service messi a disposizione dei Fruitori, gli 
Erogatori DEVONO individuare gli opportuni pattern e profili previsti 
nelle [LG INTEROPERABILITÀ TECNICA].
