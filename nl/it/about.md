---

copyright:
  years: 2017
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Informazioni su Hardware Firewall (Shared)
{: #about-hardware-firewall-shared-}

Un Hardware Firewall (Shared) è un dispositivo di rete collegato in upstream da un server. Il firewall blocca il traffico non desiderato da un server prima che lo raggiunga. Il vantaggio principale di avere un Hardware Firewall è che un server deve gestire solo il traffico 'buono' e nessuna risorsa viene sprecata con il traffico 'cattivo'. 

L'Hardware Firewall (Dedicated) utilizza una piattaforma aziendale a più tenant per proteggere un server individuale.  Può essere acquistato con il server o aggiunto successivamente.  Fornisce la sicurezza di rete virtualizzata tramite la propria tecnologia Virtual Domain (VDOM), fornendo i domini di sicurezza virtualizzati che vengono forniti e gestiti separatamente.  

Poiché esistono più clienti associati all'hardware, se il firewall ha un malfunzionamento o viene sopraffatto da un attacco, può venire coinvolto ogni cliente che condivide l'istanza dell'Hardware Firewall (Shared). 

Possono essere configurate fino a 79 regole del firewall per gli indirizzi IP instradati staticamente e primari assegnati al server. I report dei firewall condivisi sono disponibili in base all'attività di un solo IP per un intervallo di date selezionato.
I clienti possono gestire il firewall in due modi: il portale di controllo SoftLayer (la scheda del firewall nella pagina dei dettagli del server protetto) e le API SLDN SoftLayer.

Poiché la larghezza di banda del server viene registrata nella porta di switch del server, il traffico bloccato dall'Hardware Firewall (Shared) non viene contato nelle assegnazioni mensili, eliminando la necessità di pagare per il traffico non desiderato.

## Panoramica e funzioni

**Utilizzo previsto:** protezione dell'IP primario di un solo server

**Interfaccia utente:** integrata nel portale di controllo e nell'API SoftLayer

**Funzioni:** Filtraggio stateful dei pacchetti, regole del firewall Ingress, IPv4, IPv6, Registrazione di base

**Velocità effettiva:** 10Mbps, 100Mbps, 1000Mbps o 2000Mbps 

È necessario che la velocità effettiva dell'istanza dell'Hardware Firewall (Shared) corrisponda alla velocità di uplink del server a cui viene aggiunto il firewall.
