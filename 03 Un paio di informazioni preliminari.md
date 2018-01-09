## Un paio di informazioni preliminari
Ho scritto sopra che Homebrew cerca di comportarsi da "bravo cittadino" di macOS e tenere le sue cose e i programmi che installa confinati in un'unica directory. Questo serve sia a tenere l'ambiente più "pulito" che a **risolvere un altro problema**, tipico del Mac.

Infatti, macOS oltre che un sistema operativo moderno e potente per utenti tradizionali, è anche una distribuzione Unix con una serie di software che appartengono al mondo dell'open source. Per vari motivi però Apple, man mano che presenta sul mercato nuove versioni del sistema operativo, **non aggiorna altrettanto con rapidità molti di questi software**. Ad esempio, la versione di PHP presente su macOS Sierra è la 5.6, ed è in ritardo di alcune release rispetto a quella disponibile sulle pagine del progetto open source (siamo da tempo alla versione 7). I motivi per cui questo accade vanno oltre lo scopo di questo piccolo libro, comunque vale la pena notare una cosa: non è (sempre) questione di pigrizia. Alcuni software open source quando vengono aggiornati cambiano tipo di licenza utilizzandone una più restrittiva che impedisce di utilizzarli all'interno di un prodotto ibrido come macOS, a metà fra il mondo proprietario e quello open. 

Comunque, **qui entra in gioco Homebrew**, che permette non solo di installare la versione più recente di un software e tenerla aggiornata in maniera molto semplice, ma addirittura di non entrare in conflitto con quella installata di serie su macOS da Apple, trovando posto per entrambe in due aree diverse. Di una si prende cura Apple, dell'altra si occupa Homebrew. In questo modo **è possibile scegliere quale utilizzare senza conflitti o sovrapposizioni**. Era in parte quello che intendevo quando scrivevo che il sistema è molto flessibile oltre che semplice da usare.

Un altro punto importante di Homebrew è che (dopo l'installazione) funziona senza dover ricorrere a <code>sudo</code>, perché si crea una versione di <code>usr/local</code> a cui ha accesso. Non è un vantaggio da poco, Per questo occorre utilizzare un'unica volta il comando che evoca il "super utente" durante l'installazione: <code>sudo</code> in questa fase di installazione serve per non doverlo fare più dopo. E per questo il vostro utente su Mac deve essere un amministratore di cui conoscete la password. 

Tutto questo mantiene il Mac **in situazione di ottimo bilanciamento da un lato e di sicurezza dall'altra**. Consiglio di non installare altri software "esterni" dentro la directory di Homebrew al fine di evitare complicazioni inutili. Non dovrebbero essercene, a meno di non voler cercare di mettersi nei guai da soli e, ad esempio, installare software con lo stesso nome di quelli installati da gestore di pacchetti. Ma chi vorrebbe fare una cosa tanto sciocca?

Avete seguito questi passaggi? Ce n'è ancora un altro da fare per verificare che tutto sia andato bene. E per eseguirlo possiamo dare il primo comando nel terminale con Homebrew. Questo mi permette di spiegare subito una cosa: la struttura base dei comandi di Homebrew. **È la seguente: "brew", più un comando, più uno o più eventuali "argomenti" (o parametri) che specificano meglio il comando**. Ad esempio, scriviamo:

<code>brew doctor</code>

"Doctor" è un comando di Homebrew senza attributi. Con questo comando attiviamo la funzione diagnostica che verifica che la nostra installazione sia andata a buon fine e che tutto funzioni. **Se è tutto ok** il sistema risponderà nella riga immediatamente successiva:

<code>Your system is ready to brew.</code>

Invece, un classico comando con argomento di Homebrew è quello che serve per installare il software <code>wget</code> che dicevamo poco sopra:

<code>brew install wget</code>

È una sintesi molto forte. **Per adesso mettetela da parte** e vediamo prima un'altra cosa: come funziona concretamente Homebrew.
