---
author: Aleksandar Todorović
comments: false
date: 2016-08-18 00:50:00+01:00
layout: post
slug: kompjuterska-pismenost-u-bih
title: "Kompjuterska pismenost u BiH (statistika iz rezultata popisa)"
categories: bs
tags:
- research
- rant
- technology
image:
  feature: abstract-1-3
---

Napokon sam imao malo prilike da se igram sa rezultatima popisa. Naravno, od svih podataka, mene je najviše zanimala kompjuterska pismenost na području BiH.

![neka random slika popisa](http://www.tacno.net/wp-content/uploads/2013/09/popis-635x300.jpg)

Na popisu, na ovo pitanje je odgovarala svaka osoba koja je imala 10 ili više godina u toku popisa, i osobe su se svrstavale u tri kategorije:

* kompjuterski pismena lica,
* lica koja djelimično poznaju rad na računaru,
* kompjuterski nepismena lica.

Rezultati su i više nego poražavajući.

Državni prosjek:

* 36,24% kompjuterski pismenih osoba,
* 23,86% djelomično kompjuterski pismenih osoba,
* 38,68% kompjuterski nepismenih osoba.

**Pažnja:** Ovdje (kao i u nastavku teksta), četvrta kategorija je "bez odgovora", i na nju ide ostatak procenata.

Muškarci imaju vidno bolji prosjek (38,21% pismenih, 25,48% djelimično pismenih, 35,12% nepismenih), dok se četiri od deset ženskih ispitanika izjasnilo kao u potpunosti kompjuterski nepismeno (34,35% pismenih, 22,32% djelimično pismenih, 42,06% nepismenih).

Nažalost, rezultati su prikazani u jebenoj Excel tabeli i ukupni brojevi su jedino što je vidljivo iz nje, tako da nema šanse da mogu vidjeti kako se procenti mijenjanju u odnosu na starosnu grupu (što bi garantovano bilo mnogo zanimljivije od ovoga).

Da uporedim broj kompjuterski nepismenih osoba sa ostalim statistikama iz popisa čisto da pokažem koliko je broj poražavajući:

* **Nacionalnost:** Broj kompjuterski nepismenih osoba je veći od broja onih koji su se izjasnili kao Srbi, ostali, nepoznati, i onih koji se nisu izjasnili po nacionalnoj pripadnosti — zajedno.
* **Radno sposobno stanovništvo:** Broj kompjuterski nepismenih osoba je za 200tinjak hiljada veći od broja zaposlenih osoba i za samo 130ak hiljada manji od ukupnog broja radno sposobnih osoba u BiH.
* **Starosna dob:** Broj kompjuterski nepismenih osoba je veći od broja maloljetnih stanovnika. Zapravo, veći je od broja svih osoba mlađih od 29 godina.

---

Sljedeće do čega sam pokušao da dođem jesu kompjuterski najpismenije i najnepismenije opštine u BiH. To se dokazalo kao ogroman problem jer su u jednu Excel tabelu nabacani i ukupni rezultati na nivou države, i rezultati entiteta i distrikta, i rezultati kantona, i rezultati opština, i to sve nekako na random nabacano (niti su entiteti na vrhu, niti su kantoni, niti je po alfabetnom ili azbučnom rasporedu, niti po broju stanovništva), tako da bih mrdnuo dalje od ovoga, morao sam da uradim podobru čistku tabele.

Međutim, zahvaljujući apsolutno užasnom layout-u tabele (a da ni ne pominjem katastrofalne engleske prevode imena kolona), imao sam dvije mogućnosti: ili da konvertujem tabelu u CSV i onda ručno sređujem layout CSV-a jedno pola sata, ili da ručno brišem podatke unutar [LibreOffice Calc-a](https://www.libreoffice.org/discover/calc/). Odlučih se (nažalost), za ovu drugu opciju.

20ak minuta kasnije, izbrisao sam nepotrebne podatke i došao do sljedeće statistike:

#### Top 10 kompjuterski najpismenijih opština u BiH

1. Novo Sarajevo: 61,11% (35.922 od 58.783)
2. Centar Sarajevo: 60,71% (30.451 od 50.161)
3. Stari Grad Sarajevo: 52,92% (17.867 od 33.760)
4. Novi Grad Sarajevo: 52,76% (55.791 od 105.753)
5. Vogošća: 50,52% (11.765 od 23.288)
6. Ilidža: 50,23% (29.711 od 59.151)
7. Istočno Novo Sarajevo: 48,80% (4.646 od 9.520)
8. Grad Mostar: 48,1% (45.967 od 95.573)
9. Banja Luka: 47,50% (79.187 od 166.696)
10. Tuzla: 45,89% (46.430 od 101.165)

#### Top 10 kompjuterski najnepismenijih opština u BiH

1. Kupres - RS: 80,42% (230 od 286)
2. Krupa na Uni: 72,17% (1.076 od 1.491)
3. Trnovo - FBiH: 64,95% (923 od 1.421)
4. Ribnik: 60,19% (3.343 od 5.554)
5. Istočni Stari Grad: 58,93% (617 od 1.047)
6. Oštra Luka: 58,88% (1.498 od 2.544)
7. Kneževo: 57,38% (5.145 od 8.967)
8. Kalinovik: 56,18% (1.073 od 1.910)
9. Bosansko Grahovo: 55,17% (1.286 od 2.331)
10. Petrovo: 53,18% (3.180 od 5.980)

Moglo bi se reći očekivano, urbanije sredine vladaju listom kompjuterski pismenih opština, a sredine sa manjim brojem stanovnika većinom preovladavaju listom najnepismenijih.

Ono što je apsolutno devastirajuće jeste da ne postoji niti jedna opština u BiH u kojoj je dvije trećine stanovništva izjavilo da je kompjuterski pismeno, i samo šest opština u kojima je svaka druga osoba kompjuterski pismena (svih šest u Kantonu Sarajevo).

Interesantno, opština sa najmanjim brojem stanovnika (Istočni Drvar sa samo 78 stanovnika) se nije našla ni na jednoj od ovih lista. Opština sa najvećim brojem stanovnika (Banja Luka) je zauzela deveto mjesto na listi kompjuterski najpismenijih.

#### Kompjuterska pismenost u entitetima i distriktu:

1. Federacija Bosne i Hercegovine: 38,51% kompjuterski pismenih, 36,4% kompjuterski nepismenih
2. Brčko Distrikt: 33,50% kompjuterski pismenih, 38,42% kompjuterski nepismenih
3. Republika Srpska: 32,36% kompjuterski pismenih, 42,74% kompjuterski nepismenih

Nikakvih značajnih razlika ovdje. Da oduzmem sarajevske opštine iz Federacije, statistika bi bila tu u rangu sa Distriktom i Republikom Srpskom.

#### Kantoni po procentu kompjuterski pismenih osoba:

1. Sarajevo: 52,98% (30,59% kompjuterski nepismenih)
2. Hercegovačko-Neretvanski: 40,22% (33,73% kompjuterski nepismenih)
3. Bosansko-Podrinjski: 38,56% (42,35% kompjuterski nepismenih)
4. Zapadnohercegovački: 37,69% (31,48% kompjuterski nepismenih)
5. Tuzlanski: 35,52% (41,29% kompjuterski nepismenih)
6. Zeničko-Dobojski: 34,65% (40,13% kompjuterski nepismenih)
7. Unsko-Sanski: 34,47% (33,52% kompjuterski nepismenih)
8. Kanton 10 (Livanjski): 33,71% (34,27% kompjuterski nepismenih)
9. Posavski: 32,28% (38,48% kompjuterski nepismenih)
10. Srednjebosanski: 31,52% (39,02% kompjuterski nepismenih)

Dakle, u samo jednom od kantona svaka druga osoba je računarski pismena. Pa divno.

## Moja daljnja analiza rezultata popisa

Iako sam planirao da se i dalje posvećujem rezultatima cenzusa i možda napišem još poneki članak ukoliko dođem do nekih zanimljivih otkrića, format javno dostupnih rezultata cenzusa me je toliko ubio u pojam da preuzete rezultate brišem sa svog laptopa i nikada im se više ne vraćam.

Četiri jebena sata sam potrošio da sortiram rezultate iz jedne tabele na četiri različita načina.
