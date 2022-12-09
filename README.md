# ReverseIT Library
Questo repository contiene la libreria di ReverseIT.

Leggere accuratamente questo documento se si è interessati a contribuire al progetto.

## Politica sui contenuti

Sono ben accetti contenuti pertinenti alle tematiche trattate (Reverse Engineering e Cyber Security). La seguente lista evidenzia gli argomenti che NON sono graditi:

* Contenuti riguardanti il cracking/unpacking di protezioni commerciali *attulamente* utilizzate.
* Contenuti riguardanti l'hacking di computer/server *attualmente* vulnerabili
* Contenuti il cui unico scopo sia quello di diffondere materiale pirata e non conoscenza. Ad esempio guide su come scaricare illegalmente un programma completo che sia altrimenti acquistabile pagando.
* Contenuti di analisi di malware che includano codice virale, se non opportunamente commentato e racchiuso dentro gli appositi tag. NON includere mai link malevoli nei documenti, se non opportunamente modificati per non essere accidentalmente visitati.

E' possibile contribuire guide sul cracking SOLO di protezioni ormai obsolete e non più utilizzate, in modo di poter imparare il funzionamento di una determinata protezione usata in passato.

I documenti riguardanti l'hacking NON devono includere bersagli attualmente vulnerabili. E' possibile contribuire un documento che tratti di come un determinato server è stato violato, solo una volta che quest'ultimo è stato messo in sicurezza.

Non è consentita la diffusione di eseguibili virali, ne di link diretti ad essi. E' tuttavia possibile, soprattutto nei documenti di malware analysis, includere i relativi hash md5 in modo da dare la possibilità ai lettore con accesso a virusshare[dot]com o simili, di poter ottenere i campioni.

Non è necessario essere gli autori originali di un documento che si intende includere alla libreria, tuttavia è preferibile, ove possibile, contattare il creatore e chiedere il permesso.

I contributi dovranno essere in formato PDF o ZIP (nel caso di più file).

Eseguire una scansione su virustotal[dot]com prima di procedere con la PR. NON verranno accettati contributi il cui tasso di detection sia elevato senza un chiaro motivo.

Ricordate che il fine ultimo è esclusivamente la diffusione della conoscenza di queste materie.


## Come inviare il tuo contributo

Segui attentamente le seguenti istruzioni per essere sicuro che il tuo contributo venga accettato.

1) Leggi attentamente la nostra politica sui contenuti
2) Se sei l'autore originale del documento, esportalo in formato PDF e continua dal punto 3. Se invece vuoi inviare un documento che hai trovato in rete, assicurati di produrre un PDF valido usando esclusivamente il tool opensource *wkhtmltopdf*. La sintassi da usare è la seguente:

`wkhtmltopdf url_pagina_web nome_documento.pdf`

3) Esegui il fork di questo repository. Crea un nuovo branch con un nome significativo (ad esempio il titolo del documento che vuoi inviare). Copia il file in `/library/INIZIALE_NOME_AUTORE_ORIGINALE/`, se non esiste gia una cartella con l'iniziale del nome dell'autore originale, procedere creandola. Infine modificare il file `library.index.json` aggiungendo, alla fine di esso, il seguente nodo json opportunamente valozziato (rispettando l'indentatura):

```json
,{
    "title": "TITOLO DEL DOCUMENTO",
    "description": "BREVE DESCRIZIONE DEL CONTENUTO DEL DOCUMENTO",
    "categories" : [
        "CATEGORIE DEL DOCUMENTO",
        "SEPARATE DA VIRGOLA"
    ],
    "author": "NOME DELL'AUTORE ORIGINALE DEL DOCUMENTO",
    "language": "CODICE LINGUA DEL DOCUMENTO (ES: 'it' PER ITALIANO O 'en' PER INGLESE)",
    "version": "VERSIONE DEL DOCUMENTO",
    "creation_date": "DATA CREAZIONE DOCUMENTO (NEL FORMATO YYYY-MM-DD)",
    "publication_date": "DATA ODIERNA (NEL FORMATO YYYY-MM-DD)",
    "download_url": "URL AL DOWNLOAD, RELATIVO A QUESTO REPOSITORY"
}
```

Le categorie attualmente dispobili sono:
* Cracking
* Crackmes
* Cyber Security
* Hacking
* Malware Analysis
* Programming
* Unpacking
* Windows Internals / DOS Internals

Se si ritiene che il documento non rientri in nessuna di queste categorie, occorre farlo presente nel testo della PR, in modo tale da verificare la possibilità di crearne una nuova.

Il campo download_url deve avere il seguente formato:
`https://raw.githubusercontent.com/ReverseIT-GH/library/master/library/INIZIALE_NOME_AUTORE_ORIGINALE/NOME_DOCUMENTO.FORMATO_DOCUMENTO`

4) Adesso è possibile inviare una PR dal vostro branch alla master della library.

Ricordate sempre di fornire agli amministratori il tempo necessario alla verifica del vostro contributo.

Per eventuali dubbi o problemi è possibile aprire una issue con una spiegazione accurata e dettagliata.