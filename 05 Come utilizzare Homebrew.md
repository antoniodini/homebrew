## Come utilizzare Homebrew
Abbiamo installato Homebrew e verificato che l’installazione sia andata a buon fine. Nel caso invece ci siano stati problemi <code>brew doctor</code> fornisce anche le principali soluzioni. Effettuare un troubleshooting complessivo dei possibili problemi che si possono trovare installando Homebrew va oltre gli obiettivi di questo piccolo libro. Ma sulle pagine dedicate del sito di Homebrew potete trovare buona parte dell’aiuto di cui avete probabilmente bisogno, partendo da qui: [http://docs.brew.sh/Troubleshooting.html](http://docs.brew.sh/Troubleshooting.html)

Adesso possiamo cominciare a usare Homebrew. Se pensate di **migrare da una precedente installazione** (ma questa volta volete procedere in maniera più strutturata) vi consiglio di leggere questa parte ma, prima di iniziare, saltare al capitolo “*Come migrare Homebrew su una nuova macchina*”, perché troverete parecchie dritte che spero vi siano utili.

La prima cosa che potreste voler fare è **cercare nuovi pacchetti** all’interno di Homebrew. Il comando che fa per voi è ovviamente <code>search</code>. La sintassi corretta è:

<code>brew search [nome_del_programma]</code>

Se invece non avete idea e scrivete semplicemente:

<code>brew search</code>

Homebrew vi fornirà la lista di tutte le formule presenti nel repository standard (che poi sarebbe <code>homebrew/core</code>). **La lista è parecchio lunga**. Ma ci sono anche altri modi per cercare i pacchetti software che vi interessano. Il primo. consiste nell’andare sul sito [http://searchbrew.com/](http://searchbrew.com/) che permette di cercare tutte le combinazioni di parole chiave che possono essere utili a trovare quello di cui avete bisogno. Inoltre, da Search Brew si può andare anche al progetto gemello Brew Update Notifier ([https://github.com/stephennancekivell/brew-update-notifier](https://github.com/stephennancekivell/brew-update-notifier)) che permette di attivare una notifica su macOS quando una delle vostre formule è stata aggiornata. C’è anche un software a interfaccia grafica che permette di gestire gli aggiornamenti oltre alle istallazioni: ne parleremo nel capitolo finale del libro “*Alcuni piccoli trucchi*”.

Su GitHub c’è anche il repository principale con **la lista di tutti i pacchetti** (cioè le formule) supportate ufficialmente da Homebrew. Si trova a questo indirizzo: [https://github.com/Homebrew/homebrew/tree/master/Library/Formula](https://github.com/Homebrew/homebrew/tree/master/Library/Formula)

Se volete scoprire **cosa faccia un pacchetto** (e se per caso lo abbiate già installato), a quale tap appartenga e tutto il resto, il comando giusto è <code>info</code>. Se chiedo a Homebrew sul Mac con cui sto scrivendo questo libro (MaxMini) informazioni su <code>wget</code>, questa è la risposta:

````
MaxMini:~ antonio$ brew info wget
wget: stable 1.19.1 (bottled), HEAD
Internet file retriever
https://www.gnu.org/software/wget/
Not installed
From: https://github.com/Homebrew/homebrew-core/blob/master/Formula/wget.rb
==> Dependencies
Build: pkg-config ✔
Required: openssl ✔
Optional: pcre ✘, libmetalink ✘, gpgme ✘
==> Options
--with-debug
	Build with debug support
--with-gpgme
	Build with gpgme support
--with-libmetalink
	Build with libmetalink support
--with-pcre
	Build with pcre support
--HEAD
	Install HEAD version
MaxMini:~ antonio$ 

````

Per **installarlo nella modalità automatica** basta digitare:

<code>brew install wget</code>

a cui segue la risposta di Homebrew:

````

MaxMini:~ antonio$ brew install wget
==> Downloading https://homebrew.bintray.com/bottles/wget-1.19.1.sierra.bottle.tar.gz
######################################################################## 100,0%
==> Pouring wget-1.19.1.sierra.bottle.tar.gz
🍺  /usr/local/Cellar/wget/1.19.1: 10 files, 1.6MB
MaxMini:~ antonio$ 

````

Installazione portata a termine. E grazie a Unicode, abbiamo anche **una piccola birretta** a testimoniare che il lavoro è andato a buon fine.
  
Adesso, se **chiediamo di nuovo info** su <code>brew</code> la risposta di Homebrew cambia:

````

MaxMini:~ antonio$ brew info wget
wget: stable 1.19.1 (bottled), HEAD
Internet file retriever
https://www.gnu.org/software/wget/
/usr/local/Cellar/wget/1.19.1 (10 files, 1.6MB) *
  Poured from bottle on 2017-05-08 at 17:05:56
From: https://github.com/Homebrew/homebrew-core/blob/master/Formula/wget.rb
==> Dependencies
Build: pkg-config ✔
Required: openssl ✔
Optional: pcre ✘, libmetalink ✘, gpgme ✘
==> Options
--with-debug
	Build with debug support
--with-gpgme
	Build with gpgme support
--with-libmetalink
	Build with libmetalink support
--with-pcre
	Build with pcre support
--HEAD
	Install HEAD version
MaxMini:~ antonio$ 

````

