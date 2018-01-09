## Installazione di Homebrew

Prepariamoci ad usare Homebrew. In questo libro partiamo dall’idea che stiate usando un Mac con macOS Sierra. L'ambiente non cambia con le versioni immediatamente precedenti e ragionevolmente con quelle immediatamente successive (come High Sierra), ma noi qui ci basiamo su Sierra.

Prima di procedere all’installazione di Homebrew occorre mettere nel nostro Mac, se già non c'è, un altro software. Bisogna avere infatti **i Command Line Tools di Apple installati**. Sono una componente di **Xcode** (l’ambiente di sviluppo grafico delle app per macOS e per iOS) che fondamentalmente contiene i compilatori (<code>gcc</code> e alcuni framework), ma non occorre scaricare tutto il malloppo. Con un semplice comando infatti si prende dai server di Apple l'ultima versione del pacchetto delle CLT (sono circa 120 megabyte) che poi verrà regolarmente aggiornato attraverso il Mac App Store. Il comando da Terminale è il seguente:

<code>xcode-select --install</code>

Oppure potete seguire un’altra strada. Se digitate nel Terminale: 

<code>gcc</code>

e non avete già installato i CLT, vi apparirà una finestra di dialogo che vi offre di installare questo strumenti oppure tutto Xcode. Dal momento che ai fini dell’uso di Homebrew **avere Xcode non è necessario**, installiamo nel Mac solo i Command Line Tools.

Al termine dell’installazione delle CLT, si può passare a **installare Homebrew**. [Sul sito degli sviluppatori](https://brew.sh), proprio nella home page, si trova la riga di comando che dobbiamo copiare e incollare nel nostro terminale per far scaricare e installare Homebrew. Se preferite, potete prenderla da qui (è aggiornata a maggio 2017): 

<code>/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</code>  

Deve andare tutto su una riga sola e con le virgolette incluse, ovviamente.

Passeranno alcune frasi e comandi sul nostro terminale. La cosa bella è che non dobbiamo preoccuparci di quel che c’è scritto: **è la meraviglia dei gestori di pacchetti**, pensano tutto a loro. Comunque, sono i comandi e lo status di avanzamento delle operazioni che vengono svolte automaticamente. A seconda della potenza del vostro Mac e della velocità della connessione, in cinque minuti dovrebbe essere tutto pronto.

Una volta installato, Homebrew si comporta da cittadino esemplare del mondo Mac: **mette infatti tutto all’interno di un’unica directory**. È alla radice del nostro volume di avvio: <code>/usr/local</code>. Al suo interno, c’è tutto quel che ci serve per far funzionare Homebrew. Infatti il gestore di pacchetti non installerà nessun software al di fuori di quella directoty, a meno che non vogliate farlo voi (ma è meglio non complicarsi la vita, no?). 
