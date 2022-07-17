---
language: Solidity
filename: learnSolidity.sol
contributors:
  - ["Nemil Dalal", "https://www.nemil.com"]
  - ["Joseph Chow", ""]
  - ["Bhoomtawath Plinsut", "https://github.com/varshard"]
  - ["Shooter", "https://github.com/liushooter"]
  - ["Patrick Collins", "https://gist.github.com/PatrickAlphaC"]
translators:
    - ["Alias", "http://github.com/al-ias"]
lang: it-it
---

Solidity permette di programmare su [Ethereum](https://www.ethereum.org/), una
macchina virtuale basata sulla blockchain che consente la creazione e
l'esecuzione degli smart contract senza che sia richiesta centralizzazione o
fiducia negli attori coinvolti.

Solidity è un linguaggio di programmazione di contratti tipizzato staticamente e
ha molte cose in comune con Javascript e C. Come per gli oggetti nella
programmazione ad oggetti, ogni contratto contiene variabili di stato, funzioni
e tipi di dato semplici. Tra le funzionalità specifiche dei contratti troviamo
le clausole (guardie) dei modifier, gli event notifier per i listener, e le
variabili globali custom.

Come esempi di contratti su Ethereum troviamo sistemi di crowdfunding, voto,
[finanza decentralizzata](https://defipulse.com/) e aste al buio.

Compiere errori nel codice Solidity può portare a rischi e costi alti, quindi
bisogna stare molto attenti nel testare e rilasciare le modifiche lentamente. A
CAUSA DEI CONTINUI CAMBIAMENTI DI ETHEREUM È IMPROBABILE CHE QUESTO DOCUMENTO
RESTI AGGIORNATO, QUINDI COSNIGLIAMO DI SEGUIRE LA CHAT ROOM DI SOLIDITY E IL
BLOG DI ETHEREUM PER TENERSI AGGIORNATI. TUTTO IL CODICE QUI PRESENTE E' FORNITO
COSÌ COM'È, CON ANNESSI RISCHI SOSTANZIALI DI ERRORI O PATTERN DI PROGRAMMAZIONE
DEPRECATI. 

A differenza di altri tipi di codice, potresti aver bisogno di usare pattern di
pausing, deprecation e throttling usage per ridurre il rischio. Questo documento
tratta principalmene la sintassi e quindi esclude molti design pattern in voga.

Visto che Solidity e Ethereum sono in continuo sviluppo, le funzionalità
sperimentali o beta sono evidenziate e soggette a cambiamenti. Ogni Pull Request
è ben accetta.

# Lavorare con Redux e Metamask

Uno dei modi più semplici di scrivere, distribuire e testare il codice Solidity
è usare:

1. [L'amibiente di svillupo online Remix](https://remix.ethereum.org/);
2. [Il wallet Metamask](https://metamask.io/).

Per cominciare, [scarica l'estensione per browser di Metamask](https://metamask.io/).

A installazione completata, useremo Remix. Il codice qui sotto sarà
pre-inizializzato, ma prima di addentrarci nel codice diamo un occhiata a
qualche trucco su come iniziare ad usare Remix. Inizializza tutto [clickando su questo link](https://remix.ethereum.org/#version=soljson-v0.6.6+commit.6c089d02.js&optimize=false&evmVersion=null&gist=f490c0d51141dd0515244db40bbd0c17&runs=200).

1. Scegli il compilatore per Solidity

![Solidity-in-remix](../images/solidity/remix-solidity.png)

2. Apri il file caricato su quel link

![Solidity-choose-file](../images/solidity/remix-choose-file.png)

3. Compila il file

![Solidity-compile](../images/solidity/remix-compile.png)

4. Fai il deploy

![Solidity-deploy](../images/solidity/remix-deploy.png)

5. Smanetta con gli smart contracts

![Solidity-deploy](../images/solidity/remix-interact.png)

Hai distribuito il tuo primo smart contract! Congratulazioni!

Potrai testarlo e smanettare con le funzioni definite. Dai un occhiata ai
commenti per vedere cosa fa ogni funzione.