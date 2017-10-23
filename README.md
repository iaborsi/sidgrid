# SID&GRID
SID&GRID è ora scaricabile gratuitamente.

Prima di procedere con il salvataggio del software, si prega di leggere le istruzioni e i dettagli della licenza di distribuzione riportate qui di seguito.

Gli archivi ZIP contenenti tutto il materiale sono disponibili a questa pagina.

A questa pagina è possibile scaricare la documentazione:

    il Manuale Utente di SID&GRID in formato PDF;
    un Tutorial;
    le FAQ (Domande Frequenti).



INDICE:

A. CONTENUTI E ORGANIZZAZIONE DELLA CARTELLA

B. ISTRUZIONI PER L'INSTALLAZIONE

C. INFO SU LIBRERIE ESTERNE PER GEOSERVER

D. NOTE SULLA LICENZA

**************************************************************
A. CONTENUTI E ORGANIZZAZIONE DELLE CARTELLE

Le cartelle contengono tutti i file eseguibili e sorgenti sviluppati durante
il progetto SID&GRID. In particolare, sono presenti le cartelle e sotto-cartelle di seguito descritte:

-------
1. bin.zip (cartella dei file eseguibili e plug in)

1.1 modflow_sidgrid_version
In essa, suddivisa per cartelle dipendente dal sistema operativo (Windows/Linux o Mac), il file eseguibile del codice numerico MODFLOW,
nella versione modificata per il progetto SID&GRID

1.2 it.sidgrid.extension
Le estensioni di gvSIG per SID&GRID

1.3 it.sidgrid.scripting
Le estensioni di scripting per gvSIG (queste estensioni, essendo scritte in linguaggio nativo Jython
corrispondono anche ai file sorgente, e pertnato non vengono i file non vengono ripetuti nella cartella src)

1.4 sidgrid_SEXTANTE_module
Le estensioni della libreria Sextante

1.5 zonebudget_unix_modify
Il file eseguibile del programma Zone_budget, compilato per Unix/Mac in modo da essere eseguito senza
inconvenienti su questi sistemi operativi. La versione Windows puo' essere scaricata direttamente da:

http://water.usgs.gov/nrp/gwsoftware/zonebud3/zonebudget3.html



------
2. src.zip (cartella sorgenti)

2.1 modflow_sidgrid_version
I file FORTRAN comprensivi delle nuove subroutine sviluppate per SID&GRID. Sono presenti anche delle sotto-cartelle
contenenti i makefile per coloro che volessero ricompilare i sorgenti; i make file, suddivisi in Windows/Linux e Mac, sono
scritte presupponendi l'utilizzo del compilatore gfortran/gcc )

2.2 sidgrid_gvSIG_plugin
I sorgenti Java delle estensioni per gvSIG

2.3 sidgrid_SEXTANTE_module
I sorgenti Java per le estensioni della libreria Sextante

2.4 zonebudget_unix_modify
I sorgenti FORTRAN del programma ZoneBudget (USGS) modificato per essere compilato sotto Linux o Mac

**************************************************************
B. ISTRUZIONI PER L'INSTALLAZIONE
Riportiamo qui di seguito un estratto del Manuale SID&GRID relativo all'installazione di quanti presente nella cartella
SI CONSIGLIA DI LEGGERE LE ISTRUZIONI COMPLETE SUL MANUALE D'USO PRIMA DI PROCEDERE OLTRE


B.1 PREMESSA


SID&GRID è un framework su piattaforma GIS per la modellazione delle acque superficiali e sotterranee.
Si compone di diverse librerie e software di cui i seguenti sono stati sviluppati e/o modificati dal progetto SID&GRID:
Plugin SID&GRID per gvSIG desktop 1.x;
Libreria di scripting per gvSIG desktop 1.x;
Nuovo gruppo di geoalgoritmi sviluppati nel framework SEXTANTE integrato in gvSIG;
Modifiche ed integrazioni al codice numerico MODFLOW di USGS


B.2 Installazione del modulo SID&GRID per gvSIG desktop

Dopo avere scaricato la versione di SID&GRID per il proprio sistema operativo si può procedere con l’installazione manuale delle librerie e degli eseguibili per il corretto funzionamento di SID&GRID.
La cartella “bin” scaricabile conterrà i seguenti pacchetti:
a) it.sidgrid.extension (cartella di estensione per gvSIG)
b) it.sidgrid.scripting (cartella di script per gvSIG)
c) sextante_sidgrid.jar (libreria di geoalgoritmi per Sextante GIS)
d) mflgr_sidgrid (eseguibile del solutore numerico del modello idrogeologico)
e) zonbud (eseguibile del software per il calcolo del bilancio idrico zonale)

Le prime due cartelle a) e b) andranno copiate nella directory di gvSIG ../gvSIG/extensiones all’interno dei binari di gvSIG.

Il terzo file c) andrà copiato nella directory dell’estensione di Sextante GIS ../extensiones/es.unex.sextante.


I file eseguibili d) ed e) potranno essere collocati in qualunque directory dl proprio PC. Si consiglia, a tal proposito, di creare una directory nella propria Home nominandola “sidgrid” dove collocare questi due eseguibili.


N.B. Specialmente in ambiente Windows è sconsigliabile usare la directory “Documents and Settings” poiché potrebbe creare malfunzionamenti nei link con il software. In ogni caso è sempre sconsigliato usare directory con spazi quando si lavora con SID&GRID o comunque in ambiente GIS e DB.

**************************************************************
C. INFO SU LIBRERIE ESTERNE PER GEOSERVER

Librerie esterne da installare qualora si voglia utilizzare GEOSERVER:

1. geoserver-manager-1.5     /    MIT Licence
2. jxl            /    Lesser GPL v2
3. slf4j-api-1.7.2    /    MIT license
4. visad        /     GPL v2

Le sorgenti possono essere trovate su:
1. geoserver-manager-1.5     /    http://maven.geo-solutions.it/it/geosolutions/geoserver-manager/1.5/
2. jxl            /    http://sourceforge.net/projects/jexcelapi/files/jexcelapi/
3. slf4j-api-1.7.2    /    http://www.slf4j.org/download.html
4. visad        /     http://www.ssec.wisc.edu/~billh/visad.html


----------------------
Se si vuole utilizzare il modulo geoserver con geoserver-manager-1.5
l'utente necessita delle seguenti librerie: apache-http-common (http://archive.apache.org/dist/httpcomponents/httpclient/)
e jdom (http://www.jdom.org/dist/binary/), da copiare nella directory "lib".


**************************************************************
D. NOTE SULLA LICENZA

Tutti i codici sviluppati in ambiente Java e Jython per gvSIG sono rilasciati con licenza GPL: ogni cartella contenente
codice distribuito con questa modalita' contiene il file descrittivo della licenza, gpl.tx
Si consiglia di prenderne visione qualora si voglia modificare e/o sviluppare il codice

Tutti i codici provenienti dall abnca dati USGG -U.S. Geological Survey sono distribuiti
con licenza public domain (Credit: U.S. Geological Survey, Department of the Interior/USGS)



DISCLAIMER

All'interno di questa distribuzione è presente una versione modificata del codice MODFLOW, quale prodotto del gruppo di lavoro del progetto SID&GRID; esso non ha avuto nessun tipo di revisione/approvazione ufficiale da parte della U.S. Geological Survey Department of the Interior (USGS), che è invece l'autore della versione ufficiale di MODFLOW. Quest'ultima è documentata e disponibile all'indirizzo:

http://water.usgs.gov/nrp/gwsoftware/modflow.html


