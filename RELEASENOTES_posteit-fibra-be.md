# Release Notes

Attività da eseguire ad ogni rilascio, per il quale vengono indicate:
* Configurazioni da modificare sugli ambienti target (collaudo, cert, prod)
* Breve descrizione del contenuto del rilascio

Ogni modifica alle chiavi, o configurazioni, o aggiunta di nuove, necessita un redeploy dell'applicazione/scale down-scale up del POD OCP.


## Versione 1.3.15
- Fix 

## Versione 1.3.14
- Creare il secret chiamato "fibra-be-truststore" copiando le key dal secret "posteit-fibra-be-truststore"
- Fix su pratiche mancanti su one-view
- Modificare il values.yaml nel seguente modo:

Prima: 

```
env:
  TZ: "Europe/Rome"
  REST_DEFAULT_SSL_TRUSTSTORE_PASS:
    valueFrom:
       secretKeyRef:
         name: posteit-fibra-be-truststore
         key: 'password'
```

Dopo:

```
env:
  TZ: "Europe/Rome"
  REST_DEFAULT_SSL_TRUSTSTORE_PASS:
    valueFrom:
       secretKeyRef:
         name: fibra-be-truststore
         key: 'password'
```



## Versione 1.3.13
- Fix

## Versione 1.3.12
- Fix logica delle linee cessate

## Versione 1.3.11
- Modificata la logica di fattura pagata
- Fix issue di SILK: #1825, #3966, #3952, #3970, #1857, #1858, #3870, #1862, #1863


## Versione 1.3.10
- Fix issue di SILK: #3934

## Versione 1.3.9
- Fix issue di SILK: #1837, #3802

## Versione 1.3.8
- Fix sulla fibra voce. Corretta la logica nella libreria fibra-common.

## Versione 1.3.7
- Fix delle seguenti segnalazioni di SILK: #1793, #1804, #1766

## Versione 1.3.6
- Fix delle seguenti segnalazioni di SILK: #1793


## Versione 1.3.5
- Fix delle seguenti segnalazioni di SILK: #1757

## Versione 1.3.4
- Fix delle seguenti segnalazioni di SILK: #1683


## Versione 1.3.3
- In collaudo aumentare il timeout delle chiamate a 20s
- Fix delle seguenti segnalazioni di SILK: #1711, #1679, #1683, #1727, #1711, #3252


## Versione 1.3.2
- Fix nuovo stato di one-view "Attivazione_Voce"

## Versione 1.3.0
- Fibra + voce
- Gestione dell'errore 600
- La tipologia di offerta è acquisita da one-view e non da DossierHeader

## Versione 1.2.8


## Versione 1.2.7
- Fix sullo stato SIM della libreria common

## Versione 1.2.6
- Aggiornamento per poter gestire i nuovi attributi inseriti dal CRMU

## Versione 1.2.5
- Fix stato pratica

## Versione 1.2.3
- Fix lista fatture

## Versione 1.2.1
- Fix campo che identifica il tipo di offerta su CRMU

## Versione 1.2.0

- Modificare il file values.yaml nel seguente modo:

