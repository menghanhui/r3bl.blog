---
author: Aleksandar Todorović
comments: false
date: 2016-09-27 22:50:00+01:00
layout: post-bs
slug: popularnost-domacih-hostinga-i-domena
title: "Popularnost domaćih hostinga i domena"
categories: bs
tags:
- personal
- analytics
image:
  feature: abstract-1-3
---

Zanimalo me koliki je procenat najpopularnijih domaćih sajtova koji zapravo koriste domaći hosting i/ili domene. Da bih to saznao, odlučio sam da kreiram Python skriptu koja će pogledati listu najpopularnijih sajtova na našim prostorima (tako što će scrape-ovati Alexa.com), pogledati IP iza svake domene sa tog spiska, i onda pogledati u kojoj je državi taj server. U ovom članku je kratko objašnjenje skripte i rezultati za 500 najpopularnijih sajtova u državama bivše Jugoslavije.

Za potrebu ove skripte, pored osnovnih Python biblioteka, koristio sam još i [requests](http://docs.python-requests.org/en/master/), [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) i [python-geoip](http://pythonhosted.org/python-geoip/).

## Objašnjenje i poneki problemi sa kojim sam se susreo

* Pošto sam veliki fan open source-a, uštedio sam sebi jedno pola sata posla scrape-ujući Alexa.com tako što sam iskoristio već postojeću [alexa-topsites](https://github.com/inspace/alexa-topsites) skriptu (iako je zadnja promjena u ovoj skripti stara tri godine, samo je promjena jedne linije koda bila potrebna da skripta funkcioniše savršeno i dan danas).
* Dok sam ručno prolazio kroz nekoliko domena, primjetio sam da je CloudFlare dosta popularan na našim prostorima. Nažalost, zbog načina na koji CloudFlare funkcioniše, nisam u mogućnosti da dođem do fizičke lokacije servera sakrivenih iza CloudFlare-a, tako da su oni automatski otpali iz liste sajtova koji koriste domaći hosting.
* Pošto je naša regija relativno mala, dosta je slučajeva u kojoj je jedna domena (tipa `.rs`) vrlo popularna u drugoj državi (tipa Bosni i Hercegovini). Iako bi se ovo moglo smatrati domaćim hostingom, odlučio sam da pod domaćim hostingom smatram isključivo one koji su hostovani unutar države u kojoj su popularni.
* Pošto Alexa daje pun kurac rezultata, odlučio sam da se fokusiram na najpopularnijih 500 sajtova po državi.
* U rezultatima, iz logičnih razloga, nisu prikazani sajtovi koji nisu dostupni online u trenutku kada je skripta radila.
* Ukoliko želite da ponovite ovaj test, da ga odradite za neku drugu državu ili da povećate broj analiziranih sajtova, preuzmite Python skriptu [odavdje](#skripta) i pokrenite je sa `python naziv_skripte.py XX NN`, gdje je `XX` domena države, a `NN` broj najpopularnijih sajtova u toj državi koji želite da analizirate.

## Rezultati

Ukoliko želite da pređete direktno na rezultate neke države, to možete uraditi klikom na sljedeće linkove (po abecednom redu): [Bosna i Hercegovina](#bosna-i-hercegovina), [Crna Gora](#crna-gora), [Hrvatska](#hrvatska), [Makedonija](#makedonija), [Slovenija](#slovenija), [Srbija](#srbija).

**NAPOMENA:** Broj ispred sajta predstavlja rangiranje sajta po popularnosti u državi.

### Bosna i Hercegovina

* Broj sajtova sa serverom unutar Bosne i Hercegovine: 22/500
* Broj sajtova koji koriste `.ba` domenu: 76/500

Lista popularnih sajtova sa serverima unutar Bosne i Hercegovine:

<script src="https://gist.github.com/aleksandar-todorovic/a6cd6daadcb42bf0d8d19d54ee5cc439.js?file=rezultat-ba.txt"></script>

### Crna Gora

* Broj sajtova sa serverima unutar Crne Gore: 14/500 (~3%)
* Broj sajtova koji koriste `.me` domenu: 56/500

Lista popularnih sajtova sa serverima unutar Crne Gore:

<script src="https://gist.github.com/aleksandar-todorovic/a6cd6daadcb42bf0d8d19d54ee5cc439.js?file=rezultat-me.txt"></script>

### Hrvatska

* Broj sajtova sa serverima unutar Hrvatske: 112/500
* Broj sajtova koji koriste `.hr` domenu: 156/500

Lista popularnih sajtova sa serverima unutar Hrvatske:

<script src="https://gist.github.com/aleksandar-todorovic/a6cd6daadcb42bf0d8d19d54ee5cc439.js?file=rezultat-hr.txt"></script>

### Makedonija

* Broj sajtova sa serverima unutar Makedonije: 70/500
* Broj sajtova koji koriste `.mk` domenu: 151/500

Lista popularnih sajtova sa serverima unutar Makedonije:

<script src="https://gist.github.com/aleksandar-todorovic/a6cd6daadcb42bf0d8d19d54ee5cc439.js?file=rezultat-mk.txt"></script>

### Slovenija

* Broj sajtova sa serverima unutar Slovenije: 144/500
* Broj sajtova koji koriste `.si` domenu: 144/500

Lista popularnih sajtova sa serverima unutar Slovenije:

<script src="https://gist.github.com/aleksandar-todorovic/a6cd6daadcb42bf0d8d19d54ee5cc439.js?file=rezultat-si.txt"></script>

### Srbija

* Broj sajtova sa serverima unutar Srbije: 87/500
* Broj sajtova koji koriste `.rs` domenu: 112/500

Lista popularnih sajtova sa serverima unutar Srbije:

<script src="https://gist.github.com/aleksandar-todorovic/a6cd6daadcb42bf0d8d19d54ee5cc439.js?file=rezultat-rs.txt"></script>

## Skripta

<script src="https://gist.github.com/aleksandar-todorovic/a6cd6daadcb42bf0d8d19d54ee5cc439.js?file=domaci_hosting.py"></script>
