Materiale crittografico
=======================

I Fruitori tramite le funzionalità della Infrastruttura interoperabilità 
PDND associano ad ognuno dei propri Client Fruitore il materiale crittografico.

Il materiale crittografico generato nel dominio dei Fruitori DEVE rispettare 
quanto indicato dal Gestore nella documentazione tecnica predisposta dallo 
stesso per attuare quanto disposto nel presente Allegato, posto che:

- il materiale crittografico deve rispettare le “Raccomandazioni in merito 
  agli algoritmi per XML Canonicalization, Digest and signature public 
  key SOAP e Digest and signature public key REST” previste dalle 
  [LG SICUREZZA];

- il materiale crittografico NON DEVE essere utilizzato con algoritmi 
  di Message Authentication Code (MAC);

- il materiale crittografico associato ai Client Fruitore NON DEVE mai 
  contenere chiavi private;

- la Infrastruttura interoperabilità PDND pubblica il materiale crittografico 
  in formato [JWK] RFC7517 Sezione 5 tramite API REST conformi alle 
  [LG INTEROPERABILITÀ TECNICA];

- la Infrastruttura interoperabilità PDND genera ed associa un identificativo 
  univoco al materiale crittografico registrato dai Fruitori;

- i Fruitori NON POSSONO modificare l'identificativo univoco generato 
  dalla Infrastruttura interoperabilità PDND.

La Infrastruttura interoperabilità PDND NON DEVE permettere di associare 
uno specifico materiale crittografico a più Client Fruitore.

La Infrastruttura interoperabilità PDND in caso di variazione del materiale 
crittografico di un Client Fruitore DEVE permettere agli Erogatori degli 
e-service fruiti dallo stesso Client Fruitore e per cui è abilitata 
l’opzione “Voucher PoP”.

.. forum_italia::
   :topic_id: 26436
   :scope: document
