Descrizione UX (WISP)
=====================

Il WISP (*Wizard Interattivo di Scelta del Prestatore di Servizi di
Pagamento*) è un’applicazione web che consente ad un utente la
navigazione degli strumenti di pagamento resi disponibili dai PSP
aderenti alla Piattaforma pagoPA.

Tutti gli strumenti di pagamento sono raggruppati in tre categorie:

-  Pagamento con carte: attraverso questa sezione è possibile effettuare
   un pagamento con una carta di credito/debito abilitata a pagamenti
   on-line.
-  Addebito conto corrente: all’interno di questa categorie sono
   raccolti strumenti di pagamento che permettono l’interazione con
   l’home-banking del proprio istituto bancario.
-  Altri Metodi: all’interno di questa categoria rientrano altri
   strumenti di pagamento elettronici che non rientrano nei due punti
   precedenti.

La navigazione del WISP può avvenire sia in modalità anonima (verrà
richiesta una mail dove inviare l’esito dell’operazione), oppure come
utente registrato utilizzando le proprie credenziali SPID (livello 2).

Per gli utenti registrati sarà possibile salvare lo strumento di
pagamento utilizzato per poterlo selezionare più velocemente durante i
prossimi pagamenti, garantendo in tal modo un’esperienza utente più
veloce.

Selezione della Lingua
----------------------

Il WISP supporta 5 lingue:

-  Italiano ( default)
-  Inglese
-  Francese
-  Sloveno
-  Tedesco

L’EC può selezionare la lingua di avvio del WISP aggiungendo il
*query-parameter* ``lang``. I valori ammessi sono:

-  ``it`` (it-IT): Italiano
-  ``en`` (en-US): Inglese
-  ``fr`` (fr-FR): Francese
-  ``sl`` (sl-SI): Sloveno
-  ``de`` (de-DE): Tedesco

Qualora il parametro non sia presente, oppure è errato, verrà proposta
la lingua di default.

Personalizzazione del logo
--------------------------

E’ possibile sostituire il logo pagoPA all’interno della landing-page
del WISP con un proprio logo (formato 220x220, png/jpg) inserendo il
query-parameter ``logo`` valorizzato con l’identificativo del logo
caricato all’interno del Portale delle Adesioni (sezione EC > Gestione
Logo).

Compatibilità Browser
---------------------

Lo sviluppo del WISP segue le `linee guida di design per i servizi
digitali della
PA <https://docs.italia.it/italia/designers-italia/design-linee-guida-docs/it/stabile/index.html>`__.

In particolare, viene assicurata la compatibilità con versioni dei
browser che abbiano una penetrazione media tra la popolazione di almeno
1 persona ogni 100 abitanti.

Ciò significa che con i dati disponibili ad oggi i browser supportati
sono:

-  Chrome
-  Safari
-  Firefox
-  Samsung Internet Browser
-  Edge
-  Opera

Nota: il browser Internet Explorer 11 (IE-11) non rientra tra la lista
dei browser supportati. Nel dettaglio, IE-11 non supporta gli standard
web moderni ed è un freno all’implementazione all’interno delle nostre
piattaforme di API web moderne e con misure di sicurezza più avanzate
rispetto a quanto disponibile nel 2013.
