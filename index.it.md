---
layout: default
---

# Open Data Facile

> Per *open data* si intendono dati che possono essere usati gratuitamente, riutilizzati e distribuiti da chiunque. 
Sono soggetti, per la maggior parte delle volte, unicamente al requisito di attribuzione e di condivisione con la stessa licenza con la quale sono stati rilasciati. <sup><a href='http://opendatahandbook.org/it/what-is-open-data/'>*</a></sup>

Vorresti pubblicare degli open data? Evviva! Sei un grande. Qui puoi trovare dei suggerimenti per farlo in maniera semplice ed efficace.


## Obiettivi

Perché pubblicare degli open data?

* **Condividere dati può rendere la tua organizzazione più efficiente.** Quando fai attenzione a come i dati vengono pubblicati, raccolti e gestiti è più facile indirizzare altre persone a delle risorse valide e allo stesso tempo rendi più facile l'utilizzo di queste risorse. 

* **Avere un pubblico più ampio significa avere più creatività e talento rivolto alla comprensione dei tuoi dati.** Gli usi più interessanti possono essere inaspettati, come studi che fanno uso di riferimenti incrociati o visualizzazioni di dati che possono concentrare l'attenzione del pubblico su particolari dettagli.

## Usa formati Open

Avere un pubblico più ampio significa cambiare le aspettative di come verranno utilizzati i tuoi dati. Se usi un sistema operativo, del software specifico, o hai licenze per software che altri non posseggono (e che spesso hanno costi proibitivi), che senso ha rendere i tuoi dati open se per aprirli c'è bisogno di software che costa migliaia di dollari?

Per fortuna ci sono dei formati open che sono largamente supportati da prodotti gratutiti e commerciali di diversi sistemi operativi.

### Testo

**Evita di pubblicare testo con Microsoft Word.** Ci sono molteplici versioni incompatibili di questo formato e non sono lette allo stesso modo da altri software non sviluppati da Microsoft.

**Pubblicare testo in PDF è OK.** Ma ricordati che alcuni dei benefici dei PDF sono dei falsi miti: è molto facile modificare i PDF quindi questi file possono essere manomessi proprio come gli altri formati.

Se il tuo testo non ha degli stili particolari, usa un formato più semplice come il **.txt**: il formato più semplice in assoluto, facile da leggere in qualsiasi sistema.

### Tabelle

**Non pubblicare mai tabelle in PDF.** Estrarre dati da tabelle in PDF è quasi impossibile, quindi coloro che voglio usare questi dati devono fare moltissimo lavoro per estrarli o digitarli manualmente.

