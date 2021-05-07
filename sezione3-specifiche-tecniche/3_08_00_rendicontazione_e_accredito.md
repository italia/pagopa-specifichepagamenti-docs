# Rendicontazione e Accredito

Per ogni pagamento avvenuto, il PSP si impegna a riversare le somme incassate verso gli IBAN contenuti nelle richieste di pagamento tramite disposizione di SCT cumulativi di tutti i pagamenti verso il medesimo conto corrente della PA.
Inoltre, a fronte di un pagamento avvenuto in data D, il PSP in data D+2 deve inviare un Flusso di Riconciliazione (FdR).

Il Flusso di Riconciliazione rappresenta il dettaglio dei pagamenti contenuti all'interno del medesimo SCT identificato (per mezzo del campo AT-05) con l'identificativo del flusso di riconciliazione.

Nel dettaglio, ogni FdR collezione i singoli versamenti identificati come illustrato nel seguito.

## Pagamento tramite PSP

Nel caso di un pagamento effettuato direttamente tramite i servizi del PSP (si veda Sez-III "Pagamento di un Avviso"), a fronte di un addebito eseguito dal PSP, descritto dalla primitiva `sendPaymentOutcome`, nel corrispondente Flusso di Rendicontazione il campo `datiSingoloPagamento` viene così composto:

* `identificativoUnivocoVersamento`: IUV della richiesta di pagamento, il medesimo restituito all’interno della primitiva getPayment da parte dell’EC e contenuto all’interno della ricevuta acquisita dall’Ente Beneficiario.
* `identificativoUnivocoRiscossione`: pari al paymentToken generato dalla piattaforma e riportato all’interno della ricevuta acquisita dall’Ente Beneficiario.
* `indiceDatiSingoloPagamento`: identificativo della porzione dell’importo indicato all’interno della ricevuta
* `singoloImportoPagato`: importo parziale
* `codiceEsitoSingoloPagamento`: 0
* `dataEsitoSingoloPagamento`: data del pagamento riportata all’interno della ricevuta

Pertanto, qualsiasi Ente Beneficiario è in grado di riconciliare il pagamento ricercando per ogni _datoSingoloPagamento_ la corrispondente ricevuta identificata da _paymentToken_ e _IUV_, selezionando l’importo parziale corrispondente al campo _indiceDatiSingoloPagamento_.

## Pagamento in Wallet

Nel caso di un pagamento effettuato tramite i servizi di pagamento resi disponibili all'interno del wallet (WISP), a fronte di un addebito eseguito dal PSP, il corrispondente Flusso di Rendicontazione conterrà il campo `datiSingoloPagamento` così composto:

* `identificativoUnivocoVersamento`: IUV della richiesta di pagamento, il medesimo contenuto all'interno della RPT ricevuta
* `identificativoUnivocoRiscossione`: il medesimo contenuto all'interno della RT emessa dal PSP
* `singoloImportoPagato`: importo parziale
* `codiceEsitoSingoloPagamento`: 0
* `dataEsitoSingoloPagamento`: data del pagamento riportata all’interno della ricevuta.
