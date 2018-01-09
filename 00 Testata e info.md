# Homebrew a tutta birra!  

## La guida al gestore di pacchetti software open source per macOS

#### L'autore
*Antonio Dini* 
Giornalista e saggista, è nato a Firenze e ora vive a Milano. Scrive non solo di tecnologia e ha pubblicato vari libri. Il suo sito è [Antonio Dini](http://antoniodini.com) e il suo canale Telegram invece si chiama [Mostly, I Write](http://telegram.me/mostlyiwrite)  


#### Disclaimer
*L’autore di questa guida non si assume nessuna responsabilità in caso di danni, perdita di dati o altri problemi riconducibili direttamente o indirettamente all’uso delle informazioni contenute in testo, che vengono fornite a scopo meramente illustrativo e senza garanzia di funzionamento. Insomma, se succede qualcosa poi non prendetevela con me*.


#### Licenza Creative Commons
*Attribuzione - Non commerciale - Condividi allo stesso modo*. 
In altre parole, questa licenza permette alle altre persone di modificare e sviluppare non commercialmente l'opera, riconoscendo sempre l'autore originale (cioè me). 

Vi invito a leggere questo testo qui su GitHub, correggerlo, modificarlo e sottoporre le modifiche per essere integrate nel testo principale (cioè sempre questo). 

#### A chi è rivolto questo libro
Se siete impazienti, questo libro fa per voi. Troverete **tutto quel che vi serve in maniera sintetica, veloce e completa**. Attenzione però: comprate e leggete questo libro se:
- Sapete programmare almeno un po’ a livello di base
- Sapete come programmare delle applicazioni web
- Utilizzate macOS Sierra o successivi
- Sapete usare il Terminale e la riga di comando
- Sapete usare un editor di testo in una console


#### Lo scopo di questo libro
Voglio darvi la possibilità di utilizzare in maniera approfondita Homebrew raccogliendo tutte le informazioni utili alla sua installazione, utilizzo, aggiornamento, manutenzione ed eventuale migrazione in un unico testo. Lo scopo dunque è fornire **un orientamento avanzato all’uso di Homebrew**.  


#### Convenzioni usate in questo libro
I link ai siti web (cliccabili o no), gli indirizzi email e i termini particolari usati la prima volta vengono indicati con il normale carattere del testo in corsivo.

Ad esempio:
*[https://www.antoniodini.com](https://www.antoniodini.com)*


Con il testo scritto con caratteri non proporzionali vengono indicati listati di codice, elementi di programmi come variabili e nomi di funzione, variabili ambientali, dichiarazioni, parole chiave e comandi da digitare nella shell.

Ad esempio:
Il programma per scaricare documenti dal web si chiama <code>wget</code>


Vengono scritti con caratteri non proporzionale anche i comandi da digitare nel terminale. I loro argomenti sono in corsivo e tra parentesi quadra quando devono essere rimpiazzate da valori forniti dall’utente o da valori determinati dal contesto.

Ad esempio:
<code>brew install [<i>nome_del_pacchetto</i>]</code>

<code>touch <i>da_qualche_parte/nel_vostro_disco/un.file</i></code>

Un comando può andare a capo nell’impaginazione del testo sul vostro schermo ma è sempre da intendersi come una riga unica.