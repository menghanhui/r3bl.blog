---
author: Aleksandar Todorović
comments: true
date: 2016-08-10 20:00:00+01:00
layout: post
slug: najspektakularniji-pad-it-sistema-ikada
title: "Najspektakularniji pad IT sistema ikada: Australijski cenzus"
categories: bs
image:
  feature: abstract-1-3
---

Devetog avgusta, Australija je pokušala da uradi cenzus. Međutim, odlučili su da budu prva država u svijetu koja će pokušati da uradi popis stanovništva online. Ono što je uslijedilo je najspektakularniji krah IT sistema koji je svijet ikada vidio.

![census fail](https://pbs.twimg.com/media/Cpdir-SWEAA8z3a.jpg:large)

Obrađivanje cenzusa preko Interneta nije bila prva novina koji je Australija pokušala da uvede ove godine. Naime, po prvi put u australijskoj istoriji, ljudi su bili primorani da uz svoje podatke ostave njihovo pravo ime, pravu adresu stanovanja i prijašnju adresu stanovanja. Do tada, ovi podaci su bili opcioni.

Takođe, australijska vlada je donijela i odluku da se privatni podaci (imena građana, njihove adrese i slično) po prvi put u njihovoj istoriji čuvaju četiri godine nakon obavljenog cenzusa, dok je prijašnje pravilo bilo da se privatni podaci o građanima Australije čuvaju 18 mjeseci, nakon čega se isti uništavaju i na uvid ostaju dostupne samo statistike po poštanskim brojevima.

Kada kombinujemo ovo sa uvođenjem IT sistema preko kojeg će se po prvi put u svijetu obavljati cenzus, možemo lako shvatiti zašto su IT stručnjaci bili jako skeptični o ovome cenzusu. Odjednom, podaci o 21 milionu građana Australije su bili u opasnosti da budu kompromitovani. Nije teško zamisliti zašto bi rezultati cenzusa zajedno sa privatnim podacima svakog građana Australije bili fantastično dobra meta za maliciozne osobe i zašto su ovi rezultati u velikoj opasnosti da postanu najveći sigurnosni _breach_ koji je svijet ikada vidio.

Digitalizacija je predivna stvar, ali postoji nekoliko stvari koje nikada ne bi _ni smjele_ da se pokušaju digitalizovati:

* Popisi stanovništva
* Referendumi
* Glasanje na izborima

Digitalizacijom ovakvih stvari bi, u usporedbi sa prethodnom metodom, bilo nevjerovatno lako uticati na rezultate. Digitalizacijom ovakvih stvari, po prvi put u istoriji se otvara nešto što stručnjaci IT sigurnosti nazivaju centralnom tačkom neuspjeha (eng. _central point of failure_). Dok bi malverzacija tradicionalnih rezultata zahtijevalo toliku koordinaciju tolikog broja ljudi na toliko razina da se malverzacija rezultata cenzusa/referenduma/izbora u velikoj većini slučajeva jednostavno nije ni dovodila u pitanje, digitalizacijom ovakvih sistema se dešava to da osoba koja ima ili dobije kontrolu nad samo nekoliko servera može da odluči o sudbini neke države.

Australija je prva država koja je pokušala da uradi ovako nešto, i na nama je da se nadamo da će njihov neuspjeh poslužiti država širom svijeta kao primjer da ovakve stvari uopšte ne treba ni pokušavati uraditi.

Još par stvari oko ovog cenzusa koje trebate da znate prije nego što počnem da pričam o ovom spektakularnom krahu:

* Svaki građanin je (fizičkom) poštom dobio _log in_ informacije koje je trebao da iskoristi da se prijavi da bi popunio cenzus na sajtu speijalno kreiranom za potrebe cenzusa.
* Pristup formi za ispunjavanje cenzusa van granica Australije je bio u potpunosti onemogućen.
* Građani su formalno imali vremena da kasnog septembra da popune cenzus, međutim, australijski biro za statistiku (ABS) ovo nije dovoljno dobro naglasio. Veliki broj građana je mislio da to moraju da urade odma prvog dana.
* Kako bi prestrašili građane i uvjerili se da će svi građani ispuniti svoju dužnost, australijska vlada je uvela kazne od 180 australijskih dolara (oko 125 eura) po danu za one koji cenzus ne popune na vrijeme.
* Za građane koji nemaju pristup Internetu ili nisu željeli da svoje informacije unose preko Interneta, agencija za statistiku je ostavila staru "papir i olovka" metodu, međutim, ova metoda je bila opciona — građani su morali eksplicitno da zatraže popunjavanje cenzusa na papiru.

Za potrebe ovog cenzusa, otvoren je i posebni Twitter profil ([@ABSCensus](https://twitter.com/ABSCensus)) koji je stajao građanima na raspolaganju u slučaju da imaju neka pitanja o cenzusu.

Sa ovog profila je 20. jula, na izjavu jednog građana da će ovo da dovede do redovnih padova sajta, neko odgovorio:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/JennyEjlak">@JennyEjlak</a> The online Census form can handle 1,000,000 form submissions every hour. That’s twice the capacity we expect to need.</p>&mdash; Census Australia (@ABSCensus) <a href="https://twitter.com/ABSCensus/status/755588601656725505">July 20, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Ovo je bila užasno veliko upozorenje da će nešto poći po zlu. Ponavljam, Australija ima 21 milion stanovnika. Svi ti stanovnici su _morali_ da posjete ovaj sajt. Prijećeno im je novčanim kaznama u slučaju da svoju dužnost ne ispune na vrijeme. Većina ljudi je mislila da imaju samo jedan dan da ispune cenzus. Nije bio potreban genije da se shvati da su podcijenili broj posjeta za jedno 10 puta.

Ja stvarno ne razumijem šta je agencija za statistiku mislila kada je dizajnirala ovaj sistem. Šta su oni mislili, da će ukućani da se usklade u fazonu: "Ja ću popuniti ujutro prije doručka, ti obavi kad se vratiš sa posla, on će uveče dok prati olimpijadu na TV-u, a ona ionako ne spava čitave noći, tako da će ona da ispuni nekada oko 3 sata ujutro."

Jebote, logično je da će ljudi ići na to da se kurtarišu ovoga što prije. Pristupiće sajtu nekada uveče, fino popuniti i ćao. Očekivati da će najveći _spike_ u prometu biti 500 hiljada po satu u državi koja ima 21 milion stanovnika je, u najmanju ruku, idiotski.

I tako, dan cenzusa je došao, agencija je bila nespremna, ljudi su željeli da izbjegnu kaznu i da se riješe ove obaveze i pokušali su da pristupe sajtu. I tada se desilo ovo:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">We apologise for the inconvenience. The 2016 online Census form was subject to four Denial of Service attacks of varying nature &amp; severity.</p>&mdash; Census Australia (@ABSCensus) <a href="https://twitter.com/ABSCensus/status/763125821104021504">August 9, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

* * *

**Objašnjenje DDoS napada:** Zamislite da vi i par vaših prijatelja baš ne volite neku trafiku. Ono što možete da uradite da izrazite svoju nezadovoljnost jeste da odete tamo rano ujutro, stanete u red, i da svaki od vas namjerno odugovlači pružanje usluge što duže može. Dakle, stanete pred trafiku, i razmišljate pola sata o tome šta hoćete da kupite. Jednom kada više jednostavno nema smisla da odugovlačite još duže, razmijenite usluge sa radnikom/radnicom i vratite se na kraj reda da čekate dok vaši prijatelji ne urade isto što ste i vi radili, nakon čega ponavljate proces. Vi se predstavljate kao legitimni tražioci usluge, međutim svojim odugovlačenjem i ponovnim čekanjem u redu dovodite to toga da oni koji su stvarno došli do te trafike sa željom da obave neku kupovinu moraju da čekaju na kraju reda. Ti legitimni tražioci usluge sada imaju dva izbora: ili čekati pola sata u redu ili otići negdje drugdje. Poneki tražioc usluge će biti dovoljno strpljiv da sačeka i čekaće redovno u redu da bude poslužen, međutim većina će ih vrlo brzo odustati kada shvate da je čekanje neisplativo i otići negdje drugdje.

Na ovom principu funkcioniše i DDoS (skraćeno od _**D**istributed **D**enial **o**f **S**ervice_; u prevodu: distribuirano uskraćivanje usluge) napad. Njega u osnovi izvršava jedna osoba ili manja grupa osoba koja je stekla kontrolu nad relativno velikim brojem računara (nekoliko hiljada ili nekoliko desetina hiljada) raširenih po čitavom svijetu kako se ne bi moglo doći do informacije odakle je napad koordinisan. Tada, sve što osoba (ili grupa osoba) koja ima kontrolu nad tolikim brojem računara mora da uradi jeste da kaže svim tim računarima nad kojima ima kontrolu da posjećuju sajt u isto vrijeme. Ukoliko operateri sajta nisu sproveli dobru pripremu da bi ovakav napad izbjegli, događa se identična situacija kao u primjeru trafike: poneki legitiman posjetioc sajta će moći da mu pristupi, ali većina će biti neko vrijeme zaglavljena u redu, čekajući da napokon pristupe sajtu, nakon čega će odustati.

* * *

Kada su serveri koji su hostovali sajt cenzusa doživili krah pod količinom prometa, na vidjelo je došla još jedna nekompetentnost onih koji upravljaju sajtom preko kojeg se obavlja cenzus.

Naime, svaki sajt ima jednu postavku koja se naziva TTL (eng. _**t**ime **t**o **l**ive_). Ta postavka označava koliko dugo posjetioci mogu da pokušavaju da uspostave kontakt sa serverom koji služi sajt prije nego što server odbije konekciju i zatraži od posjetioca da pokušaju ponovo da se konektuju. Vrijednost ove postavke se mjeri u sekundama i po default-u, ova vrijednost je negdje između jedne i dvije minute (64 na Linux/Unix serverima, 128 na Windows serverima).

Ovo znači da će, u najgorem slučaju, posjetioc sajta pokušati da pristupi sajtu u periodu od jedne ili dvije minute. Ukoliko u tom vremenskom periodu posjetioc ne uspije da dođe do sajta, pokušaj konekcije se odbija, a korisnici dobijaju poruku da je sajtu "trebalo predugo da odgovori". Random primjer sa Google-a kako izgleda ova greška:

![took too long to respond error](https://c1.staticflickr.com/2/1580/25559978976_bccd7a3835.jpg)

Ova vrijednost na sajtu preko koje se obavljao cenzus je bila — ni manje ni više — 14400 sekundi.

Četiri jebena sata.

Dakle, korisnici su mogli da četiri sata pokušavaju da pristupe sajtu prije nego što bi im _browser_ rekao da pokušaju ponovo da se konektuju. Međutim, legitimni korisnici su najmanji dio problema koji za sobom vuče postavljanje ovoliko velike TTL vrijednosti. Postoje još dva važnija problema:

1. Neko ko pokušava da izvrši DDoS napad na sajt može četiri sata bez problema da mu pokušava pristupiti sa svakog računara koji kontroliše.
2. Ukoliko operateri servera _pokušaju_ da izvrše neke promjene u infrastrukturi tokom samog napada, trebaće _minimalno_ četiri sata da te promjene stupe na snagu, jer računari koji napadaju ovaj sajt nastavljaju da pokušavaju da se po prijašnjim konfiguracijama konektuju na server.

Zahvaljujući ovako početnikoj grešci, kada se sajt jednom našao pod DDoS napadom, operateri sajta su sami sebi skrojili sudbinu: sajt će biti nedostupan _minimalno_ četiri sata u periodu kada očekuju najveću količinu prometa.

Jednom kada su to operateri sajta napokon shvatili, na Twitter-u su objavili sljedeću poruku:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">After the fourth attack, just after 7:30pm, the ABS took the precaution of closing down the system to ensure the integrity of the data.</p>&mdash; Census Australia (@ABSCensus) <a href="https://twitter.com/ABSCensus/status/763126044622671873">August 9, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Ovo je sljedeći potez koji bi napravio samo apsolutni idiot koji pojma nema o održavanju servera. DDoS napad nema _apsolutno nikakve veze_ sa sigurnošću podataka već sačuvanih na serveru. Naprotiv, svako ko bi _pokušao_ da ukrade informacije sa njihovog sistema bi morao, kao i svi ostali, da sačeka minimalno četiri sata prije nego što bi mogao da pristupi sadržaju na njihovim serverima i istraži kako da ukrade podatke sa njega.

Dakle, nakon što su sebi iskrojili sudbinu i pobrinuli se da minimalno četiri sata niko ne može da pristupi sajtu, oni su sajt u potpunosti uklonili sa Interneta, time stavljajući "tačku na i" u svom pokušaju digitalizacije cenzusa.

Priprema za količinu prometa je bila toliko katastrofalna da nije postojalo apsolutno ništa što su mogli uraditi jednom kada je njihov sistem postao preopterećen, a odgovor operatera na ovaj problem jeste bio da sami uklone sajt sa Interneta.

I tako, ono što se u početku možda i činila kao dobra ideja u glavama onih iz agencije za statistiku, doživilo je apsolutan krah. Sve što je ostalo jeste da pokušaju kontrolu štete.

U svojoj [izjavi za javnost](http://www.abs.gov.au/AUSSTATS/abs@.nsf/dd0ca10eed681f12ca2570ce0082655d/5239447c98b47fd0ca25800b00191b1a!OpenDocument), izjavili su, između ostalog, sljedeće:

> The ABS apologises to the Australian public for inconvenience caused and reassures Australia that no data has been lost or compromised. The ABS has an unblemished record of protection of data and there has never been a breach in relation to Census data. The protection of Census data has and always will be our first priority.

Ili u prevodu:

> ABS (Australijski biro za statistiku) se izvinjava australijskog javnosti za neugodnosti i uvjerava Australiju da nije došlo do kompromisa podataka. ABS ima neokaljanu istoriju zaštite podataka i nikada nije bio sigurnosni propust vezan za podatke cenzusa. Zaštita podataka iz cenzusa je bila i uvijek će biti naš najveći prioritet.

Naravno, u pravu su, "nikada nije bio sigurnosni propust vezan za podatke cenzusa". Kao što sam naveo na početku članka, malverzacije _prije_ digitalizacije bi zahtijevale toliku koordinaciju tolikog broja ljudi na toliko razina da se malverzacija rezultata jednostavno nije ni dovodila u pitanje. Međutim, pošto je ovo bio prvi australijski (a i svjetski) pokušaj održavanja cenzusa preko Interneta, govoriti o "neokaljanoj istoriji zaštite podataka" je jednostavno glupo i ništa više od primjera kontrole štete jednom kada je sve već otišlo u kurac.

Naravno, Australijanci su smatrali da je ovo glupost i da sajt jednostavno nije bio u mogućnosti da primi legitiman promet koji je pristizao. Jedan Twitter korisnik je kontaktovao hosting kompaniju koju je koristio biro za statistiku i dobio sljedeći odgovor:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">So, I contacted Softlayer support, this was their response <a href="https://twitter.com/ABSCensus">@ABSCensus</a> <a href="https://twitter.com/hashtag/CensusFail?src=hash">#CensusFail</a> <a href="https://t.co/7N3zRqtf3u">pic.twitter.com/7N3zRqtf3u</a></p>&mdash; sortius (@sortius) <a href="https://twitter.com/sortius/status/763181521201049600">August 10, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Gdje je istina?

Vjerovatno je zapela negdje u sredini.

Sajt je definitivno bio nedostupan, neko je definitivno ispao glup odgovarajući na opravdane žalbe građana:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/ABSCensus">@ABSCensus</a> So why did you repeatedly tell people the site was working smoothly when you knew this was happening? <a href="https://t.co/P6SB2Za9RD">pic.twitter.com/P6SB2Za9RD</a></p>&mdash; Buzz Lightkeir (@keirt) <a href="https://twitter.com/keirt/status/763183133273436160">August 10, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

...nije došlo do nikakve provale u podatke, ali se australijska birokracija dokazala kao potpuno nekompetentnom za ovakav projekat, tako da krađa podataka i nema nekog smisla.

U zadnjem _update_-u do sada, biro za statistiku je naveo da će javnosti dostaviti više podataka sutra. Bliži se polako jutro, sajt je još uvijek nedostupan, a epilog ove priče nije ni na vidiku.

Nekoliko stvari koje mogu sa sigurnošću da izjavim:

* Ovo je za sada najspektakularniji slučaj pada IT sistema koji je svijet ikada doživio.
* Strahovi građana da biro za statistiku nije dovoljno kompetentan da izvrši ovako nešto je bio i više nego opravdan.
* Nadam se da će ovaj blam poslužiti kao primjer ostalim državama da ni ne pokušavaju digitalizirati ovako bitan dio demokratskog procesa.