| **Property**								| **Value**      															| **Type**    |								
| ------------------------------------------|---------------------------------------------------------------------------|-------------| 
| **FIBRA_ANAGRAFICA_MOCK**					| 					| DELETE		  |
| **FIBRA_OFFERTA_MOCK**					| 					| DELETE		  |
| **FIBRA_FATTURE_MOCK**					| 					| DELETE		  |
| **FIBRA_OTP_MOCK**						| 					| DELETE		  |
| **FIBRA_TIPOLOGICHE_MOCK**				| 					| DELETE		  |
| **REST_SERVICES_BLD_IGNITE2REST_BASEURI**	| 	http://bdl-ignite2rest.billing-data-layer.svc/billing-data/api/v1/contracts/{providerContract}/documents		| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_REQUEST_CONN_TIMEOUT**	| 15s					| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_REQUEST_SO_TIMEOUT**		| 15s					| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_MONITORING_EXCHANGE_ENABLE**	| true				| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_MONITORING_LATENCY_ENABLE**	| true				| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_MONITORING_LOG_BODY_ENABLE**	| true				| NEW		  |
| **BRIM_SOAP_URL**				| 					| DELETE		  |
| **BRIM_SOAP_USERNAME**		| 					| DELETE		  |
| **BRIM_SOAP_PASSWORD**		| 					| DELETE		  |
| **REDIS_ENABLED**				| 					| DELETE		  |
| **MOTOREPAGAMENTI**			| 					| NEW/EDIT		  |
| **REST_SERVICES_BLD_IGNITE2REST_INVOICES_BASEURI**	| 	http://bdl-ignite2rest.billing-data-layer.svc/billing-data/billing-data/api/v2/contracts/{providerContract}/invoices	| NEW  |
| **REST_SERVICES_BLD_IGNITE2REST_INVOICES_REQUEST_CONN_TIMEOUT**		| 15s					| NEW	  |
| **REST_SERVICES_BLD_IGNITE2REST_INVOICES_REQUEST_SO_TIMEOUT**			| 15s					| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_INVOICES_MONITORING_EXCHANGE_ENABLE**	| true				| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_INVOICES_MONITORING_LATENCY_ENABLE**	| true				| NEW		  |
| **REST_SERVICES_BLD_IGNITE2REST_INVOICES_MONITORING_LOG_BODY_ENABLE**	| true				| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_BASEURI**					| http://crmu-interop-ms-svc.crmu.svc:8080/interop/crmu/v1/dossiers/header				| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_REQUEST_CONN_TIMEOUT**		| 15s		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_REQUEST_SO_TIMEOUT**			| 15s		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_MONITORING_EXCHANGE_ENABLE**	| true		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_MONITORING_LATENCY_ENABLE**	| true		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_MONITORING_LOG_BODY_ENABLE**	| true		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_BASEURI**						| http://crmu-interop-ms-svc.crmu.svc:8080/interop/crmu/v1/assets/header		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_REQUEST_CONN_TIMEOUT**			| 15s		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_REQUEST_SO_TIMEOUT**			| 15s		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_MONITORING_EXCHANGE_ENABLE**	| true		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_MONITORING_LATENCY_ENABLE**		| true		| NEW		  |
| **REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_MONITORING_LOG_BODY_ENABLE**	| true		| NEW		  |
| **SETTINGS_CRMU_HEADER_PI_OFFICE_ID**	| 55111				| NEW/EDIT		  |
| **SETTINGS_CRMU_HEADER_PI_USER_ID**	| TEST0011			| NEW/EDIT		  |
| **SETTINGS_CRMU_CANALE_ACQUISTO_WEB**	| WEB				| NEW/EDIT		  |
| **SETTINGS_CRMU_CANALE_ACQUISTO_CC**	| ContactCenter		| NEW/EDIT		  |
| **SETTINGS_CRMU_CANALE_ACQUISTO_UFFICIO_POSTALE**	| UP	| NEW/EDIT		  |
| **livenessProbe -> initialDelaySeconds** | 80 | EDIT |
| **readinessProbe -> initialDelaySeconds** | 100 | EDIT |
| **resources -> requests -> cpu** | 200m | EDIT |
| **resources -> limits -> cpu** | 500m | EDIT |
| **SETTINGS_PAYMENT_METHODS_DOMICILIAZIONEBANCARIA** | sepa,domiciliazione bancaria | NEW |
| **SETTINGS_PAYMENT_METHODS_BOLLETTINOPOSTALE** | bollpost,bollettino postale | NEW |
| **SETTINGS_ONLINEBILLING** | 1,true | NEW |
| **livenessProbe -> httpGet -> path** | /actuator/health | EDIT
| **readinessProbe -> httpGet -> path** | /actuator/health | EDIT

- Installare le seguenti network policy sui namespace:
 
| **Namespace** | **Network policy** |
| billing-data-layer | [allow-from-fibra-posteit-namespace](doc/networkPolicy/billingdatalayer/allow-from-fibra-posteit-namespace.yaml)
| crmu | [allow-from-fibra-posteit-namespace](doc/networkPolicy/crmu/allow-from-fibra-posteit-namespace.yaml)