**Il formato più efficace per pubblicare dati tabulari è il [CSV](https://it.wikipedia.org/wiki/Comma-separated_values)**. CSV sta per 'Comma-separated values' (valori separati da virgola) ed è un'opzione per esportare dati presente in Microsoft Excel.

### Informazioni Geografiche

I formati per i dati geospaziali sono o in formato vettore o *raster*, e vengono scelti a seconda della dimensione dei dati.

**Per dati di piccole dimensioni, usa [GeoJSON](http://geojson.org/) or [KML](http://developers.google.com/kml/documentation/)**. 
Sono formati standard semplici e largamente adottati. Ricorda che questi formati richiedono che le coordinate geografiche siano espresse nel Datum [WGS84](http://en.wikipedia.org/wiki/World_Geodetic_System) che è un sistema di riferimento di facile uso per gli utilizzatori dei dati. È quindi necessario proiettare i dati in questo sistema prima di pubblicarli. Se hai dati ad alta precisione, che usano un altro sistema di riferimento, pubblica una versione nativa per l'alta precisione e, per facilità d'uso, pubblica anche una versione che usa il Datum WGS84.

**Per dati vettoriali di grandi dimensioni usa Shapefiles**. 

**Un buon formato per la distribuzione di dati in formato raster è [GeoTIFF](http://it.wikipedia.org/wiki/GeoTIFF).** È un open standard con molte implementazioni. Per datasets più grandi e array di dati non geografici usa  [NetCDF](https://en.wikipedia.org/wiki/NetCDF), un'altra buona scelta con un ampio supporto.

Alcuni tipi di dati Esri come FileGDB e `.zslas` sono intenzionalmente criptati e sono solo supportati da costosi sistemi Esri, quindi non sono raccomandati per la distribuzione di open data. Allo stesso modo, il formato GeoPDF non è raccomandato perché è raramente implementato e ha anche delle restrizioni legali.

## Usa Licenze Open

Specificare una licenza è essenziale per ogni tipo di distribuzione: senza chiari limiti legali, nessuno può essere sicuro di poter utilizzare i tuoi dati. Puoi scegliere una licenza in base a un certo numero di fattori:

Se i dati sono frutto di un [lavoro di un impiegato del governo federale degli Stati Uniti, quei dati sono di pubblico dominio](http://en.wikipedia.org/wiki/Work_of_the_United_States_Government) negli Stati Uniti, quindi non c'è alcuna scelta. Allo stesso modo [leggi americane e atri editti](http://en.wikipedia.org/wiki/Edict_of_government) non possono essere soggetti a copyright negli Stati Uniti.

Se i tuoi dati non rientrano in queste condizioni, probabilmente ne detieni il diritto d'autore, il che significa che sta a te scegliere quali diritti d'uso concedere. 

L'opzione più altruista a tua disposizione è di rilasciare i tuoi dati sotto licenza [CC0](https://creativecommons.org/publicdomain/zero/1.0/deed.it), una licenza che replica lo status di Pubblico Dominio. Con questa licenza rinunci alla maggior parte dei diritti come il diritto di richiedere un'attribuzione di autore o di impedire l'uso commerciale dei dati. Questo significa che gli utilizzatori non avranno alcun dubbio riguardo al loro utilizzo e che quindi siano più propensi ad utilizzarli. 

Se vuoi richiedere l'attribuzione dei tuoi dati, puoi usare la licenza [ODC-BY](http://opendatacommons.org/licenses/by/summary/) che permette alle persone di usare i tuoi dati fino a che l'origine dei dati venga ricondotta a te.

Un altro tipo di licenza è la "sharealike", ovvero rilasciare i dati con la stessa licenza con la quali sono stati ottenuti. Se da un lato questo permette che altre persone non si arricchiscano con il tuo lavoro, dall'altro rende molto difficile, o quasi impossibile, mischiare i tuoi dati con altri pubblicati con licenze non compatibili. Per quest'ultimo motivo non è raccomandabile usare licenze sharealike come [ODbL](http://opendatacommons.org/licenses/odbl/).

## Pubblicare

Una volta che hai creato i tuoi open data, è ora di pubblicarli!

È meglio iniziare in maniera semplice: non costruire un portale o non impostare un server quando quello di cui hai bisogno è solo di una semplice pagina con un pulsante per scaricare i tuoi dati. Se non hai molti dati, puoi provare a pubblicarli nel tuo CMS esistente (ad esempio Wordpress). 

L'elemento più importante di ogni strategia per la pubblicazione è l'indirizzo Web (URL): la regola più semplice è provare a rendere i tuoi dati accessibili utilizzando indirizzi affidabili, semplici da ricordare e che non cambiano nel tempo.

Per molte organizzazioni è importante che la pubblicazione di open data sia un processo affidabile e poco costoso. Pensare di trovare il budget per creare un portale per questi dati rende il tutto più difficile. Un modo per evitare questo problema è utilizzare servizi già esistenti come [Amazon S3](http://aws.amazon.com/s3/) per il download e l'archiviazione dei dati.

Hai bisogno di una API? Creane una se:

* Hai persone, tempo e fondi per mantenerla una volta che hai degli utenti.
* Hai più dati di quanto una persona ne voglia scaricare con un singolo download e c'è una distinzione chiara tra tipi di persone che necessitano un filtro.

Altrimenti pubblica i tuoi dati grezzi come singolo file per evitare complessità e la responsabilità necessaria per mantenere una API.

## Promozione

Hai finalmente pubblicato i tuoi dati – congratulazioni! Stai permettendo di pensare in nuovi, stimolanti modi. Fantastico! Ma come fai a far sì che altri si interessino ai tuoi dati e che inizino a usarli?

**Comunica con i tuoi utenti.** Pubblicare i tuoi dati è l'inizio di una conversazione con i tuoi utenti. Fornisci un indirizzo e-mail dove le persone possano mettersi in contatto, fare domande e condividere quello che stanno facendo con i tuoi dati. Una mailing list, un forum o un "issue tracker", può permettere ai tuoi utenti di collaborare e rispondersi a vicenda.

**Trova i tuoi pari e parlaci.** Adesso che i tuoi dati sono là fuori scoprirai che ci sono altre persone che stanno facendo cose simili alle tue – il paese vicino al tuo ha probabilmente lo stesso tipo di dati. Parla con altre persone, crea un collegamento e scopri come e cosa potete imparare l'uno dall'altro.

**Mostra perché i dati sono utili:** crea una semplice visualizzazione o un'analisi che utilizza i dati e inserisci un collegamento al tuo sito. Fanne menzione su social media e posti dove giornalisti e analisti di dati si ritrovano.






