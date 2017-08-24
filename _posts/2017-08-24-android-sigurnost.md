---
author: Aleksandar Todorović
comments: true
date: 2017-08-21 12:00:00+02:00
layout: post-bs
slug: android-sigurnost
title: "Android i sigurnost: 5 razloga zašto smatram da je Android (napokon) siguran"
categories: bs
tags:
- blogging
- personal
image:
  feature: abstract-1-3
---

Nakon što sam nedavno kupio telefon koji (za divno čudo), radi na najnovijoj verziji Androida, odlučio sam da navedem neke sigurnosne novine koje je Google uveo u Android od verzije 4.4 (KitKat), pa sve do verzije 8.0 (Oreo) i da dam svoje mišljenje zašto smatram da je Android, napokon, siguran operativni sistem.

![android security logo](https://tr4.cbsistatic.com/hub/i/r/2016/03/10/9e4d8190-70c5-49fc-8411-526754dee945/resize/770x/f9f866239afeaab1415c8ceb9127ea92/android-security-1.jpg)

Nedavno sam se riješio svog kineskog [Lenovo A5000](http://www.gsmarena.com/lenovo_a5000-7167.php) telefona. Služio me je odlično gotovo dvije godine, međutim, nikada se nisam previše oslanjao na pametne telefone. Znajući da Android telefoni, po default-u nisu update-ovani godinama, nikada ništa ozbiljno nisam držao na telefonu (tipa poslovne mejlove) niti sam ikada instalirao aplikacije kojima ne vjerujem. Služio mi je više kao igračka koja, eto, između ostalog, može da posjećuje Internet.

Nedavno sam se odlučio za pronalazak novog telefona. Kriterijum je bio jasan i jednostavan: mora imati što noviji Android i mora primati update (ne mora svaki, ali sigurnosne mora) minimalno godinu dana. Sve ostalo manje-više, moglo se pregovarati. Što sam tražio, to sam i našao u [Nexus 5X modelu](http://www.gsmarena.com/lg_nexus_5x-7556.php), modelom iz kraja 2015. godine, lako dostupnom na našim prostorima i sa prihvatljivom cijenom (za nekoga kome se ne troši 500+ eura za telefon).

Kratka uporedba mog starog i novog telefona:

* **Lenovo A5000:**
    * Originalno došao sa Android KitKat (4.4).
    * Upgrade-ovan na Android Lollipop (5.0) kada je Lenovo pustio jedini update za ovaj telefon.
    * Security Patch level: Jul 2015. godine.
    * Hardverske specifikacije: Quad-core 1.3 GHz Cortex-A7 / 1 GB RAM / 4000 mAh baterija.
* **Nexus 5X:**
    * Originalno Marshmallow (6.0).
    * Upgrade-ovan na trenutno najnoviju Android verziju Oreo (8.0).
    * Security Patch level: August 2017.
    * Hardverske specifikacije: Hexa-core (4x1.4 GHz Cortex-A53 i 2x1.8 GHz Cortex-A57) / 2 GB RAM / 2700 mAh baterija.

Dakle, ovo je kao da sam iz Golfa trojke prešao u Teslu Model 3. Punim rezervoarom (to jest, baterijom) sada mogu preći manju distancu, međutim doza komfora i sigurnosti u korišćenju je neuporediva.

Sada ću detaljno objasniti razloge zašto mislim da je Google napokon izvadio glavu iz guzice, shvatio sigurnost Android korisnika kao nešto na šta treba obratiti pažnju, i novine koje je uveo od KitKat (4.4) verzije pa na vamo.

Razlog zašto sam odabrao KitKat kao početnu tačku jeste što veći procenat korisnika pametnih telefona koristi KitKat od procenta desktop računara koji koriste Windows XP (izvor: [NetMarketShare](https://www.netmarketshare.com)). Pored svakog podnaslova se nalazi verzija u kojoj je ta novina predstavljena.

## 1. Security patch level (5+ verzije)

Pošto sam ovu novinu već spomenuo u komparaciji mog starog i novog telefona, da je odma i objasnim:

Način na koji Google distribuira popravke sigurnosnih propusti jeste da ih sredinom svakog mjeseca prikupi, te pusti u javnost jedan update koji popravlja sve sigurnosne propuste koje su pronašli u zadnjih mjesec dana (to jeste, od prethodnog puštanja u javnost sigurnosnih popravki).

Security patch level je jednostavno prikaz zadnjeg sigurnosnog update-a kojeg je telefon primio. Uveden je 2015. godine, malo nakon objave Android 5.0 Lollipop verzije, i može se pronaći u `Settings` -> `About phone` -> `Android security patch level`. Pored Google-a i njegovih Nexus i Pixel linija, za sada tri proizvođača održavaju liste propusta na modifikovanim Androidima koji se nalaze na telefonima na tržištu: ([Samsung](http://security.samsungmobile.com/smrupdate.html), [LG](https://lgsecurity.lge.com/security_updates.html) i [Motorola](https://motorola-global-portal.custhelp.com/app/software-upgrade-security/g_id/5593)). Ostale, izgleda, pretjerano baš i ne zanima sigurnost korisnika njihovih telefona.

Ovo spominjem kao prvu bitnu promjenu kroz različite verzije Androida, jer makar znaš na čemu si kada možeš da vidiš kada je zadnji put tvoj telefon primio popravke za sigurnosne propuste. U konkretnim primjerima na ova dva telefona, Lenovo je zadnji primio u julu 2015. (dakle, ranjiv je na sve sigurnosne propuste iz zadnje dvije godine), dok Nexus još uvijek prima redovne sigurnosne ispravke (ovaj konkretan model će ih primati minimalno do septembra 2018. godine).

![Googe-ov Android security patch level](https://i.imgur.com/YNRedYG.png)

## 2. Enkripcija čitavog diska je uključena po default-u (6+ verzije)

Još otkako je Android postao popularan, uvijek je imao opciju enkripcije čitavog diska (eng. _full disk encryption_, ili, još jednostavnije, _FDE_). To je podrazumijevalo da možete otići u `Settings` -> `Security` i kliknuti na `Encrypt Phone`. Proces treba uraditi samo jednom, i u prosjeku traje nekih dva-tri sata. Ono što radi jeste enkriptuje sve podatke na telefonu, tako da neko ko ima fizički pristup uređaju ne može uraditi ništa da dođe do podataka koji su na telefonu (pod uslovom da ne zna PIN/šifru/pattern za otključavanje telefona).

Od šestice (Marshmallow), "hard disk" telefona je enkriptovan po default-u, i po default-u neko sa fizičkim pristupom uređaju ne može da dođe do podataka na telefonu bez da zna vašu šifru/PIN/pattern za otključavanje.

### 2.1 Enkripcija datoteka pojedinačno (7+ verzije)

Novost u verziji sedam (Nougat) je dodatak opcionalne enkripcije datoteka pojedinačno ([_file-based encryption_](https://source.android.com/security/encryption/file-based), ili, još jednostavnije, _FBE_). Kada je enkripcija čitavog diska uključena, prilikom pokretanja telefona uvijek je potrebno otključati telefon da bi on izvršio neke esencijalne zadatke (tipa alarm). To je očito bilo neprihvatljivo za Google inžinjere iz nekog meni nepoznatog razloga, pa su odlučili da malo "spuste loptu" i uvedu enkripciju datoteka pojedinačno. Ukoliko se izabere ova opcija, esencijalni zadaci telefona (tipa alarm) rade čim se pokrene telefon, bez da je potrebno da se telefon otključa tokom pokretanja. Ova opcija generiše pojedinačni ključ za svaku datoteku i enkriptuje svaku datoteku pojedinačno, a esencijalne funkcije telefona nisu enkriptovane.

Razlika u algoritmu: FDE koristi AES algoritam sa 256-bitnim ključem (maksimalna dužina koju podržava AES standard). FBE koristi AES algoritam sa 128-bitnim ključem (minimalna dužina koju podržava AES standard). U enkripciji, veći ključ je uvijek bolji, međutim, sa ovom pojedinačnom enkripcijom je potrebno čuvati mnogo veći broj ključeva, što vjerujem da je razlog zašto su odabrali ključeve minimalne dužine. Kod enkripcije čitavog diska, čitav disk je enkriptovan jednim ključem, tako da on može da bude maksimalne dužine.

Sve u svemu, po default-u, podaci na uređaju su enkriptovani, a, ukoliko se korisnik odluči da zamijeni malo sigurnosti za mali pomak u komforu prilikom korišćenja, enkripcija pojedinačnih podataka mu pruža tu opciju.

## 3. Permisije za aplikacije (6+ verzije)

Prije Android šestice (Marshmallow), prije instalacije neke aplikacije ste uvijek dočekani sa listom dozvola sa kojom se morate složiti da biste instalirali aplikaciju. Morali ste pristati na sve ili ništa. Ukoliko ste instalirali Facebook aplikaciju, morali ste pristati na to da, između ostalog, Facebook ima pristup vašoj listi kontakta, SMS porukama i mnogim drugim. Pošto se meni nikada nije dalo biti jedan od tih na kojima Facebook vrši eksperimente koji [upravljaju emocijama svojih korisnika](http://www.slate.com/articles/health_and_science/science/2014/06/facebook_unethical_experiment_it_made_news_feeds_happier_or_sadder_to_manipulate.html) ili [testiraju lojalnost svojih korisnika](https://www.theverge.com/2016/1/4/10708590/facebook-google-android-app-crash-tests), moje rješenje je bilo jednostavno: nikada ne imati niti jednu Facebook-ovu aplikaciju na telefonu.

Jednostavno, u tom "ili daj sve, ili ne možeš koristiti naš proizvod" izboru, često sam bio prisiljen izabrati ovu drugu opciju, jer mi je stalo do toga da ne dam mogućnost kompanijama da imaju pristup podacima koji joj nisu potrebni za esencijalno pružanje servisa.

Međutim, većina ljudi ovo ne radi. Većina ljudi slijepo klikće na "prihvatam" kada izađe prostor sa zahtjevima koje aplikacija traži. Igre ovo najviše iskorištavaju, pa tako možete naći [jebeni soliter koji traži pristup vašim kontaktima i informacijama o pozivima koje pravite](https://play.google.com/store/apps/details?id=com.spacegame.solitaire.basic).

Od Android šestice, Google je uradio nešto povodom toga. Uzmimo za primjer aplikaciju koja traži pristup vašoj kameri za neko ne-esencijalno pružanje usluga. Vi instalirate aplikaciju, koristite je, i ukoliko pokrenete tu opciju unutar aplikacije koja zahtijeva pristup vašoj kameri, otvara vam se pop-up u kojem piše da aplikacija traži pristup vašoj kameri, što možete dozvoliti ili odbiti.

### 3.1 Centralno mjesto za upravljanje permisijama (6+ verzije)

Od verzije 6 (Marshmallow), Google je uveo još jednu novinu: centralno mjesto za upravljanje permisijama. Malo je zabačeno (`Settings` -> `Apps` -> _gear_ ikona -> `App permissions`), međutim tu je. Ovdje vidite spisak nekih najesencijalnijih privatnosnih permisija, i, kada kliknete na neku od njih, vidite listu svih instaliranih aplikacija koje traže pristup toj permisiji.

Konkretan primjer: kada otvorim lokaciju na tom ekranu, vidim da imam 30 instaliranih aplikacija koje traže pristup mojoj lokaciji. Pažljivo sam pregledao svaku od njih i došao do zaključka da želim da dam tu dozvolu ukupno 9 (od tih 30) aplikacija (npr. Google Maps treba pristup mojoj aplikaciji da bi funkcionisao), dok sam drugim aplikacijama onemogućio da koriste moju lokaciju za pružanje usluge (npr. Shazam apsolutno ne treba pristup mojoj lokaciji da bi funkcionisao).

![pristup lokaciji na mom telefonu](https://i.imgur.com/majnLAY.png)

## 4. Automatsko preuzimanje popravki sigurnosnih propusta (7+ verzije)

Prije Nougat (7.0) verzije, kada izađu popravke sigurnosnih propusta vama izađe notifikacija na koju morate kliknuti da bi vaš telefon preuzeo te popravke. Od verzije sedam, one se automatski preuzimaju sa Interneta, i, jednom kada su spremne da budu instalirane, vama izađe notifikacija da trebate da restartujete telefon da se popravke instalirale.

Automatsko preuzimanje popravki sigurnosnih propusta time postaje nešto na šta ne morate da eksplicitno pristanete. Umjesto toga, sve što morate jeste da ponovo uključite vaš telefon (a to će se desiti prije ili kasnije) i najnovije popravke sigurnosnih propusta su već tu na vašem telefonu.

## 5. Hardverski način čuvanja kredencijala (7+ verzije)

Kada se prijavite na neki sajt koristeći vaš telefon, vaši podaci o prijavi moraju da se sačuvaju... negdje. U starijim verzijama telefona koji koriste Android, to je bilo softversko rješenje, oko verzije šest to je mogao da bude ili hardversko ili softversko rješenje, a sa Nougat (7.0) verzijom, sada mora postojati odvojeni prostor u memoriji telefona koji će služiti isključivo za čuvanje kredencijala.

Dakle, Google je postojanje tog specijalnog prostora stavio kao hardverski zahtjev da telefon uopšte pokrene trenutno najnoviju verziju Android operativnog sistema.

Ono što ovaj novi način čuvanja kredencijala donosi jeste da aplikacije nemaju pristup kredencijalima drugih aplikacija. Čak i ako instalirate neku malicioznu aplikaciju na svom telefonu, ta aplikacija nema pristup kredencijalima iz drugih aplikacija.

Od Oreo verzije (8.0) se može i provjeriti kako vaš telefon čuva kredencijale tako što odete u `Settings` -> `Security & Location` -> `Encryption & credentials` i provjerite `Storage type` polje.

![hardversko čuvanje kredencijala](https://i.imgur.com/aWHHdo1.png)

## 6. Antivirus i Google Play Protect (8+ verzije)

Kada me bilo ko pita da li treba da ima antivirus na Android telefonu (ili na bilo kojem telefonu uopšteno), moj odgovor je uvijek isti: ne treba.

Ukoliko aplikacije skidate samo sa službene prodavnice (Google Play Store), šanse da pokupite virus su ravne nuli (to jest postoje, ali morate da budete baš baksuzi da instalirate jednu od njih). Ukoliko instalirate aplikacije iz drugih izvora (`.apk` fajlovi na Androidu), šanse da pokupite virus rastu.

Od Android Oreo verzije, sa sistemom dobijate antivirus: Google Play Protect. Ovaj softver je do sada radio isključivo na Google-ovom serveru (kada pokušate da upload-ujete aplikaciju na Google Play Store, ta aplikacija mora da prođe Google Play Protect antivirus test), a od verzije Oreo, ovaj softver je instaliran i na samim telefonima i u pozadini skenira aplikacije koje imate instalirane. Njegov interfejs možete pronaći u `Settings` -> `Security & Location` -> `Google Play Protect` i možete vidjeti kako on izgleda na slici ispod.

![Google Play Protect interfejs](https://i.imgur.com/mNvBRzU.png)

## Sumarizacija pozitivnih stvari

Od KitKat verzije (4.4) do Oreo verzije (8.0), desilo se sljedeće:

* Znaš kada ti je telefon zadnji put update-ovan i koliko (ni)je siguran.
* Telefon je automatski enkriptovan.
* Više ne moraš pristajati na "sve ili ništa" kada su u pitanju permisije aplikacijama.
* Android telefoni automatski preuzimaju najnoviji update.
* Aplikacije ne mogu ukrasti kredencijale korišćene od strane drugih aplikacija.
* Automatski dobijaš i antivirus koji periodično skenira tvoje aplikacije.

Kada malo razmislim, apsolutno svaki prigovor koji sam imao na to kako je funkcionisala starija verzija Androida je do sada ispravljena. Pod uslovom da imaš mogućnost da kupiš telefon koji je relativno nedavno izdan, dobićeš telefon kojem zapravo možeš vjerovati.

## Vrlo bitne negativne strane

Od KitKat-a pa na vamo, Google nije ispravio jedan sigurnosni propust i dodao još jedan novi<sup>1</sup>.

### 1. Update

Za početak, moram da spomenem za sada najveći nerješivi problem za Androidov ekosistem: update. Android Oreo neće dobiti 99% telefona trenutno dostupnih na tržištu. Da bi došli od Oreo verzije, vrlo vjerovatno ćete morati kupiti novi telefon.

### 2. (Ne)sigurni načini otključavanja telefona

U novijim telefonima su dodane neke dodatne mogućnosti kako da se otključa telefon. Ovaj moj može da bude otključan na otisak prsta (loša metoda jer svuda ostavljamo otiske prsta), prepoznavanjem lica prednjom kamerom (loše jer neko može uzeti sliku vašeg oka, vidjeti video ispod) i može prepoznati kada je u rukama i automatski ostati otključan dok ga držim u ruci (loše jer neko može uzeti telefon iz moje ruke i neće se automatski zaključati).

Evo jednominutni video u kojem istraživači koriste noćne postavke na kameri + laserski printer da otključaju Samsung Galaxy S8:

<iframe width="1024" height="576" src="https://media.ccc.de/v/biometrie-s8-iris-en/oembed" frameborder="0" allowfullscreen></iframe>

## Sve u svemu...

Sumarizirajući sve do sada rečeno, Google je napravio dobar posao. Uveli su bitne sigurnosne promjene iz verzije u verziju, i došli smo do trenutka gdje, ukoliko imate Android telefon sa novijim sistemom i ne koristite glupe načine otključavanja telefona, u svojim rukama držite telefon kojem možete vjerovati. Time ne samo da su sustigli iPhone-ovu sigurnost, nego bih rekao da su je i prešli.

Ja se napokon osjećam kao da posjedujem pametni telefon i napokon mogu na njemu da držim poslovne mail-ove i da instaliram koji god program želim da instaliram, bez da kompanijama dajem pristup mom čitavom životu.

Bravo Google!

---

<sup>1</sup> Zapravo, Google je dodao i WiFi Assistant, opciju koja automatski šalje sav promet koji pravite preko javne WiFi mreže kroz Google-ove servere. Srećom, ova opcija trenutno nije dostupna nikome u našoj regiji.
