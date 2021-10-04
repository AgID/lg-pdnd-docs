Raccolta delle informazioni relative agli accessi e alle transazioni 
====================================================================

L’Infrastruttura interoperabilità PDND fornisce il supporto per il tracciamento 
e l’osservazione delle interazioni tra Erogatori e Fruitori. L’Infrastruttura 
interoperabilità PDNDcolleziona alcune  informazioni utili a misurare 
l'efficacia  dell’interoperabilità nel tempo ma non ha lo scopo di 
verificare gli SLA concordati tra Erogatori e Fruitori. 

In particolare, l’articolo 50-ter, comma 2, stabilisce che l’Infrastruttura 
interoperabilità PDND rende possibile l’interoperabilità dei sistemi 
informativi e delle basi di dati anche mediante “la raccolta e conservazione 
delle informazioni relative agli accessi e alle transazioni effettuate 
suo tramite”.

A tal fine, i servizi previsti includono:

- Probing: verifica nel tempo della disponibilità delle API presenti nel 
  relativo Catalogo dichiarate "in erogazione". L’Aderente che eroga il 
  servizio deve includere nella firma dell’e-service una chiamata 
  secondo le indicazioni presenti nella documentazione tecnica caricata 
  sul portale della Infrastruttura interoperabilità PDND. L’Infrastruttura 
  Interoperabilità PDND conserva, anche in maniera aggregata, gli esiti 
  delle chiamate in termini di: 

  - successo/fallimento;
 
  - coordinate temporali;
  
  - tempi di risposta. 

- Auditing: registrazione delle autorizzazioni (Voucher) rilasciate dalla 
  Infrastruttura Interoperabilità PDND e richieste dai Fruitori. 
  L’Infrastruttura interoperabilità conserva per ogni evento di 
  autorizzazione almeno:

  - le coordinate temporali del rilascio del Voucher;
  
  - il riferimento all’Accordo di interoperabilità stipulato;
  
  - la finalità entro cui saranno realizzate le transazioni;
  
  - l'URL dell'API richiesta;
  
  - eventuali parametri con cui il Fruitore decora la richiesta di 
    autorizzazione.

Il Gestore dell’Infrastruttura interoperabilità PDND PUÒ implementare 
anche un servizio di Tracing, ossia un servizio di raccolta dei tracciati 
che descrivono l’andamento esclusivamente quantitativo delle transazioni 
avvenute tra ciascun Erogatore e ciascun Fruitore. Le informazioni raccolte 
mediante tale servizio - che non dovranno comprendere il contenuto informativo 
scambiato tra Erogatore e Fruitore - descriveranno il numero di transazioni 
intervenute tra Erogatore e Fruitore in un determinato arco di tempo. 
In caso di implementazione di tale servizio, il Gestore informa gli Aderenti c
on il preavviso indicato nella Lettera di Adesione. In tal caso, gli Aderenti 
sono tenuti a depositare, con le modalità e le tempistiche che saranno 
indicate nella Lettera di Adesione, sulla Infrastruttura interoperabilità 
PDND i tracciati delle transazioni a cui hanno partecipato in qualità 
sia di Erogatore sia di Fruitore. 

Le informazioni depositate dagli Aderenti sull’Infrastruttura interoperabilità 
PDND DEVONO essere aggregate in base ai seguenti criteri:

- coordinate temporali con la granularità che sarà definita; 

- Aderenti coinvolti nella transazione e loro ruolo;	

- e-service oggetto della transazione (endpoint);

- esito della chiamata/risposta.

Ulteriori criteri di aggregazione delle informazioni depositate dagli 
Aderenti sull’Infrastruttura interoperabilità PDND POSSONO essere definiti 
dal Gestore.

L’obiettivo della Infrastruttura interoperabilità PDND resta ancorato 
alla realizzazione di un punto unico di raccolta di queste informazioni, 
non essendo tenuta a svolgere un compito di riconciliazione dei tracciati 
di una stessa transazione e provenienti da Aderenti diversi. 
