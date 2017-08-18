---
author: Aleksandar Todorović
comments: true
date: 2017-08-18 12:00:00+02:00
layout: post-bs
slug: daily-stormer-ukratko
title: "The Daily Stormer: Šta je, šta mu se desilo, i moguće posljedice svega ovoga"
categories: bs
tags:
- blogging
- personal
image:
  feature: abstract-1-3
---

The Daily Stormer je sajt koji promoviše neo-nacizam. Nakon nedavnog sranja u Charlestonville-u, kompanije su odlučile da mu onemoguće uslugu. Šta to znači za budućnost Interneta?

![baner The Daily Stormer-a](http://i.imgur.com/EHAqAOJ.png)

## Šta je ovaj sajt i zašto je kontroverzan

Ovaj sajt je učestvovao u organizaciji Ujedinimo desnicu mitinga (eng. [_Unite the Right Rally_](https://en.wikipedia.org/wiki/Unite_the_Right_rally)) koji je okupio solidan broj pripadnika krajnje desnice u gradu Charlestonville-u u saveznoj državi Virdžiniji, i solidan broj antifašista u kontramitingu. Stvari su se malo zagrijale, pa se jedna osoba spucala autom u antifašiste. Smrtno je stradala jedna osoba, i povrijeđeno 19<sup>1</sup>.

The Daily Stormer je godinama promovisao krajnju desnicu, međutim vijest o smrtno stradaloj osobi<sup>2</sup> je bila ta kap koja je prelila čašu:

![Naslov vijesti o smrti kontramitingašice](http://i.imgur.com/wB61iL0.png)

Do tog trenutka, The Daily Stormer je godinama koristio `dailystormer.com` domenu i hosting od strane GoDaddy-a. Onda se desilo sljedeće:

* GoDaddy im je rekao da su prekršili pravila korišćenja njihovog servisa i dali im 24 sata da nađu drugog provajdera i naprave tranziciju.
* Facebook i Discord su na svojim platformama zabranili linkove koji vode prema `dailystormer.com` domeni.
* Vlasnici sajta su pokušali da koriste Google Domains, i to je trajalo nekoliko sati prije nego što im je Google otkazao uslugu. Google je stavio `dailystormer.com` kao suspendovanu domenu prilikom otkazivanja usluge, što znači da su vlasnici sajta potpuno izgubili kontrolu nad domenom. Google ju je preuzeo i učinio je nedostupnom.
* Google je usput i ugasio YouTube kanal vezan za sajt.
* Vlasnici sajta su se privremeno prebacili na Tor mrežu i koristili `.onion` domenu.
* Vlasnici sajta su kupili `dailystormer.ru` domenu i prebacili se sa `.onion` domene na `.ru` domenu. `.onion` domena je nakon toga prikazivala kratak tekst koji je rekao da su na `dailystormer.ru` domeni i da će se vratiti na `.onion` ukoliko bude potrebe.  
* Sajt je koristio Cloudflare-ove usluge (kao DNS<sup>3</sup> provajdera i kao DDoS zaštitu). Cloudflare im je ugasio račun, učinivši njihovu `.ru` domenu nedostupnom (jer nije vodila ni na kakvu IP adresu servera).
* Ruska vlada je zatražila od registratora domena da oduzme `.ru` domenu od vlasnika sajta, što se i dogodilo.
* Vlasnici sajta su vratili sajt na `.onion` domenu.

Uh, kao što možete da vidite, mnogo toga se izdešavalo u zadnjih sedam dana sa ovim sajtom. Krenimo redom.

## Američke kompanije imaju pravo da onemoguće uslugu

Američke kompanije imaju zakonsko pravo da odbiju pružanje usluge kome god žele, sve dok odbijanje usluge nije urađeno pod sljedećim osnovama ([izvor](http://www.phrc.pa.gov/File-A-Complaint/Types-of-Complaints/Pages/DenialofServicesandFacilities.aspx)):

> Da bi se odbijanje usluge smatralo ilegalnom diskriminacijom, ono mora biti bazirano na nečijoj rasi, boji tena, seksualnoj orijentaciji, porijeklu, nacionalnoj pripadnosti, religijskoj pripadnosti, hendikepu ili invalidnosti, korišćenju životinja vodiča osobama sa invalidnosti, ili osobama koje imaju ličnu vezu sa osobom sa invalidnošću.

Logično, neo-nacizam ne spada niti u jednu od ovih skupina, tako da su GoDaddy, Google, Facebook, Discord i Cloudflare imali potpunu zakonsku mogućnost da im onemoguće da budu njihovi korisnici.

## Zašto je ovaj sajt uopšte dozvoljen?

Ukratko: prvi amandman američkog ustava, koji kaže da vlada nema pravo da krivično goni nekoga na osnovu izrečenih izjava. Ovo je za stanovnike SAD-a gotovo krucijalan amandman i jedan od najbitnijih razloga zašto svoju državu smatraju "slobodnom zemljom".

"Govor mržnje" ne postoji u američkom zakonu. Bez obzira šta izgovorio, bez obzira šta podržavao, država te ne može krivično goniti zbog toga (sve dok to sve ostane na riječima). U praksi, to znači da možeš promovisati ISIS, organizovati skup podrške nacizmu, reći da su Jevreji krivi za svako zlo na svijetu... i ne biti krivično gonjen za to, jer tvoju slobodu govora štiti prvi amandman.

Dakle, javno govorenje kako "Hitler nije uradio ništa pogrešno" tokom skupa u Charlestonville-u i vođenje ovog sajta je oboje u potpunosti legalno unutar SAD-a, zahvaljujući upravo tom prvom amandmanu<sup>4</sup>.

## Oduzimanje kontrole nad domenom

Da bi neko pokrenuo sajt, mora imati domenu (logično). Da bi kupio domenu, mora je kupiti od registratora domena. U zavisnosti od domene (`.com` i `.me` nemaju ista pravila) i registratora domene (Namecheap i GoDaddy nemaju ista pravila), može doći do bezbroj situacija u kojima neko preuzme kontrolu nad nekom domenom.

U praksi, vjerovatno svi znate da se tokom svojih 13 godina postojanja The Pirate Bay selio jedno 20 puta sa jedne domene na drugu. Istraživači malware-a redovno sarađuju sa registratorima da preuzmu kontrole nad domenama koje služe kao komandni centar za neki malware. Microsoft je prošli mjesec koristio zakon o zaštitnom zakonu (eng. _trademark_) da [preuzme kontrolu](https://arstechnica.com/tech-policy/2017/07/microsoft-targets-fancy-bears-domains-in-trademark-lawsuit/) nad domenama koje je kontrolisala APT28 (grupa malicioznih hakera koja je gotovo sigurno finansirana od strane ruske vlade). Primjera je bezbroj, tako da ću stati ovdje.

"Kupovanje domena" je praktički servis za iznajmljivanje. Autorizovane kompanije iznajmljuju domene za fiksan vremenski period (najčešće jednu godinu), međutim, one i dalje imaju pravo da kontrolišu te domene za slučaj da osoba koja ih je iznajmila na neki način krši pravila korišćenja te kompanije. Dodatno, kada su u pitanju domene neke države (tipa `.ru`, `.us`, `.rs`, `.ba`, `.hr`, `.me`), vlade imaju pravo zatražiti od kompanije da onemoguće pristup nekoj domeni (što je ruska vlada i [uradila](https://rkn.gov.ru/news/rsoc/news48958.htm) u ovome slučaju).

## Subjektivna mišljenja

Ovime sam završio činjeničnu sekciju ovog članka, i sada je vrijeme za moja subjektivna mišljenja.

Nakon svega ovoga, organizacije koje se bore za prava na Internetu (tipa [Electronic Frontier Foundation (EFF)](https://www.eff.org/) i [American Civil Liberties Union (ACLU)](https://www.aclu.org/)) i obični građani zainteresovani za slobodu govora na Internetu (kao što sam ja) smo se našli u dilemi. Iako se gotovo čitav svijet može složiti da je The Daily Stormer sajt sa čijim mišljenjima i metodom se ne slažemo, da li treba da postoji?

Sa jedne strane, ne krši niti jedan zakon države iz koje je. Sa druge strane, promoviše mržnju i nacizam.

Lično, smatram da postoji jedna lekcija koju smo trebali izvući kada je Trump postao predsjednik SAD-a. Većina javne sfere se slagala sa time da Trump ne bi trebao da bude predsjednik. Ismijavali smo ga, izrugivali, i odbijali da čujemo drugu stranu i njihove argumente. Time smo potiskivali dio američke populacije, i taj dio američke populacije je postajao sve sigurniji i sigurniji da žele da glasaju za Trump-a, te je on na kraju i pobijedio.

Ova akcija protiv The Daily Stormer-a može da dovede do istih posljedica. Vlasnici sajta nisu prekršili zakon, međutim bili su primorani da mijenjaju domene i trenutno se bore protiv kompanija koje ne žele da taj sajt postoji na njihovoj platformi. Postavljajući se u kožu neke osobe koja je na granici da postane nacista, ova akcija protiv The Daily Stormer-a bi me definitivno razljutila i učinila moja uvjerenja da je nacizam dobra ideja još jačim.

Sa druge strane, da je ovaj sajt ostao netaknut, da je neko ko je na granici nacizma saznao za mišljenja neo-nacista jednostavno posjećujući `dailystormer.com`, i da je vidio da je osoba iz kontramitinga koja je smrtno stradala obilježena kao "debela 32-godišnja kurva bez djece", možda bi se ta osoba predomislila oko svoje potencijalne afilijacije sa neo-nacizmom. Da mi, kao obični Internet korisnici, možemo da linkujemo prema toj vijesti na Facebook-u, možda bi imali više koristi od toga (pod korist smatram osobe koje su se predomislile oko afilijacije sa neo-nacizmom) nego štete (pod štetom smatram osobe koje su zahvaljujući tom članku postali neo-nacisti).

Zbog toga smatram da je ova akcija protiv The Daily Stormer-a ektremno loša ideja. EFF se [slaže sa mojim zaključkom](https://www.eff.org/deeplinks/2017/08/fighting-neo-nazis-future-free-expression) [disklejmer: tokom ove godine sam donirao jedno 100 dolara EFF-u jer podržavam njihov rad]. ACLU nije javno iznijeo svoje mišljenje, međutim ima neslaganja između glavne ACLU organizacije (koja, navodno, smatra da su akcije protiv The Daily Stormer-a loša ideja) i njenih lokalnih jedinica (koje, navodno, razmišljaju o tome da prekinu veze sa glavnom ACLU organizacijom baš zbog ovoga) [disklejmer: tokom ove godine sam donirao jedno 20ak dolara ACLU-u jer podržavam njihov rad].

EFF je do svojeg zaključka došao zbog malo drugačijeg razloga:

> Svi pravedni ljudi moraju da ustanu protiv agresije i nasilja iz mržnje, koje se čini kao da se proširuje našom državom. Ali, takođe, moramo da se suočimo sa time da će bilo koja akcija koja se danas koristi protiv neo-nacista na Internetu uskoro biti iskorišćena i protiv drugih, uključujući i one sa čijim mišljenjima se slažemo.

Osnivač Cloudflare-a (Matthew Prince) je u [email-u](http://gizmodo.com/cloudflare-ceo-on-terminating-service-to-neo-nazi-site-1797915295) kojeg je poslao svojim zaposlenicima, između ostalog, izjavio sljedeće:

> Bukvalno, probudio sam se loše raspoložen i donijeo odluku da nekome ne bi trebalo dopustiti da bude na Internetu. Niko ne bi trebao da ima tu moć.

Naravno, niti jedna od ovih kompanija (pa tako ni Cloudflare) zapravo nema tu moć da _bukvalno_ ukloni nekoga sa Interneta. Međutim, kompanije su im priredile borbu za to da ostanu na Internetu. Ovo bih više nazvao _Denial of Service_ napadom (akcije kompanija su dovele do privremene nedostupnosti sajtu) nego uklanjanjem sa Interneta (što dokazuje to što je The Daily Stormer u trenutku pisanja ovoga ponovo online, ponovo na `.onion` domeni).

Dakle, sa moje perspektive: ovo što su kompanije uradile je definitivno loša vijest. I za budućnost Interneta, i za borbu protiv širenja nacizma.

---

<sup>1</sup> Broj smrtno stradalih povezanih sa tim protestom je zapravo tri. Dva policajca su poginula u padu helikoptera koji je tu bio da prati proteste.

<sup>2</sup> Ukoliko vam se čita ova ogavština od vijesti, to možete uraditi [ovdje](https://web.archive.org/web/20170814221942/https://www.dailystormer.com/heather-heyer-woman-killed-in-road-rage-incident-was-a-fat-childless-32-year-old-slut/). Ja lično nisam smogao snage da ga pročitam u cjelosti.

<sup>3</sup> DNS je protokol koji kaže da se iza `r3bl.me` sajta krije IP adresa `94.176.239.57`.

<sup>4</sup> Vrijedno napomenuti: prvi amandman se odnosi isključivo na krivično gonjenje. Ono ne znači, na primjer, da te organizatori nekog skupa ne mogu izbaciti sa privatnog skupa zbog svog govora, ili da te Internet zajednice ne mogu banovati zbog svog govora. Vidi [ovaj xkcd](https://xkcd.com/1357/).