## Versione 1.1.1
- Fix sul controller delle configurazioni.
- Modificata la configMap "rottedasretail" nel seguente blocco (Dalla versione 1.2.2 non occorre modificare il rottedasretail):

Da:

```
fibra_posteit_ms:
  Path("/fibra-poste-be/**")
  -> feuTracing()
  -> modPath("^/fibra-poste-be", "/")
  -> "http://posteit-fibra-be.posteit-fibra.svc.cluster.local:80"; 
```

A:

```
fibra_posteit_ms:
  Path("/fibra-poste-be/**")
  -> feuTracing()
  -> modPath("^/fibra-poste-be", "")
  -> "http://posteit-fibra-be.posteit-fibra.svc.cluster.local:80";
```

- Modificati i nomi delle immagini docker nel deployment.yaml del routerdasretail:

```
...
image: 'palmcreg01a.azurecr.io/incubation-hermodr:v1.5.3'
...
image: 'palmcreg01a.azurecr.io/jaegertracing/jaeger-agent:1.13'
...
image: 'palmcreg01a.azurecr.io/feurouter:1.3.7'

```


## Versione 1.1.0
- Aggiungere service account di OCP sulla cartella di Jenkins dove c'e' l'upstream di deploy.
- Eliminare routes posteit-fibra-be (previo backup dello .yaml)
- Eliminare il deployment posteit-fibra-be (previo backup dello .yaml)
- Eliminare il secret posteit-fibra-be-truststore (Eseguire backup secret, verrà ricreato durante il deploy del microservizio ma successivamente dovrà essere sostituito con il precedente truststore backuppato)
- Farsi esportare le pipeline di deploy su gli ambienti COLLAUDO/CERTIFICAZIONE/PRODUZIONE
- Copiare il values.yaml dei repo git di COLLAUDO/CERTIFICAZIONE/PRODUZIONE

## Versione 1.0.33
- Aggiornato valore costante inviata durante la modifica dell'indirizzo di spedizione della fattura. 

## Versione 1.0.32
- Aggiunto il campo "codice catastale" nella tabella comuni
- Eseguire gli script [7.Comuni.sql](doc/sql/7.Comuni.sql) e [9.Comuni_INSERT.sql](doc/sql/9.Comuni_INSERT.sql)

## Versione 1.0.31
- Modificate le stringhe di riferimento per il metodo getMetodoPagamento.
- Aggiunto il campo "channel" nelle richieste verso gateway-anagraphicmanagement.

## Versione 1.0.30
- Nel metodo getSpedizioneFattura si è modificato il nome del campo su cui leggere l'indirizzo di spedizione della fattura. Ora si legge da billingAddress


## Versione 1.0.29
- Nel kit contrattuale sono stati nascosti i documenti di asserzione
- Corretto il bug nel logoutt

### routerdasretail-hermodr-conf

```
 logout:
    callbackpath: /loggedout
    redirecturi: https://fibra.test.poste.it/loggedout
    handler: poste
    path: /logout
  ...

 provider:
    logoutpath: https://idp-poste.test.poste.it/jod-idp-retail/federation/openid-logout
```

### rottedasretail    

```
loggedout: Path("/loggedout")
  -> feuTracing()
  -> modPath("^/loggedout", "")
  -> stripQuery()
  -> redirectTo(302, "https://www.test.poste.it" )
  -> <shunt>;
```

### posteit-fibra-be configmap  

```
logout: https://fibra.test.poste.it/logout 
redirectUrl: #
```

### IDP Retail

Impostare la logout URI del client_name:fibraposteit-hermodr con il seguente valore su IDP retail

```
https://fibra.test.poste.it/loggedout
```

E' stato aggiornato il FE in modo che generasse la URL di logout prendendo solo il valore della variabile "logout" ricevuta come configurazione senza aggiungere redirectUrl come parametro.
FE ver. 1.0.32

## Versione 1.0.28
Allineamento tag

