# Prodotto
PSLP : Piattaforma Servizi Lavoro Piemonte - Versione 2.3.2

# Descrizione del prodotto

La piattaforma permette di gestire diversi servizi legati alle tematiche del Lavoro gestite da Regione Piemonte. Tali servizi possono essere rivolti sia ai cittadini che agli utenti dei Centri per l'impiego. Attraverso il servizio applicativo, infatti l’operatore dei Centri per l’Impiego potrà gestire l’afflusso al CPI mediante la configurazione di calendari e, qualora necessario sostituirsi al cittadino per fissare un appuntamento.
Al cittadino sono rese disponibili diversi servizi specifici: 
- gestione del proprio "fascicolo" (composto di dati presenti nella SAP ANPAL);
- Prenotare appuntamenti con il CPI;
- Richieste per il "collocamento mirato", gestione del reddito e dei famigliari a carico;
- adesioni al piano "Garanzia Giovani"; 
- gestire la "dichiarazione di disponibilità";
- Visualizzazione su mappa dell'ubicazione dei CPI e degli sportelli;
- gestione delle autorizzazioni al trattamento dei dati personali e informativa sulla privacy.

Il prodotto è composto dalle seguenti componenti:
- [pslpdb](https://github.com/regione-piemonte/pslp-2.3.2-pslpdb): 			 script DDL/DML per la creazione ed il popolamento iniziale del DB;
- [pslwcl](https://github.com/regione-piemonte/pslp-2.3.2-pslwcl): 			 Client Web (Angular) per la piattaforma servizi lavoro piemonte;
- [pslweb](https://github.com/regione-piemonte/pslp-2.3.2-pslweb): 			 Componente SPA con servizi REST per pslwcl;
- [pslorch](https://github.com/regione-piemonte/pslp-2.3.2-pslorch): 			 Orchestratore Piattaforma Servizi Lavoro Piemonte;
- [pslcommonobj](https://github.com/regione-piemonte/pslp-2.3.2-pslcommonobj): Libreria di classi usate trasversalmente nel prodotto.
	
Questa versione di prodotto è in dismissione alla fine del 2025, la nuova versione ha subito una profonda trasformazione, ed è disponibile qui:
https://github.com/regione-piemonte/pslp

# Prerequisiti di sistema

Una istanza DB Oracle (v. 11 o sup.) ed un'utenza con privilegi per l'esecuzione di istruzioni DDL di creazione tabelle ed altri oggetti DB, ed una eventuale utenza separata per l'esecuzione di istruzioni DML di Create, Readd, Update e Delete sui dati.
Una istanza di application server J2EE come REDHAT JBOSS EAP 6.4.5 .
Una istanza di web server (preferibilmente apache).
Per la compilazione/build della componente pslweb sono rese disponibili nella directory "lib" una serie di librerie predisposte da CSI Piemonte per un uso trasversale nei prodotti realizzati, o per uso specifico in altri prodotti con cui PSLP si interfaccia. Indicazioni più specifiche sono disponibili nella documentazione della componente, anche in relazione alla necessità di avere a disposizione la libreria proprietaria Oracle "weblogic-client-3.0.0.jar".
La piattaforma PSLP è integrata nei servizi del sistema informativo di Regione Piemonte "Lavoro": alcune sue funzionalità sono quindi strettamente legate alla possibilità di accedere a servizi esposti da altre componenti dell'ecosistema "Lavoro"
 

# Installazione

Creare lo schema del DB e popolarlo, tramite gli script della componente pslpdb. 
Configurare i datasource in pslweb e pslorch.
Per pslorch, nel caso si vogliano sfruttare le funzionalità di invio mail e sms, occorre anche configurare un mail-server ed un sms-gateway.


# Deployment

Dopo aver seguito le indicazioni del paragrafo relativo all'installazione, si può procedere al build dei pacchetti ed al deploy su application server JBoss.


# Versioning
Per la gestione del codice sorgente viene utilizzato Git, ma non vi sono vincoli per l'utilizzo di altri strumenti analoghi.
Per il versionamento del software si usa la tecnica [Semantic Versioning](http://semver.org).


# Copyrights
© Copyright Regione Piemonte – 2021

© Copyright CSI-Piemonte – 2021

# License

SPDX-License-Identifier: EUPL-1.2-or-later .

Questo software è distribuito con licenza EUPL-1.2 . 
Consultare il file LICENSE.txt per i dettagli sulla licenza.


