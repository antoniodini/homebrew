## La struttura di Homebrew e delle sue metafore
Quando Max Howell ha progettato Homebrew, non ha scelto solo un nome  che richiamasse la produzione di birra fai-da-te, ma ha deciso di creare una intera classe di nomi ispirati all'attività dei birrifici. E sono tutte molto utili, anche se alle volte possono creare un po' di confusione.

Homebrew è stato creato utilizzando Ruby on Rails come linguaggio di programmazione e Git come sistema di versionamento per la gestione e la distribuzione dei software. Homebrew stesso funziona con una installazione di Git che aggiorna il codice del programma e la lista dei software che si possono installare. Questi software possono provenire dalla  lista ufficiale di ricette mantenute da Homebrew (<code>homebrew/core</code>), da liste di terze parti che possiamo aggiungere, da una lista che possiamo costruire noi stessi con le nostre ricette.

Ma qual è la nomenclatura utilizzata da Homebrew? Utilizzo ovviamente i nomi in inglese, cercando di tradurli per far capire anche il riferimento all'arte della birrificazine.

**Formula** è la definizione di un pacchetto software da installare.
**Keg** (barilotto di piccole dimensioni) è il prefisso di installazione di una Formula
 **Cellar** (cantina) è il posto dove vengono installate tutti i Keg
 **Tap** (rubinetto/spina) un deposito di Formule e/o di comandi realizzati da terzi 
**Bottle** (bottiglia) sono delle Keg precompilate anziché costruite dal codice sorgente
**Brew Bundle** Una estensione di Homebrew per descrivere delle dipendenze
**Cask** Una estensione di Homebrew per installare applicazioni native di macOS (con interfaccia grafica)
**opt prefix** un simlink verso una versione attiva di una Keg

Il punto di partenza sono le **Formule**: si tratta di semplici script in Ruby che permettono a Homebrew di sapere cosa fare per installare un particolare software: a quale siti collegarsi, quali sorgenti o binari scaricare, come configurare l’installazione, quali librerie e dipendenze risolvere. Tutti possono scrivere delle formule e, dato che sostanzialmente Homebrew **si appoggia sopra il software di versionamento git**,   creare una propria raccolta, oppure agganciarsi a quelle di terze parti.

Un esempio di formula? **Una delle più semplici**, che viene mostrata anche sul sito di Homebrew, è quella di <code>wget</code>:

````
class Wget < Formula
  homepage "https://www.gnu.org/software/wget/"
  url "https://ftp.gnu.org/gnu/wget/wget-1.15.tar.gz"
  sha256 "52126be8cf1bddd7536886e74c053ad7d0ed2aa89b4b630f76785bac21695fcd"

  def install
    system "./configure", "--prefix=#{prefix}"
    system "make", "install"
  end
end
````

Sul nostro Mac le formule vengono installate all’interno della directory <code>user/local/Cellar</code>. **La “cantina**” è il posto in effetti dove vanno le formule e tutto quel che serve al funzionamento del software, **sotto forma di barilotti (i Keg**). Se macOS contiene già delle librerie o software che stiamo installando nuovamente con Homebrew, l’installazione avviene **in modalità “keg-only**”, cioè il software viene installato dentro <code>user/local/Cellar</code> e non viene linkato nelle varie directory che vengono viste dal sistema, come <code>/usr/local/bin</code> e <code>/usr/local/lib</code>. Questo permette di mantenere più versioni degli stessi software.

Cosa succede quando si installa un’altra formula che ha bisogno di usare le stesse librerie? Facciamo un esempio. Se installiamo <code>brew install [un_software]</code> viene creata una cartella dentro <code>/usr/local/Cellar/un_software/version</code>. Se dobbiamo installarne <code>un_altro_software</code> che ha bisogno di librerie di quella versione di <code>un_software</code>, sarà automaticamente <code>brew install</code> a preoccuparsi di fare un modo che utilizzi proprio quella versione e non altre. **In modo da non disturbare né l’eventuale versione presente di default su macOS né le altre installate da Homebrew che abbiamo release differenti**.

Tra poco vedremo anche come utilizzare le raccolte di formule (**Tap**) realizzate da altri, come scaricare binari (**Bottle**), cioè programmi precompilati (questo allunga i tempi di download ma alleggerisce il vostro Mac dal lavoro di installazione che avviene dietro le quinte). Adesso, è il momento di una pausa e, dopo aver sentito tanto parlare di Homebrew, **anche di una bella birra**, perché no?