## Versione 1.0.27
- Fix sul numero delle fatture visualizzate
- Aggiunto nuovo stato Annullamento_Pratica->Completato
- Eseguire lo script [12.update_query.sql](/doc/sql/12.update_query.sql)

 
## Versione 1.0.26 
- Aggiunti 2 nuovi eventi BAM (Gestione_Fattura, Gestione_Contatti)
- Numero max di fatture visualizzabili e' 6
- Aggiunta cache per funzione getAppuntamento
- Aggiunti controlli sulla data della DAC



## Versione 1.0.25
fix sulla data attivazione inviata durante la procedura di modifica metodo pagamento

## Versione 1.0.24
Fix sulla visualizzazione delle date emissione e scadenza delle fatture


## Versione 1.0.23
Fix search e download fattura


## Versione 1.0.22
Da abilitare i mock delle fatture per fare il test in collaudo di download delle fatture. Questa versione deve essere rilasciata solo in COLL con il valore di mock a true. 
Sugli altri ambienti il valore di mock deve sempre essere a false. 

Sezione application.properties:

| **Property**								| **Value**      															| **Type**    |								
| ------------------------------------------|---------------------------------------------------------------------------|-------------| 
| **FIBRA_FATTURE_MOCK**					| true					| EDIT		  |


## Versione 1.0.21

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata


Sezione application.properties:

| **Property**								| **Value**      															| **Type**    |								
| ------------------------------------------|---------------------------------------------------------------------------|-------------| 
| **POSTEL_SOAP_SEARCH_IDCLASSEDOCSCARTO**	| ${POSTEL_SOAP_SEARCH_IDCLASSEDOCSCARTO:C4E1129A63C40A78E05335881EAC56E0}	| NEW		  |


## Versione 1.0.20

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**								| **Value**      															| **Type**    |								
| ------------------------------------------|---------------------------------------------------------------------------|-------------| 
| **POSTEL_SOAP_SEARCH_IDCLASSEDOC**		| ${POSTEL_SOAP_SEARCH_IDCLASSEDOC:BB89E50680D40CBCE05335881EAC5810}		| NEW/EDIT	  |
| **POSTEL_SOAP_SEARCH_SISTEMACHIAMANTE**	| ${POSTEL_SOAP_SEARCH_SISTEMACHIAMANTE:POSTEIT_FIBRA}						| NEW/EDIT 	  |
| **POSTEL_SOAP_DOWNLOAD_IDCLASSEDOC**		| ${POSTEL_SOAP_DOWNLOAD_IDCLASSEDOC:BB89E50680D40CBCE05335881EAC5810}		| NEW/EDIT 	  |
| **POSTEL_SOAP_DOWNLOAD_SISTEMACHIAMANTE**	| ${POSTEL_SOAP_DOWNLOAD_SISTEMACHIAMANTE:POSTEIT_FIBRA}					| NEW/EDIT 	  |





