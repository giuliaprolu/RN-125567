# Release Notes

## [1.0.18]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Fix fattura pagata									| **25-10-2022** | FIX  |      |


## [1.0.17]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Fix calcolo voce										| **21-10-2022** | FIX  |      |


## [1.0.16]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Fix fatture: #1825									| **15-10-2022** | FIX  |      |


## [1.0.15]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Fix anomalia											| **12-10-2022** | FIX  |      |

## [1.0.14]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Fix anomalia nullPointException in mancanza della voce| **11-10-2022** | FIX  |      |

## [1.0.13]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Rollback logica contatore fattura, risolta issue #1774	| **05-10-2022** | FIX  |      |


## [1.0.12]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Aggiornata libreria fibra-common con al gestione della voce	| **03-10-2022** | FIX  |      |


## [1.0.11]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| Modifica gestione errore 600							| **30-09-2022** | FIX  |      |

## [1.0.10]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| fix segnalazione 1759                                 | **26-09-2022** | FIX  |      |

## [1.0.9]
| Attivita'                                             | Data           | Tipo | Note |
|-------------------------------------------------------|----------------|------|------|
| fix 123513 - Fibra Fase 1B - non risalgono card fibra | **23-09-2022** | FIX  |      |

## [1.0.8]
| Attivita'                                                         | Data           | Tipo | Note |
|-------------------------------------------------------------------|----------------|------|------|
| Aggiornata libreria fibra-common | **19-09-2022** | FIX  |      |

## [1.0.7]
| Attivita'                                                         | Data           | Tipo | Note |
|-------------------------------------------------------------------|----------------|------|------|
| Aggiunta elenco campi dossierHeader, assetHeader | **19-09-2022** | FIX  |      |


## [1.0.6]

| Attivita'                                                         | Data           | Tipo | Note |
|-------------------------------------------------------------------|----------------|------|------|
| Aggiunta mappatura campi mancanti alla chiamata info-pagamento v2 | **12-09-2022** | FIX  |      |


## [1.0.5]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Implementato il meccanismo di recupero della fattura in base lla pushId, integrato con il microservizio fibra-app-batch | **29-08-2022** | CR |  |


***Nuove properties***

| Key                                    | Type   | Default   | Description                                                   |
|----------------------------------------|--------|-----------|---------------------------------------------------------------|
| envFrom.CACHE_METADATO_NOTIFICA_TTL_MM | string | `"1440"`  | TTL in minuti per cache risposte dal sistema fibra-app-batch  |



## [1.0.4]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Fibra Voce Fase 1 - Aggiornata versione libreria fibra-common per una segnalazione relativa alla lettura dello stato della SIM| **01-07-2022** | FIX |  |


## [1.0.3]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Fibra Voce Fase 1 - Aggiornata libreria common per leggere nuovi attributi| **28-06-2022** | FIX |  |

### Attivita' manuali

Nessuna

## [1.0.2]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Fibra Voce Fase 1 - modifiche dispositive per integrazione CRMU Interop| **14-06-2022** | FIX |  |

### Attivita' manuali

Nessuna


## [1.0.1]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Fibra Voce Fase 1 - modifiche logiche recupero opzione voce | **01-06-2022** | FIX |  |

### Attivita' manuali

Nessuna


## [1.0.0]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Fibra Voce Fase 1 - Introduzione chiamate CRMU Interop | **23-05-2022** | NEW |  |

### Attivita' manuali

Nessuna

### Elenco nuove configurazioni

**fibra-app-services-env-cm**

