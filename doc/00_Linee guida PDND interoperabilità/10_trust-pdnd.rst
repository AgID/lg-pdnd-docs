Trust Infrastruttura interoperabilità PDND e sistemi informatici degli Aderenti
===============================================================================

Per il tramite delle funzionalità rese disponibili dall’Infrastruttura 
interoperabilità PDND è realizzato il trust machine-to-machine tra: 

- sistemi informatici degli Aderenti e sistemi informatici della Infrastruttura 
  interoperabilità PDND;
  
- sistemi informatici degli Aderenti. 

Gli Aderenti DEVONO generare il materiale crittografico utilizzato nel 
trust.

Gli Aderenti DEVONO assicurare la riservatezza del materiale crittografico 
adottando opportune misure di sicurezza che preservino l’utilizzo improprio 
dello stesso. 

Gli Aderenti DEVONO registrare e mantenere sull’Infrastruttura interoperabilità 
PDND il materiale crittografico pubblico utilizzato dai propri sistemi 
informatici che interagiranno con la Infrastruttura interoperabilità PDND 
e i sistemi informatici degli altri Aderenti.

L’Infrastruttura interoperabilità PDND DEVE generare il materiale crittografico 
utilizzato dagli Aderenti per verificare i Voucher emessi dalla stessa 
infrastruttura. 

L’Infrastruttura interoperabilità PDND DEVE assicurare la riservatezza 
del materiale crittografico adottando opportune misure di sicurezza che 
preservino l’utilizzo improprio degli stessi. 

L’Infrastruttura interoperabilità PDND DEVE rendere disponibili agli 
Aderenti il materiale crittografico pubblico necessario alla verifica 
dei Voucher emessi dalla stessa infrastruttura.

Per dare seguito alle transazioni tra Erogatore e Fruitore sulla base 
di un Accordo di Interoperabilità, i sistemi informatici degli stessi 
DEVONO realizzare i seguenti passi:

1. il sistema informatico del Fruitore richiede all’Infrastruttura interoperabilità 
   PDND  l'emissione di un Voucher riconducibile all’Accordo di Interoperabilità 
   e alla finalità entro cui le transazioni saranno realizzate, utilizzando 
   il materiale crittografico registrato sull’Infrastruttura interoperabilità 
   PDND;
   
2. l’Infrastruttura interoperabilità PDND emette un Voucher, con validità 
   temporale limitata, contenente le informazioni necessarie ad identificare 
   il Fruitore e l’Accordo di Interoperabilità entro cui il Voucher è 
   stato emesso, utilizzando il materiale crittografico a tal fine generato 
   dalla stessa infrastruttura;
   
3. il sistema informatico del Fruitore utilizza il Voucher per richiedere 
   accesso all’e-service pubblicato sul Catalogo API dall'Erogatore relativo 
   all’Accordo di Interoperabilità entro cui le transazioni sono realizzate;
   
4. il sistema informatico dell’Erogatore ricevuto il Voucher, ne verifica 
   l’emissione da parte dell’Infrastruttura interoperabilità PDND e la 
   validità temporale e solo in caso di verifica positiva il sistema 
   informatico dell’Erogatore applica le regole di autorizzazione 
   associate allo specifico Accordo di interoperabilità, nella sua completa 
   responsabilità, per abilitare l’accesso del sistema informatico del 
   Fruitore e provvede a dare seguito alle transazioni per l’e-service 
   richiesto. 

L’Erogatore al momento della definizione dell’Accordo di Interoperabilità 
PUÒ prevedere tra i Requisiti di Fruizione che il sistema informatico 
del Fruitore sia identificato direttamente al precedente passo 4. 
In questo caso il Fruitore utilizza, al precedente passo 3, il materiale 
crittografico registrato sull’Infrastruttura interoperabilità PDND per 
decorare il Voucher per permettere all’Erogatore di identificarlo.

Le tecnologie utilizzate per l’implementazione dei Voucher che l’Infrastruttura 
interoperabilità PDND DEVE assicurare sono indicate nell’Allegato 3.

Gli Aderenti DEVONO implementare i passi indicati in precedenza per il 
tramite dell’Infrastruttura interoperabilità PDND nelle modalità 
indicate nell’Allegato 3. 