## Versione 1.0.18

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**					| **Value**      		| **Type**    |								
| ------------------------------|-----------------------|-------------| 
| **GECT_SOAP_URL**							| ${GECT_SOAP_URL:https://servizibusinesswsdev.rete.poste:2470/Orchestratore/ContrattiFinanziari/NewDocUpload}		| NEW		  |
| **GECT_SOAP_SSL_TRUST_STORE_PATH**		| ${REST_DEFAULT_SSL_TRUSTSTORE_PATH:}					| NEW 		  |
| **GECT_SOAP_SSL_TRUST_STORE_PASSWORD**	| ${REST_DEFAULT_SSL_TRUSTSTORE_PASS:}					| NEW 		  |
| **GECT_SOAP_SSL_TRUST_STORE_TYPE**		| ${GECT_SOAP_SSL_TRUST_STORE_TYPE:JKS}					| NEW 		  |


2. Aggiungere nel truststore il certificato SSL /doc/certificati/collaudo/servizibusinesswsdev.rete.poste.cer (CAInterna)


## Versione 1.0.8

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**					| **Value**      		| **Type**    |								
| ------------------------------|-----------------------|-------------| 
| **HTTP_REST_SERVICES_GATEWAY_PAYMENT_MANAGEMENT_MS_BASE_URI**	| ${REST_SERVICES_PAYMENT_MANAGEMENT_MS_BASEURI:https://payment-management-ms-route-fibra.app.svil.gpweb2.openshift.aztestposte/payment-management/v1/verifySepa}		| NEW/EDIT 		  |
| **HTTP_REST_SERVICES_GATEWAY_PAYMENT_MANAGEMENT_MS_REQUEST_CONNECTION_TIMEOUT**	| ${REST_SERVICES_PAYMENT_MANAGEMENT_MS_REQUEST_CONN_TIMEOUT:15s}		| NEW 		  |
| **HTTP_REST_SERVICES_GATEWAY_PAYMENT_MANAGEMENT_MS_REQUEST_SOCKET_TIMEOUT**	| ${REST_SERVICES_PAYMENT_MANAGEMENT_MS_SO_TIMEOUT:15s}		| NEW 		  |
| **HTTP_REST_SERVICES_GATEWAY_PAYMENT_MANAGEMENT_MS_MONITORING_ENABLE_EXCHANGE_LOGGING**	| ${REST_SERVICES_PAYMENT_MANAGEMENT_MS_MONITORING_EXCHANGE_ENABLE:true}		| NEW 		  |
| **HTTP_REST_SERVICES_GATEWAY_PAYMENT_MANAGEMENT_MS_MONITORING_ENABLE_LATENCY_LOGGING**	| ${REST_SERVICES_PAYMENT_MANAGEMENT_MS_MONITORING_LATENCY_ENABLE:true}		| NEW 		  |

## Versione 1.0.7

Fissato bug su metodo spedizione fatture.

## Versione 1.0.6

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**					| **Value**      		| **Type**    |								
| ------------------------------|-----------------------|-------------| 
| **HTTP_REST_SERVICES_GATEWAY_WEBACTIVATION_BASE_URI**	| ${REST_SERVICES_WEBACTIVATION_BASEURI:https://gateway-bss-mobile-ms-route-fibra.app.coll2.ocprm.testposte/gateway-bss-mobile/v1/gatewayBSSMobile/webActivation}		| NEW 		  |
| **HTTP_REST_SERVICES_GATEWAY_WEBACTIVATION_REQUEST_CONNECTION_TIMEOUT**	| ${REST_SERVICES_WEBACTIVATION_REQUEST_CONN_TIMEOUT:15s}		| NEW 		  |
| **HTTP_REST_SERVICES_GATEWAY_WEBACTIVATION_REQUEST_SOCKET_TIMEOUT**	| ${REST_SERVICES_WEBACTIVATION_SO_TIMEOUT:15s}		| NEW 		  |
| **HTTP_REST_SERVICES_GATEWAY_WEBACTIVATION_MONITORING_ENABLE_EXCHANGE_LOGGING**	| ${REST_SERVICES_WEBACTIVATION_MONITORING_EXCHANGE_ENABLE:true}	| NEW 		  |
| **HTTP_REST_SERVICES_GATEWAY_WEBACTIVATION_MONITORING_ENABLE_LATENCY_LOGGING**	| ${REST_SERVICES_WEBACTIVATION_MONITORING_LATENCY_ENABLE:true}	| NEW 		  |


2. Eseguire i seguenti script sql:

- /doc/sql/11.update_query.sql
- /doc/sql/grant.sql


 

## Versione 1.0.4

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**					| **Value**      		| **Type**    |								
| ------------------------------|-----------------------|-------------| 
| **OTP_DEBUG**					| ${OTP_DEBUG:true}		| NEW 		  |




## Versione 1.0.3

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**						| **Value**      															  													| **Type**    |								
| ----------------------------------| ------------------------------------------------------------------------------------------------------------------------------|-------------| 
| **HTTP_REST_SERVICES_GATEWAY_CONSENTMANAGEMENT_BASE_URI**	|	${REST_SERVICES_GATEWAY_CONSENTMANAGEMENT_BASEURI:https://consent-management-ms-route-fibra.app.svil2.ocprm.testposte/consent-management/v1/consent}	|	NEW |
| **HTTP_REST_SERVICES_GATEWAY_CONSENTMANAGEMENT_REQUEST_CONNECTION_TIMEOUT**	| ${REST_SERVICES_CONSENTMANAGEMENT_REQUEST_CONN_TIMEOUT:15s}				| NEW	|
| **HTTP_REST_SERVICES_GATEWAY_CONSENTMANAGEMENT_REQUEST_SOCKET_TIMEOUT** | ${REST_SERVICES_GATEWAY_CONSENTMANAGEMENT_SO_TIMEOUT:15s} 						| NEW 	|
| **HTTP_REST_SERVICES_GATEWAY_CONSENTMANAGEMENT_MONITORING_ENABLE_EXCHANGE_LOGGING** | ${REST_SERVICES_CONSENTMANAGEMENT_MONITORING_EXCHANGE_ENABLE:true}	| NEW 	|
| **HTTP_REST_SERVICES_GATEWAY_CONSENTMANAGEMENT_MONITORING_ENABLE_LATENCY_LOGGING**	| ${REST_SERVICES_CONSENTMANAGEMENT_MONITORING_LATENCY_ENABLE:true}	| NEW 	|




## Versione 1.0.2

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**						| **Value**      															  													| **Type**    |								
| ----------------------------------| ------------------------------------------------------------------------------------------------------------------------------|-------------| 
| **HTTP_REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_BASE_URI** | ${REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_BASEURI:https://anagraphic-management-ms-route-fibra.app.coll.gpweb2.openshift.aztestposte/anagraphic-management} | NEW 			| 
| **HTTP_REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_REQUEST_CONNECTION_TIMEOUT** 	| ${REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_REQUEST_CONN_TIMEOUT:15s}				| NEW 		   |
| **HTTP_REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_REQUEST_SOCKET_TIMEOUT**	| ${REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_SO_TIMEOUT:15s}								| NEW 		   |
| **HTTP_REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_MONITORING_ENABLE_EXCHANGE_LOGGING**	| ${REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_MONITORING_EXCHANGE_ENABLE:true}	| NEW 		   | 
| **HTTP_REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_MONITORING_ENABLE_LATENCY_LOGGING**	| ${REST_SERVICES_GATEWAY_ANAGRAPHICMANAGEMENT_MONITORING_LATENCY_ENABLE:true}		| NEW 		  |



## Versione 1.0.0

1. Accedere al file values.yaml e modificare le seguenti variabili

Legenda type: 
- **EDIT**: Property già presente dalla versione precedente e occorre solo modificare il suo value
- **NEW**: Property nuova, bisogna compiare il Value come è impostato nella tabella
- **NEW/EDIT**: Property nuova, ma il suo value dipendente dall'ambiente di installazione
- **DELETE**: Property deve essere cancellata

Sezione application.properties:

| **Property**						| **Value**      															  													| **Type**    |								
| ----------------------------------| ------------------------------------------------------------------------------------------------------------------------------|-------------| 
| **HTTP_REST_SERVICES_GATEWAY_POSTVENDITA_BASE_URI**							| ${REST_SERVICES_GATEWAY_POSTVENDITA_BASEURI:https://fibra-post-vendita-ms-route-fibra.app.svil2.ocprm.testposte/fibra-post-vendita}									| NEW 	    	|
| **HTTP_REST_SERVICES_GATEWAY_POSTVENDITA_REQUEST_CONNECTION_TIMEOUT**			| ${REST_SERVICES_GATEWAY_POSTVENDITA_REQUEST_CONN_TIMEOUT:15s}						| NEW			|	
| **HTTP_REST_SERVICES_GATEWAY_POSTVENDITA_REQUEST_SOCKET_TIMEOUT**				| ${REST_SERVICES_GATEWAY_BSS_POSTVENDITA_SO_TIMEOUT:15s}							| NEW			|	
| **HTTP_REST_SERVICES_GATEWAY_POSTVENDITA_MONITORING_ENABLE_EXCHANGE_LOGGING**	| ${REST_SERVICES_GATEWAY_POSTVENDITA_MONITORING_EXCHANGE_ENABLE:true}				| NEW			|	
| **HTTP_REST_SERVICES_GATEWAY_POSTVENDITA_MONITORING_ENABLE_LATENCY_LOGGING**	| ${REST_SERVICES_GATEWAY_POSTVENDITA_MONITORING_LATENCY_ENABLE:true}				| NEW			|	
| **FIBRA_OTP_MOCK**															| false																			  	| NEW			|	
| **HTTP_REST_SERVICES_OTP_SEND_BASE_URI**										| ${REST_SERVICES_OTPSEND_BASEURI:https://notification-service.app.svil2.ocprm.testposte/notification-service/v1/sms/dl/send}															| NEW			|	
| **HTTP_REST_SERVICES_OTP_SEND_REQUEST_CONNECTION_TIMEOUT**					| ${REST_SERVICES_OTPSEND_REQUEST_CONN_TIMEOUT:2s}									| NEW			|	
| **HTTP_REST_SERVICES_OTP_SEND_REQUEST_SOCKET_TIMEOUT**						| ${REST_SERVICES_OTPSEND_REQUEST_SO_TIMEOUT:5s}									| NEW			|	
| **HTTP_REST_SERVICES_OTP_SEND_MONITORING_ENABLE_EXCHANGE_LOGGING**			| ${REST_SERVICES_OTPSEND_MONITORING_EXCHANGE_ENABLE:true}							| NEW			|	
| **HTTP_REST_SERVICES_OTP_SEND_MONITORING_ENABLE_LATENCY_LOGGING**				| ${REST_SERVICES_OTPSEND_MONITORING_LATENCY_ENABLE:true}							| NEW			|	
| **HTTP_REST_SERVICES_OTP_VERIFY_BASE_URI**									| ${REST_SERVICES_OTPVERIFY_BASEURI:https://notification-service.app.svil2.ocprm.testposte/notification-service/v1/sms/dl/verify}																			| NEW			|	
| **HTTP_REST_SERVICES_OTP_VERIFY_REQUEST_CONNECTION_TIMEOUT**					| ${REST_SERVICES_OTPVERIFY_REQUEST_CONN_TIMEOUT:2s}								| NEW			|	
| **HTTP_REST_SERVICES_OTP_VERIFY_REQUEST_SOCKET_TIMEOUT**						| ${REST_SERVICES_OTPVERIFY_REQUEST_SO_TIMEOUT:5s}									| NEW			|	
| **HTTP_REST_SERVICES_OTP_VERIFY_MONITORING_ENABLE_EXCHANGE_LOGGING**			| ${REST_SERVICES_OTPVERIFY_MONITORING_EXCHANGE_ENABLE:true}						| NEW			|	
| **HTTP_REST_SERVICES_OTP_VERIFY_MONITORING_ENABLE_LATENCY_LOGGING**			| ${REST_SERVICES_OTPVERIFY_MONITORING_LATENCY_ENABLE:true}							| NEW			|	
| **RETAILSERVICE_URL**															|																				 	| DELETE		|
| **RETAILSERVICE_CONNECTION_TIMEOUT**											|																				 	| DELETE		|
| **RETAILSERVICE_READ_TIMEOUT**												|																				 	| DELETE		|
| **HTTP_HESSIAN_DEFAULTS_SSL_SKIP_HOSTNAME_VERIFICATION** 						| ${HESSIAN_DEFAULT_SSL_TRUSTSTORE_SKIP_HOSTNAME_VERIFICATION:true}					| NEW			|
| **HTTP_HESSIAN_DEFAULTS_SSL_TRUST_STORE_TRUST_STRATEGY** 						| ${HESSIAN_DEFAULT_SSL_TRUSTSTORE_TRUST_STRATEGY:}									| NEW			|
| **HTTP_HESSIAN_DEFAULTS_SSL_TRUST_STORE_URL** 								| ${HESSIAN_DEFAULT_SSL_TRUSTSTORE_PATH:}											| NEW			|
| **HTTP_HESSIAN_DEFAULTS_SSL_TRUST_STORE_PASSWORD** 							| ${HESSIAN_DEFAULT_SSL_TRUSTSTORE_PASS:}											| NEW			|
| **HTTP_HESSIAN_DEFAULTS_SSL_KEY_STORE_URL** 									| ${HESSIAN_DEFAULT_SSL_KEYSTORE_PATH:}												| NEW			|
| **HTTP_HESSIAN_DEFAULTS_SSL_KEY_STORE_PASSWORD** 								| ${HESSIAN_DEFAULT_SSL_KEYSTORE_PASS:}												| NEW			|
| **HTTP_HESSIAN_DEFAULTS_SSL_KEY_STORE_KEY_PASSWORD** 							| ${HESSIAN_DEFAULT_SSL_KEYSTORE_KEYPASS:}											| NEW			|
| **HTTP_HESSIAN_SERVICES_RETAIL_URL** 											| ${HESSIAN_SERVICES_RETAIL_BASEURI:XXX}											| NEW			|
| **HTTP_HESSIAN_SERVICES_RETAIL_REQUEST_TIMEOUT** 								| ${HESSIAN_SERVICES_RETAIL_REQUEST_TIMEOUT:10s}									| NEW			|
| **HTTP_HESSIAN_SERVICES_RETAIL_CONNECTION_TIMEOUT** 							| ${HESSIAN_SERVICES_RETAIL_CONNECTION_TIMEOUT:10s}									| NEW			|
| **HTTP_HESSIAN_SERVICES_RETAIL_MONITORING_ENABLE_LATENCY_LOGGING** 			| ${HESSIAN_SERVICES_RETAIL_MONITORING_LATENCY_ENABLED:true}						| NEW			|
| **HTTP_REST_SERVICES_GATEWAY_ONEVIEW_BASE_URI** 								| ${REST_SERVICES_GATEWAY_ONEVIEW_BASEURI:https://oneview-service-customerassets.app.coll2.ocprm.testposte/OneViewServices/customerAssets/v1}	| NEW			|
| **HTTP_REST_SERVICES_GATEWAY_ONEVIEW_REQUEST_CONNECTION_TIMEOUT** 			| ${REST_SERVICES_GATEWAY_ONEVIEW_REQUEST_CONN_TIMEOUT:15s}							| NEW			|
| **HTTP_REST_SERVICES_GATEWAY_ONEVIEW_REQUEST_SOCKET_TIMEOUT** 				| ${REST_SERVICES_GATEWAY_BSS_ONEVIEW_SO_TIMEOUT:15s}								| NEW			|
| **HTTP_REST_SERVICES_GATEWAY_ONEVIEW_MONITORING_ENABLE_EXCHANGE_LOGGING** 	| ${REST_SERVICES_GATEWAY_ONEVIEW_MONITORING_EXCHANGE_ENABLE:true}					| NEW			|
| **HTTP_REST_SERVICES_GATEWAY_ONEVIEW_MONITORING_ENABLE_LATENCY_LOGGING** 		| ${REST_SERVICES_GATEWAY_ONEVIEW_MONITORING_LATENCY_ENABLE:true}					| NEW			|
| **SPRING_KAFKA_CONSUMER_BOOTSTRAP_SERVERS** 									| 																					| DELETE		|
| **SPRING_KAFKA_CONSUMER_GROUP_ID**		 									| 																					| DELETE		|
| **SPRING_KAFKA_CONSUMER_AUTO_OFFSET_RESET** 									| 																					| DELETE		|
| **SPRING_KAFKA_CONSUMER_KEY_DESERIALIZER** 									| 																					| DELETE		|
| **SPRING_KAFKA_CONSUMER_VALUE_DESERIALIZER** 									| 																					| DELETE		|
| **SPRING_KAFKA_MAX_POLL_INTERVAL_MS** 										| 																					| DELETE		|

Sezione frontend.yaml:

| **Property**						| **Value**      										| **Type**    |								
| ----------------------------------| ------------------------------------------------------|-------------| 
| **ASSISTENZA**					| https://www.test.poste.it/home-assistenza.html		| EDIT		  |
| **LOGOUT**						| https://idp-poste.test.it/							| EDIT		  |
| **REDIRECTURL**					| https://www.test.poste.it/							| EDIT		  |
				

2. Eseguire gli script sql contenuti nella cartella /doc/sql dal numero 6. Dopo aver creato le tabelle eseguire sempre lo script grant.sql che corregge i grant sulle nuove tabelle.