***Nuove properties***

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_MONITORING_EXCHANGE_ENABLE | string | `"true"` | Abilitazione logging di request e response delle chiamate del servizio retrieve asset esposto da CRMU (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_MONITORING_LATENCY_ENABLE | string | `"true"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio retrieve asset esposto da CRMU (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_MONITORING_LOG_BODY_ENABLE | string | `"true"` | Abilitazione logging del body delle chiamate del servizio retrieve asset esposto da CRMU (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio retrieve asset esposto da CRMU |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEASSET_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio retrieve asset esposto da CRMU |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_MONITORING_EXCHANGE_ENABLE | string | `"true"` | Abilitazione logging di request e response delle chiamate del servizio retrieve asset esposto da CRMU (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_MONITORING_LATENCY_ENABLE | string | `"true"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio retrieve asset esposto da CRMU (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_MONITORING_LOG_BODY_ENABLE | string | `"true"` | Abilitazione logging del body delle chiamate del servizio retrieve asset esposto da CRMU (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio retrieve asset esposto da CRMU |
| envFrom.REST_SERVICES_CRMUINTEROP_RETRIEVEDOSSIER_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio retrieve asset esposto da CRMU |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_INVOICES_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio ignite2restInvoices esposto da Billing Data Layer (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_INVOICES_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio ignite2restInvoices esposto da Billing Data Layer (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_INVOICES_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio ignite2restInvoices esposto da Billing Data Layer (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_INVOICES_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio ignite2restInvoices esposto da Billing Data Layer |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_INVOICES_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio ignite2restInvoices esposto da Billing Data Layer |
| envFrom.SETTINGS_CRMU_HEADER_PI_OFFICE_ID | string | `"_#PLACEHOLDER"` | Valorizzazione header 'PI-Office-Id' (collaudo: 55111 , certificazione: XXX , produzione: XXX ) |
| envFrom.SETTINGS_CRMU_HEADER_PI_USER_ID | string | `"_#PLACEHOLDER"` | Valorizzazione header 'PI-User-Id' (collaudo: TEST0011 , certificazione: XXX , produzione: XXX ) |


## [0.0.29]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Introduzione canale Contact Center su CRMU | **11-03-2022** | NEW |  |

### Attivita' manuali

Nessuna

### Elenco nuove configurazioni

**fibra-app-services-env-cm**

***Rimozione properties***

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_BASEURI | string | `"http://localhost:9998/postel/DownloadService"` | Base URI del servizio downloadDocumenti esposto da Postel (il servizio e' esposto su sidecar heimdallr) |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_MONITORING_EXCHANGE_ENABLE | string | `"true"` | Abilitazione logging di request e response delle chiamate del servizio downloadDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_MONITORING_LATENCY_ENABLE | string | `"true"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio downloadDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_MONITORING_LOG_BODY_ENABLE | string | `"true"` | Abilitazione logging del body delle chiamate del servizio downloadDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio downloadDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio downloadDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_RICERCA_BASEURI | string | `"http://localhost:9998/postel/RicercaDocumentiService"` | Base URI del servizio ricercaDocumenti esposto da Postel (il servizio e' esposto su sidecar heimdallr) |
| envFrom.REST_SERVICES_POSTEL_RICERCA_MONITORING_EXCHANGE_ENABLE | string | `"true"` | Abilitazione logging di request e response delle chiamate del servizio ricercaDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_RICERCA_MONITORING_LATENCY_ENABLE | string | `"true"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio ricercaDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_RICERCA_MONITORING_LOG_BODY_ENABLE | string | `"true"` | Abilitazione logging del body delle chiamate del servizio ricercaDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_RICERCA_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio ricercaDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_RICERCA_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio ricercaDocumenti esposto da Postel |
| envFrom.HTTP_WS_SERVICES_GECT_BASE_URI | string | `"_#PLACEHOLDER"` | Base URI del servizio upload document esposto da GECT (il servizio e' esposto esternamente a OCP. Per l'ambiente di collaudo la url dovrebbe essere https://servizibusinesswsdev.rete.poste:2470/Orchestratore/ContrattiFinanziari/NewDocUpload, per certificazione https://servizibusinesswsdev.rete.poste:3498/Orchestratore/ContrattiFinanziari/NewDocUpload, per produzione https://servizibusinessws.rete.poste:4888/Orchestratore/ContrattiFinanziari/NewDocUpload) |
| envFrom.HTTP_WS_SERVICES_GECT_CONNECTION_TIMEOUT | string | `"30000"` | Valore connection timeout applicato alle chiamate del servizio upload document esposto da GECT |
| envFrom.HTTP_WS_SERVICES_GECT_SOCKET_TIMEOUT | string | `"60000"` | Valore request timeout applicato alle chiamate del servizio upload esposto da GECT |

***Nuove properties***

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.SETTINGS_CRMU_CANALE_ACQUISTO_CC | string | `"ContactCenter"` | Canale acquisto Contact Center |
| envFrom.SETTINGS_CRMU_CANALE_ACQUISTO_UFFICIO_POSTALE | string | `"UP"` | Canale acquisto UP |
| envFrom.SETTINGS_CRMU_CANALE_ACQUISTO_WEB | string | `"WEB"` | Canale acquisto WEB |
| envFrom.WS_DEFAULT_MONITORING_BODY_BUFFER_ENABLED | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate SOAP (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_DEFAULT_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate SOAP (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_DEFAULT_MONITORING_LATENCY_ENABLED | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate SOAP (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_DEFAULT_POOL_MAX_CONNECTIONS | string | `"48"` | Numero massimo di connessioni del pool per le chiamate SOAP |
| envFrom.WS_DEFAULT_POOL_MAX_IDLE_TIME | string | `"2s"` | Tempo dopo il quale una connessione del pool viene considerata idle per le chiamate SOAP |
| envFrom.WS_DEFAULT_POOL_MAX_LIFE_TIME | string | `"20s"` | Tempo massimo di vita di una connessione per le chiamate SOAP |
| envFrom.WS_DEFAULT_POOL_TIMEOUT | string | `"2s"` | Timeout applicato di default per il recupero delle connessioni dal pool per le chiamate SOAP |
| envFrom.WS_DEFAULT_REQUEST_CONN_TIMEOUT | string | `"2s"` | Connection timeout applicato di default a tutte le invocazioni SOAP |
| envFrom.WS_DEFAULT_REQUEST_SO_TIMEOUT | string | `"5s"` | Request timeout applicato di default a tutte le invocazioni SOAP |
| envFrom.WS_DEFAULT_SSL_KEYSTORE_PATH | string | `""` | Uri dell'eventuale key store per le chiamate SOAP |
| envFrom.WS_DEFAULT_SSL_TRUSTSTORE_PATH | string | `"file:///usr/app/bin/configuration/certs/truststore.jks"` | Uri dell'eventuale trust store per le chiamate SOAP |
| envFrom.WS_DEFAULT_SSL_TRUSTSTORE_SKIP_HOSTNAME_VERIFICATION | string | `"true"` | Disabilitazione hostname verification per chiamate HTTPS di tipo SOAP |
| envFrom.WS_DEFAULT_SSL_TRUSTSTORE_TRUST_STRATEGY | string | `""` | Strategia di trust da applicare nel caso di chiamate HTTPS di tipo SOAP. Puo' valere TRUST_ALL, TRUST_SELF_SIGNED nel caso si vogliano saltare o effettuare verifiche parziali dei certificati; se lasciato vuoto, permette una verifica completa |
| envFrom.WS_SERVICES_GECT_NEWDOCUPLOAD_BASEURI | string | `"https://servizibusinesswsdev.rete.poste:2470/Orchestratore/ContrattiFinanziari/NewDocUpload"` | Base URI del servizio NewDocUpload esposto da GECT (collaudo: https://servizibusinesswsdev.rete.poste:2470/Orchestratore/ContrattiFinanziari/NewDocUpload, certificazione: https://servizibusinesswsdev.rete.poste:3498/Orchestratore/ContrattiFinanziari/NewDocUpload, produzione: https://servizibusinessws.rete.poste:4888/Orchestratore/ContrattiFinanziari/NewDocUpload) |
| envFrom.WS_SERVICES_GECT_NEWDOCUPLOAD_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio NewDocUpload esposto da GECT (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_SERVICES_GECT_NEWDOCUPLOAD_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio NewDocUpload esposto da GECT (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_SERVICES_GECT_NEWDOCUPLOAD_REQUEST_CONN_TIMEOUT | string | `"10s"` | Valore connection timeout applicato alle chiamate del servizio NewDocUpload esposto da GECT |
| envFrom.WS_SERVICES_GECT_NEWDOCUPLOAD_REQUEST_SO_TIMEOUT | string | `"30s"` | Valore request timeout applicato alle chiamate del servizio NewDocUpload esposto da GECT |
| envFrom.WS_SERVICES_POSTEL_DOWNLOAD_WS_BASEURI | string | `"https://ged.postel.it/ws-docufe-coll/DownloadService"` | Base URI del servizio download esposto da Postel (collaudo: https://ged.postel.it/ws-docufe-coll/DownloadService, produzione: https://servizidoc.postel.it/ws-docufe-fatture-prod/DownloadService) |
| envFrom.WS_SERVICES_POSTEL_DOWNLOAD_WS_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio download esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_SERVICES_POSTEL_DOWNLOAD_WS_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio download esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_SERVICES_POSTEL_DOWNLOAD_WS_REQUEST_CONN_TIMEOUT | string | `"10s"` | Valore connection timeout applicato alle chiamate del servizio download esposto da Postel |
| envFrom.WS_SERVICES_POSTEL_DOWNLOAD_WS_REQUEST_SO_TIMEOUT | string | `"30s"` | Valore request timeout applicato alle chiamate del servizio download esposto da Postel |
| envFrom.WS_SERVICES_POSTEL_RICERCA_WS_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio ricerca esposto da Postel (collaudo: https://ged.postel.it/ws-docufe-coll/RicercaDocumentiService, produzione: https://servizidoc.postel.it/ws-docufe-fatture-prod/RicercaDocumentiService) |
| envFrom.WS_SERVICES_POSTEL_RICERCA_WS_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio ricerca esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_SERVICES_POSTEL_RICERCA_WS_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio ricerca esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.WS_SERVICES_POSTEL_RICERCA_WS_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio ricerca esposto da Postel |
| envFrom.WS_SERVICES_POSTEL_RICERCA_WS_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio ricerca esposto da Postel |


**fibra-app-services-heimdallr-conf**

***Rimozione properties***

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| heimdallr.configuration.heimdallr.http.connectiontimeout | int | `30` | Valore globale connection timeout (es. 30) - Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |
| heimdallr.configuration.heimdallr.http.disablecompression | bool | `false` |  |
| heimdallr.configuration.heimdallr.http.disablekeepalive | bool | `false` |  |
| heimdallr.configuration.heimdallr.http.expectcontinuetimeout | int | `30` | Valore globale expect continue timeout (es. 30) - Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |
| heimdallr.configuration.heimdallr.http.idleconntimeouttimeout | int | `30` |  |
| heimdallr.configuration.heimdallr.http.maxconnperhost | int | `20` |  |
| heimdallr.configuration.heimdallr.http.maxidleconn | int | `20` |  |
| heimdallr.configuration.heimdallr.http.maxidleconnperhost | int | `20` |  |
| heimdallr.configuration.heimdallr.http.responseheadertimeout | int | `30` | Valore globale response header timeout (es. 30) - Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |
| heimdallr.configuration.heimdallr.http.tlshandshaketimeout | int | `30` | Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |
| heimdallr.configuration.heimdallr.services[0].name | string | `"POSTEL Ricerca Documenti Service"` |  |
| heimdallr.configuration.heimdallr.services[0].requestContentType | string | `"text/xml; charset=utf-8"` |  |
| heimdallr.configuration.heimdallr.services[0].requestTemplate | string | `"heimdallr/templates/postelRicercaDocumentiRequest.xml"` |  |
| heimdallr.configuration.heimdallr.services[0].requestTemplateIsXML | bool | `true` |  |
| heimdallr.configuration.heimdallr.services[0].responseTemplate | string | `"heimdallr/templates/postelRicercaDocumentiResponse.json"` |  |
| heimdallr.configuration.heimdallr.services[0].selector.actionregexp | string | `"*"` |  |
| heimdallr.configuration.heimdallr.services[0].selector.pathregexp | string | `"/postel/RicercaDocumentiService*"` |  |
| heimdallr.configuration.heimdallr.services[0].service | string | `nil` |  |
| heimdallr.configuration.heimdallr.services[0].soapserver.context | string | `"_#PLACEHOLDER"` | Context path per invocazione Postel Ricerca Documenti (per collaudo: /ws-docufe-coll/RicercaDocumentiService - per produzione: /ws-docufe-fatture-prod/RicercaDocumentiService) |
| heimdallr.configuration.heimdallr.services[0].soapserver.host | string | `"_#PLACEHOLDER"` | Host per invocazione Postel Ricerca Documenti (per collaudo: ged.postel.it - per produzione: servizidoc.postel.it) |
| heimdallr.configuration.heimdallr.services[0].soapserver.key | string | `""` |  |
| heimdallr.configuration.heimdallr.services[0].soapserver.pem | string | `""` |  |
| heimdallr.configuration.heimdallr.services[0].soapserver.port | int | `443` | Porta per invocazione Postel Ricerca Documenti |
| heimdallr.configuration.heimdallr.services[0].soapserver.protocol | string | `"https"` | Protocollo per invocazione Postel Ricerca Documenti |
| heimdallr.configuration.heimdallr.services[0].soapserver.timeout | string | `"30s"` | Timeout per invocazione Postel Ricerca Documenti |
| heimdallr.configuration.heimdallr.services[0].validation.responseSoapNamespace | string | `"S"` |  |
| heimdallr.configuration.heimdallr.services[1].name | string | `"POSTEL Download Documenti Service"` |  |
| heimdallr.configuration.heimdallr.services[1].requestContentType | string | `"text/xml; charset=utf-8"` |  |
| heimdallr.configuration.heimdallr.services[1].requestTemplate | string | `"heimdallr/templates/postelDownloadRequest.xml"` |  |
| heimdallr.configuration.heimdallr.services[1].requestTemplateIsXML | bool | `true` |  |
| heimdallr.configuration.heimdallr.services[1].responseTemplate | string | `"heimdallr/templates/postelDownloadResponse.json"` |  |
| heimdallr.configuration.heimdallr.services[1].selector.actionregexp | string | `"*"` |  |
| heimdallr.configuration.heimdallr.services[1].selector.pathregexp | string | `"/postel/DownloadService*"` |  |
| heimdallr.configuration.heimdallr.services[1].service | string | `nil` |  |
| heimdallr.configuration.heimdallr.services[1].soapserver.context | string | `"_#PLACEHOLDER"` | Context path per invocazione Postel Download Documenti (per collaudo: /ws-docufe-coll/DownloadService - per produzione: /ws-docufe-fatture-prod/DownloadService) |
| heimdallr.configuration.heimdallr.services[1].soapserver.host | string | `"_#PLACEHOLDER"` | Host per invocazione Postel Download Documenti (per collaudo: ged.postel.it - per produzione: servizidoc.postel.it) |
| heimdallr.configuration.heimdallr.services[1].soapserver.key | string | `""` |  |
| heimdallr.configuration.heimdallr.services[1].soapserver.pem | string | `""` |  |
| heimdallr.configuration.heimdallr.services[1].soapserver.port | int | `443` | Porta per invocazione Postel Download Documenti |
| heimdallr.configuration.heimdallr.services[1].soapserver.protocol | string | `"https"` | Protocollo per invocazione Postel Download Documenti |
| heimdallr.configuration.heimdallr.services[1].soapserver.timeout | string | `"30s"` | Timeout per invocazione Postel Download Documenti |
| heimdallr.configuration.heimdallr.services[1].validation.responseSoapNamespace | string | `"S"` |  |
| heimdallr.env.HEIMDALLR_DEBUG | bool | `true` | Abilitazione debug in Heimdallr (mettere a true in tutti gli ambienti tranne che in Produzione) |
| heimdallr.livenessProbe.initialDelaySeconds | int | `30` |  |
| heimdallr.readinessProbe.initialDelaySeconds | int | `30` |  |
| heimdallr.resources.limits.cpu | string | `"150m"` | Impostazione valore di limite della CPU per il sidecar Heimdallr |
| heimdallr.resources.limits.memory | string | `"128Mi"` | Impostazione valore di limite della memoria per il sidecar Heimdallr |
| heimdallr.resources.requests.cpu | string | `"20m"` | Impostazione valore di request della CPU per il sidecar Heimdallr |
| heimdallr.resources.requests.memory | string | `"128Mi"` | Impostazione valore di request della memoria per il sidecar Heimdallr |


## [0.0.28]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Rimozione codifica base64 per il pdf inviato a GECT | **19-01-2022** | FIX |  |


## [0.0.27]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica API "Modifica ricezione fattura" per mancato inserimento campo channel in input | **01-12-2021** | FIX |  |


## [0.0.26]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica API "visualizzazione fatture" per introduzione campo "contatoreFattureDaSaldare" | **29-11-2021** | FIX |  |

## [0.0.25]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica API "Modifica ricezione fattura" per introduzione campo "codCatastaleComune" | **25-11-2021** | FIX |  |
| Gestione recupero iban per vendita da canale UP | **25-11-2021** | NEW |  |

## [0.0.24]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica API "Modifica ricezione fattura" | **23-11-2021** | FIX |  |
| Modifica API "Modifica info contatto" | **23-11-2021** | FIX |  |


## [0.0.23]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica API "Modifica ricezione fattura" | **19-11-2021** | FIX |  |


## [0.0.22]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Nuova API "Recupero info pagamento fattura" | **10-11-2021** | NEW |  |

### Elenco nuove configurazioni

**fibra-app-services-env-cm**

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.SETTINGS_FATTURE_COMMISSIONI | string | `'_#PLACEHOLDER'` | Valore di default delle commissioni per pagamento con bollettino premarcato (es. 1.00) |


## [0.0.21]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica API "Modifica modalità di ricezione fattura" | **25-10-2021** | FIX |  |


## [0.0.20]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica API "Modifica domiciliazione e strumento di pagamento fattura" | **20-10-2021** | FIX |  |


## [0.0.19]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Nuova API "Recupero modulo SEPA" | **15-10-2021** | NEW |  |
| Modifica filtri dossier da OneView | **15-10-2021** | FIX |  |


## [0.0.18]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Nuova API "Modifica domiciliazione e strumento di pagamento fattura" | **12-10-2021** | NEW |  |
| Nuova API "Modifica modalità di ricezione fattura" | **12-10-2021** | NEW |  |
| Integrazione campi "metodoPagamentoFattura" e "modalitaRicezioneFattura nell'API "dettaglio contratti" | **12-10-2021** | EDIT | |
| Modifica recupero info asset | **12-10-2021** | FIX |  |

### Attivita' manuali

- Verificare che nel namespace "fibra" sia presente una Network Policy che permetta il traffico dal namespace "fibra-app" al namespace "fibra". Se non presente, fare richiesta al gruppo "Supporto DEVOPS Middleware" (mwdevops@posteitaliane.it).

### Elenco nuove configurazioni

**fibra-app-services-env-cm**

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.HTTP_WS_SERVICES_GECT_BASE_URI | string | `"_#PLACEHOLDER"` | Base URI del servizio upload document esposto da GECT (il servizio e' esposto esternamente a OCP. Per l'ambiente di collaudo la url dovrebbe essere https://servizibusinesswsdev.rete.poste:2470/Orchestratore/ContrattiFinanziari/NewDocUpload, per certificazione https://servizibusinesswsdev.rete.poste:3498/Orchestratore/ContrattiFinanziari/NewDocUpload, per produzione https://servizibusinessws.rete.poste:4888/Orchestratore/ContrattiFinanziari/NewDocUpload) |
| envFrom.HTTP_WS_SERVICES_GECT_CONNECTION_TIMEOUT | string | `"30000"` | Valore connection timeout applicato alle chiamate del servizio upload document esposto da GECT |
| envFrom.HTTP_WS_SERVICES_GECT_SOCKET_TIMEOUT | string | `"60000'"` | Valore request timeout applicato alle chiamate del servizio upload esposto da GECT |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_BILLINGMETHOD_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio billing method esposto da Anagraphic Management (il servizio e' esposto su OCP gpweb2 namespace fibra. La url del service dovrebbe essere http://anagraphic-management-ms-svc.fibra:8080/anagraphic-management/v1/customers/billingMethod per tutti gli ambienti) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_BILLINGMETHOD_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio billing method esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_BILLINGMETHOD_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio billing method esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_BILLINGMETHOD_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio billing method esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_BILLINGMETHOD_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio billing method esposto da Anagraphic Management |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_BILLINGMETHOD_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio billing method esposto da Anagraphic Management |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_PAYMENTMETHODS_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio payment methods esposto da Anagraphic Management (il servizio e' esposto su OCP gpweb2 namespace fibra. La url del service dovrebbe essere http://anagraphic-management-ms-svc.fibra:8080/anagraphic-management/v1/customers/payment-methods per tutti gli ambienti) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_PAYMENTMETHODS_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio payment methods esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_PAYMENTMETHODS_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio payment methods esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_PAYMENTMETHODS_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio payment methods esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_PAYMENTMETHODS_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio payment methods esposto da Anagraphic Management |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_PAYMENTMETHODS_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio payment methods esposto da Anagraphic Management |
| envFrom.REST_SERVICES_PAYMENTMANAGEMENT_VERIFYSEPA_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio verify sepa esposto da Payment Management (il servizio è esposto su OCP gpweb2 namespace fibra. La url del service dovrebbe essere http://payment-management-ms-svc.fibra:8080/payment-management/v1/verifySepa per tutti gli ambienti) |
| envFrom.REST_SERVICES_PAYMENTMANAGEMENT_VERIFYSEPA_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio verify sepa esposto da Payment Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_PAYMENTMANAGEMENT_VERIFYSEPA_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio verify sepa esposto da Payment Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_PAYMENTMANAGEMENT_VERIFYSEPA_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio verify sepa esposto da Payment Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_PAYMENTMANAGEMENT_VERIFYSEPA_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio verify sepa esposto da Payment Management |
| envFrom.REST_SERVICES_PAYMENTMANAGEMENT_VERIFYSEPA_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio verify sepa esposto da Payment Management |
| envFrom.SETTINGS_PAYMENTMANAGEMENT_MOCK_ENABLED | string | `"false"` | Abilitazione modalita' mock per il sistema Payment Management |

### Attivita' manuali

- Modificare la secret con nome "fibra-app-services-secrets" aggiungendo nella chiave "truststore.jks" il certificato per poter accedere al sistema GECT. Il comando da lanciare per la modifica della secret e' il seguente:
	```
	oc patch secret fibra-app-services-secrets -p '{"data": {"truststore.jks": " < TRUSTSTORE.JKS >" }}'
	```
	
	dove 
	
	< TRUSTSTORE.JKS >  e' la codifica in base64 del campo truststore.jks presente nella secret con nome "fibra-app-services-secrets" e contiene anche il certificato di GECT (nel caso di collaudo reperibile con il comando openssl s_client -connect servizibusinesswsdev.rete.poste:2470 2>/dev/null </dev/null |  sed -ne '/-BEGIN CERTIFICATE-/,/-END CERTIFICATE-/p').
    Per poter aggiungere il certificato di GECT all'attuale truststore.jks, e' necessario recuperare la string base64 presente nella secret con nome "fibra-app-services-secrets", decodificarla in base64 e memorizzarne il contenuto in un file per poi aggiungervi il certificato di GECT e procedere con una nuova codifica in base64 del truststore.jks cosi' ottenuto.
	
	Il comando richiede che sia presente un client oc (se installato su windows, si rende necessario l'uso di cygwin per il lancio del comando sopra).


## [0.0.17]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Revisione API "Modifica dati di contatto" | **01-10-2021** | FIX |  |
| Revisione API "Modifica DAC" | **01-10-2021** | FIX |  |

### Elenco modifiche configurazioni (presenti nella ConfigMap fibra-app-services-heimdallr-conf)
| Key | Type | Default | Description |
|-----|------|---------|-------------|
| heimdallr.configuration.heimdallr.http.connectiontimeout | int | `30` | Valore globale connection timeout (es. 30) - Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |
| heimdallr.configuration.heimdallr.http.expectcontinuetimeout | int | `30` | Valore globale expect continue timeout (es. 30) - Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |
| heimdallr.configuration.heimdallr.http.responseheadertimeout | int | `30` | Valore globale response header timeout (es. 30) - Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |
| heimdallr.configuration.heimdallr.http.tlshandshaketimeout | int | `30` | Negli ambienti non produttivi e' consigliabile lasciare questo valore a 30 |


## [0.0.16]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica ricerca/download fatture da Postel | **30-09-2021** | FIX |  |


## [0.0.15]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| API "Modifica dati di contatto" | **23-09-2021** | FIX |  |

### Elenco modifiche configurazioni
| Key | Type | Default | Description |
|-----|------|---------|-------------|
| heimdallr.env.HEIMDALLR_DEBUG | bool | `true` | Abilitazione debug in Heimdallr |


## [0.0.14]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Nuova API "Modifica dati di contatto" | **20-09-2021** | NEW |  |
| Nuova API "Modifica DAC" | **20-09-2021** | NEW |  |

### Attivita' manuali

- Verificare che nel namespace "fibra" sia presente una Network Policy che permetta il traffico dal namespace "fibra-app" al namespace "fibra". Se non presente, fare richiesta al gruppo "Supporto DEVOPS Middleware" (mwdevops@posteitaliane.it).

### Elenco nuove configurazioni

**fibra-app-services-env-cm**

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_CONTACT_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio contact esposto da Anagraphic Management (il servizio e' esposto su OCP gpweb2 namespace fibra. La url del service dovrebbe essere http://anagraphic-management-ms-svc.fibra.svc:8080/anagraphic-management/v1/customers/contact per tutti gli ambienti) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_CONTACT_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio contact esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_CONTACT_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio contact esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_CONTACT_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio contact esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_CONTACT_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio contact esposto da Anagraphic Management |
| envFrom.REST_SERVICES_ANAGRAPHICMANAGEMENT_CONTACT_REQUEST_SO_TIMEOUT | string | `"15s"` | Valore request timeout applicato alle chiamate del servizio contact esposto da Anagraphic Management |
| envFrom.REST_SERVICES_POSTVENDITA_DETAILDOSSIER_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio detailDossier esposto da Postvendita (il servizio e' esposto su OCP gpweb2 namespace fibra. La url del service dovrebbe essere http://fibra-post-vendita-ms-svc.fibra.svc.cluster.local:8080/fibra-post-vendita/v1/post-vendita/detailDossier per tutti gli ambienti) |
| envFrom.REST_SERVICES_POSTVENDITA_DETAILDOSSIER_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio detailDossier esposto da Postvendita (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_DETAILDOSSIER_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio detailDossier esposto da Postvendita (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_DETAILDOSSIER_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio detailDossier esposto da Postvendita (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_DETAILDOSSIER_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio detailDossier esposto da Postvendita |
| envFrom.REST_SERVICES_POSTVENDITA_DETAILDOSSIER_REQUEST_SO_TIMEOUT | string | `"15s"` | Valore request timeout applicato alle chiamate del servizio detailDossier esposto da Postvendita |
| envFrom.REST_SERVICES_POSTVENDITA_DOSSIERSBYCF_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio dossiersByCf esposto da Postvendita (il servizio e' esposto su OCP gpweb2 namespace fibra. La url del service dovrebbe essere http://fibra-post-vendita-ms-svc.fibra.svc.cluster.local:8080/fibra-post-vendita/v1/post-vendita/dossierByCF per tutti gli ambienti) |
| envFrom.REST_SERVICES_POSTVENDITA_DOSSIERSBYCF_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio dossiersByCf esposto da Postvendita (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_DOSSIERSBYCF_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio dossiersByCf esposto da Postvendita (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_DOSSIERSBYCF_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio dossiersByCf esposto da Postvendita (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_DOSSIERSBYCF_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio dossiersByCf esposto da Postvendita |
| envFrom.REST_SERVICES_POSTVENDITA_DOSSIERSBYCF_REQUEST_SO_TIMEOUT | string | `"15s"` | Valore request timeout applicato alle chiamate del servizio dossiersByCf esposto da Postvendita |
| envFrom.REST_SERVICES_POSTVENDITA_UPDATEACTION_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio updateAction esposto da Postvendita (il servizio e' esposto su OCP gpweb2 namespace fibra. La url del service dovrebbe essere http://fibra-post-vendita-ms-svc.fibra.svc.cluster.local:8080/fibra-post-vendita/v1/post-vendita/updateAction per tutti gli ambienti) |
| envFrom.REST_SERVICES_POSTVENDITA_UPDATEACTION_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio updateAction esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_UPDATEACTION_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio updateAction esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_UPDATEACTION_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio updateAction esposto da Anagraphic Management (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTVENDITA_UPDATEACTION_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio updateAction esposto da Anagraphic Management |
| envFrom.REST_SERVICES_POSTVENDITA_UPDATEACTION_REQUEST_SO_TIMEOUT | string | `"15s"` | Valore request timeout applicato alle chiamate del servizio updateAction esposto da Anagraphic Management |
| envFrom.SETTINGS_ANAGRAPHICMANAGEMENT_MOCK_ENABLED | string | `"false"` | Abilitazione modalita' mock per il sistema Anagraphic Management |
| envFrom.SETTINGS_POSTVENDITA_MOCK_ENABLED | string | `"false"` | Abilitazione modalita' mock per il sistema Postvendita |


## [0.0.13]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Restore versione heimdallr | **06-09-2021** | FIX |  |

## [0.0.12]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica ricerca/download fatture da Postel  | **06-09-2021** | FIX |  |

## [0.0.11]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica recupero metadati fatture da Billing Data Layer | **26-08-2021** | FIX |  |

## [0.0.10]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica logica di filtro dei dossier di tipo FIBRA dal sistema OneView | **21-07-2021** | NEW |  |
| Modifica parametro "requester" nello header della chiamata verso OneView | **21-07-2021** | FIX |  |
| Modifica API dettaglio contratti: aggiunto nuovo campo "providerContract" | **21-07-2021** | NEW |  |
| Nuova API "visualizzazione fatture" | **21-07-2021** | NEW |  |
| Nuova API "download fattura" | **21-07-2021** | NEW |  |

### Attivita' manuali

- Verificare che nel namespace "billing-data-layer" sia presente una Network Policy che permetta il traffico dal namespace "fibra-app" al namespace "billing-data-layer". Se non presente, fare richiesta al gruppo "Supporto DEVOPS Middleware" (mwdevops@posteitaliane.it).
- Modificare la secret con nome "fibra-app-services-secrets" aggiungendo le due nuove chiavi "postel.username" e "postel.password" usate per la Basic Authentication verso il sistema POSTEL. Il comando da lanciare per la modifica della secret e' il seguente:
	```
	oc patch secret fibra-app-services-secrets -p '{"data": {"postel.username": "'$(echo -n "< POSTEL_USERNAME >" | base64)'", "postel.password": "'$(echo -n "< POSTEL_PASSWORD >" | base64)'"}}'
	```
	
	dove 
	
	< POSTEL_USERNAME > e < POSTEL_PASSWORD > sono rispettivamente la username e la password usate per la Basic Authentication verso il sistema POSTEL. In ambiente di collaudo username e password sono uguali a "user_cicloattivo_fibra". Per l'ambiente di Produzione, fare richiesta di questi valori a Ottonelli Cinzia <cinzia.ottonelli@postel.it>.
	
	Il comando richiede che sia presente un client oc (se installato su windows, si rende necessario l'uso di cygwin per il lancio del comando sopra).

### Elenco nuove configurazioni

**fibra-app-services-env-cm**

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.REST_SERVICES_BLD_IGNITE2REST_BASEURI | string | `"_#PLACEHOLDER"` | Base URI del servizio ignite2rest esposto da Billing Data Layer (il servizio e' esposto su OCP gpweb2 namespace XXX. La url del service dovrebbe essere http://bdl-ignite2rest.billing-data-layer.svc/billing-data/api/v1/contracts/{providerContract}/documents per tutti gli ambienti) |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_MONITORING_EXCHANGE_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging di request e response delle chiamate del servizio ignite2rest esposto da Billing Data Layer (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_MONITORING_LATENCY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio ignite2rest esposto da Billing Data Layer (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_MONITORING_LOG_BODY_ENABLE | string | `"_#PLACEHOLDER"` | Abilitazione logging del body delle chiamate del servizio ignite2rest esposto da Billing Data Layer (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio ignite2rest esposto da Billing Data Layer |
| envFrom.REST_SERVICES_BLD_IGNITE2REST_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio ignite2rest esposto da Billing Data Layer |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_BASEURI | string | `"http://localhost:9998/postel/DownloadService"` | Base URI del servizio downloadDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_MONITORING_EXCHANGE_ENABLE | string | `"true"` | Abilitazione logging di request e response delle chiamate del servizio downloadDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_MONITORING_LATENCY_ENABLE | string | `"true"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio downloadDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_MONITORING_LOG_BODY_ENABLE | string | `"true"` | Abilitazione logging del body delle chiamate del servizio downloadDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio downloadDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_DOWNLOAD_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio downloadDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_RICERCA_BASEURI | string | `"http://localhost:9998/postel/RicercaDocumentiService"` | Base URI del servizio ricercaDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_RICERCA_MONITORING_EXCHANGE_ENABLE | string | `"true"` | Abilitazione logging di request e response delle chiamate del servizio ricercaDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_RICERCA_MONITORING_LATENCY_ENABLE | string | `"true"` | Abilitazione logging dei tempi di esecuzione delle chiamate del servizio ricercaDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_RICERCA_MONITORING_LOG_BODY_ENABLE | string | `"true"` | Abilitazione logging del body delle chiamate del servizio ricercaDocumenti esposto da Postel (in certificazione puo' essere impostato a true, in produzione a false) |
| envFrom.REST_SERVICES_POSTEL_RICERCA_REQUEST_CONN_TIMEOUT | string | `"2s"` | Valore connection timeout applicato alle chiamate del servizio ricercaDocumenti esposto da Postel |
| envFrom.REST_SERVICES_POSTEL_RICERCA_REQUEST_SO_TIMEOUT | string | `"5s"` | Valore request timeout applicato alle chiamate del servizio ricercaDocumenti esposto da Postel |
| envFrom.SETTINGS_BLD_MOCK_ENABLED | string | `"false"` | Abilitazione modalita' mock per il sistema Billing Data Layer (metadati fatture) |
| envFrom.SETTINGS_FATTURE_EXECUTOR_CORE_POOL_SIZE | string | `"16"` | Numero minimo di thread nel pool usati dall'API di download fattura |
| envFrom.SETTINGS_FATTURE_EXECUTOR_KEEP_ALIVE_TIME | string | `"60s"` | Tempo massimo di permanenza dei thread nel pool se idle usati dall'API di download fattura |
| envFrom.SETTINGS_FATTURE_EXECUTOR_MAX_POOL_SIZE | string | `"48"` | Numero massimo di thread nel pool usati dall'API di download fattura |
| envFrom.SETTINGS_FATTURE_EXECUTOR_MAX_QUEUE_SIZE | string | `"16"` | Size della queue utilizzata per i task usati dall'API di download fattura |
| envFrom.SETTINGS_POSTEL_DOWNLOAD_IDCLASSEDOC | string | `"_#PLACEHOLDER"` | Parametro "idClasseDoc" del sistema POSTEL (download fatture). Se presenti piu' classi documentali, separarle mediante virgola |
| envFrom.SETTINGS_POSTEL_IDCLIENTE | string | `"_#PLACEHOLDER"` | Parametro "idCliente" del sistema POSTEL (ricerca e download fatture) |
| envFrom.SETTINGS_POSTEL_MOCK_ENABLED | string | `"false"` | Abilitazione modalita' mock per il sistema POSTEL (ricerca e download fatture) |
| envFrom.SETTINGS_POSTEL_RICERCA_IDCLASSEDOCS | string | `"_#PLACEHOLDER"` | Parametro "idClasseDoc" del sistema POSTEL (ricerca fatture). Se presenti piu' classi documentali, separarle mediante virgola |
| envFrom.SETTINGS_POSTEL_SISTEMACHIAMANTE | string | `"_#PLACEHOLDER"` | Parametro "sistemaChiamante" del sistema POSTEL (ricerca e download fatture) |

**fibra-app-services-heimdallr-conf**

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| heimdallr.configuration.heimdallr.http.connectiontimeout | int | `10` | Valore globale connection timeout (es. 10) |
| heimdallr.configuration.heimdallr.http.disablecompression | bool | `false` |  |
| heimdallr.configuration.heimdallr.http.disablekeepalive | bool | `false` |  |
| heimdallr.configuration.heimdallr.http.expectcontinuetimeout | int | `10` | Valore globale expect continue timeout (es. 10) |
| heimdallr.configuration.heimdallr.http.idleconntimeouttimeout | int | `10` |  |
| heimdallr.configuration.heimdallr.http.maxconnperhost | int | `20` |  |
| heimdallr.configuration.heimdallr.http.maxidleconn | int | `20` |  |
| heimdallr.configuration.heimdallr.http.maxidleconnperhost | int | `20` |  |
| heimdallr.configuration.heimdallr.http.responseheadertimeout | int | `10` | Valore globale response header timeout (es. 10) |
| heimdallr.configuration.heimdallr.http.tlshandshaketimeout | int | `10` |  |
| heimdallr.configuration.heimdallr.services[0].name | string | `"POSTEL Ricerca Documenti Service"` |  |
| heimdallr.configuration.heimdallr.services[0].requestContentType | string | `"text/xml; charset=utf-8"` |  |
| heimdallr.configuration.heimdallr.services[0].requestTemplate | string | `"heimdallr/templates/postelRicercaDocumentiRequest.xml"` |  |
| heimdallr.configuration.heimdallr.services[0].requestTemplateIsXML | bool | `true` |  |
| heimdallr.configuration.heimdallr.services[0].responseTemplate | string | `"heimdallr/templates/postelRicercaDocumentiResponse.json"` |  |
| heimdallr.configuration.heimdallr.services[0].selector.actionregexp | string | `"*"` |  |
| heimdallr.configuration.heimdallr.services[0].selector.pathregexp | string | `"/postel/RicercaDocumentiService*"` |  |
| heimdallr.configuration.heimdallr.services[0].service | string | `nil` |  |
| heimdallr.configuration.heimdallr.services[0].soapserver.context | string | `"_#PLACEHOLDER"` | Context path per invocazione Postel Ricerca Documenti (per collaudo: /ws-docufe-coll/RicercaDocumentiService - per produzione: /ws-docufe-fatture-prod/RicercaDocumentiService) |
| heimdallr.configuration.heimdallr.services[0].soapserver.host | string | `"_#PLACEHOLDER"` | Host per invocazione Postel Ricerca Documenti (per collaudo: ged.postel.it - per produzione: servizidoc.postel.it) |
| heimdallr.configuration.heimdallr.services[0].soapserver.key | string | `""` |  |
| heimdallr.configuration.heimdallr.services[0].soapserver.pem | string | `""` |  |
| heimdallr.configuration.heimdallr.services[0].soapserver.port | int | `443` | Porta per invocazione Postel Ricerca Documenti |
| heimdallr.configuration.heimdallr.services[0].soapserver.protocol | string | `"https"` | Protocollo per invocazione Postel Ricerca Documenti |
| heimdallr.configuration.heimdallr.services[0].soapserver.timeout | string | `"30s"` | Timeout per invocazione Postel Ricerca Documenti |
| heimdallr.configuration.heimdallr.services[0].validation.responseSoapNamespace | string | `"S"` |  |
| heimdallr.configuration.heimdallr.services[1].name | string | `"POSTEL Download Documenti Service"` |  |
| heimdallr.configuration.heimdallr.services[1].requestContentType | string | `"text/xml; charset=utf-8"` |  |
| heimdallr.configuration.heimdallr.services[1].requestTemplate | string | `"heimdallr/templates/postelDownloadRequest.xml"` |  |
| heimdallr.configuration.heimdallr.services[1].requestTemplateIsXML | bool | `true` |  |
| heimdallr.configuration.heimdallr.services[1].responseTemplate | string | `"heimdallr/templates/postelDownloadResponse.json"` |  |
| heimdallr.configuration.heimdallr.services[1].selector.actionregexp | string | `"*"` |  |
| heimdallr.configuration.heimdallr.services[1].selector.pathregexp | string | `"/postel/DownloadService*"` |  |
| heimdallr.configuration.heimdallr.services[1].service | string | `nil` |  |
| heimdallr.configuration.heimdallr.services[1].soapserver.context | string | `"_#PLACEHOLDER"` | Context path per invocazione Postel Download Documenti (per collaudo: /ws-docufe-coll/DownloadService - per produzione: /ws-docufe-fatture-prod/DownloadService) |
| heimdallr.configuration.heimdallr.services[1].soapserver.host | string | `"_#PLACEHOLDER"` | Host per invocazione Postel Download Documenti (per collaudo: ged.postel.it - per produzione: servizidoc.postel.it) |
| heimdallr.configuration.heimdallr.services[1].soapserver.key | string | `""` |  |
| heimdallr.configuration.heimdallr.services[1].soapserver.pem | string | `""` |  |
| heimdallr.configuration.heimdallr.services[1].soapserver.port | int | `443` | Porta per invocazione Postel Download Documenti |
| heimdallr.configuration.heimdallr.services[1].soapserver.protocol | string | `"https"` | Protocollo per invocazione Postel Download Documenti |
| heimdallr.configuration.heimdallr.services[1].soapserver.timeout | string | `"30s"` | Timeout per invocazione Postel Download Documenti |
| heimdallr.configuration.heimdallr.services[1].validation.responseSoapNamespace | string | `"S"` |  |
| heimdallr.env.HEIMDALLR_DEBUG | bool | `false` | Abilitazione debug in Heimdallr |
| heimdallr.livenessProbe.initialDelaySeconds | int | `30` |  |
| heimdallr.readinessProbe.initialDelaySeconds | int | `30` |  |
| heimdallr.resources.limits.cpu | string | `"150m"` | Impostazione valore di limite della CPU per il sidecar Heimdallr |
| heimdallr.resources.limits.memory | string | `"128Mi"` | Impostazione valore di limite della memoria per il sidecar Heimdallr |
| heimdallr.resources.requests.cpu | string | `"100m"` | Impostazione valore di request della CPU per il sidecar Heimdallr |
| heimdallr.resources.requests.memory | string | `"128Mi"` | Impostazione valore di request della memoria per il sidecar Heimdallr |


### Elenco modifica configurazioni

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| envFrom.REST_SERVICES_ONEVIEW_CUSTOMERASSETS_REQUESTER | string | `"posteit-retail"` | Valore requester da passare negli header http per richiesta di customerAssets su OneView |


## [0.0.9]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Correzione meccanismo di serializzazione/deserializzazione delle response del sistema CRMU asset retrieve | **19-05-2021** | FIX | |

### Attivita' manuali

Prima di effettuare il deploy del microservizio, accedere al terminale del pod redis e lanciare il comando ```redis-cli -a < PASSWORD >``` e successivamente il comando ```FLUSHALL```. < PASSWORD > e' la password impostata nella chiave **redis.password** della secret con nome **fibra-app-services-secrets** (Se la password contiene caratteri speciali, racchiuderla tra apici singoli). 
Aggiornare la property **global.repository** del file **values.yaml** con il nuovo valore **palmcreg01a.azurecr.io/**


## [0.0.8]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Rimossa indicazione ora e minuti nel campo data.contratti[].tracking[].data dell'API "dettaglio contratti" | **05-05-2021** | NEW | |


## [0.0.7]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Modifica logica di recupero informazioni contratto da CRMU asset retrieve nel caso di linea attiva | **04-05-2021** | NEW | |
| Modifica logica di recupero informazioni contratto in base al canale di acquisto (UP/WEB) | **04-05-2021** | NEW | |


## [0.0.6]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Upgrade versione libreria bff-common-starter-parent da 0.2.8 a 0.2.10 | **23-04-2021** | NEW | |
| Gestione campo "costoMensile" nell'API "dettaglio contratti". Se il costo non viene restituito da CRMU dossier retrieve e se la data di sottoscrizione e' antecedente al 17/05/2021, viene inserito un costo fisso di "19,90" | **23-04-2021** | NEW | |  


## [0.0.5]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| FIX API dettaglio contratti: il campo "appuntamentoTecnico" deve essere mostrato solo nei seguenti casi: statoLinea = NON_ATTIVA e dettaglioStatoLinea = IN_LAVORAZIONE/CONSEGNA_DISPOSITIVI | **16-04-2021** | FIX | | 


## [0.0.4]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| FIX API dettaglio contratti: aggiunto remapping campo "offerCost" di CRMU dossier retrieve | **13-04-2021** | FIX | | 


## [0.0.3]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Nuova API attivazione SIM | **09-04-2021** | NEW | | 


## [0.0.2]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Fix API dettaglio contratti | **06-04-2021** | FIX | | 


## [0.0.1]

| Attivita'| Data | Tipo | Note |
| -------- | ---- | ---- | ---- |
| Prima release | **06-04-2021** | NEW | | 
