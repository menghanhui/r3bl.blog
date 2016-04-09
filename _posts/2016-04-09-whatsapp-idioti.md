---
author: Aleksandar Todorović
comments: true
date: 2016-04-09 22:50:00+02:00
layout: post-bs
slug: whatsapp-idioti
title: "Ne, idioti, WhatsApp vas ne čini sigurnim"
categories: bs
tags:
- blogging
- personal
- security
- encryption
image:
  feature: abstract-1-3
---

Stvarno mi nije padalo na pamet posvećivati se ovoj temi, ali kada vidim da sve više i više ljudi u zadnjih X dana sponzoriše WhatsApp kao "sigurnu platformu", nešto u meni umre. Tako da, u ovom postu, želim da vam objasnim zašto WhatsApp nije siguran, iako je enkriptovan.

![whatsapp](https://blog.kaspersky.com/files/2016/04/whatsapp-encryption-featured.jpg)

## WhatsApp u prošlosti

WhatsApp je i prije nego što je izašao sa ovom velikom viješću imao implementovanu enkripciju. Svi razgovori su se vodili preko HTTPS protokola, tako da od trenutka kada vi pošaljete poruku, ona ide do servera enkriptovana, na serveru enkripcija ne postoji, zatim se šalje nazad do primaoca enkriptovana.

Onda je WhatsApp počeo da sarađuje sa [Open Whisper Systems](https://whispersystems.org/). To je jedna od najrespektabilnijih kompanija na polju sigurnosti koja nam je podarila RedPhone (za enkripciju poziva) i TextSecure (za enkripciju poruka), i kasnije ih objedinila u [Signal](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms), aplikaciju koja je do dana današnjeg najviše korišćena respektabilna aplikacija sa polja sigurnosti, mada i ona ima svoje mane.

Kada je Open Whisper Systems počeo da sarađuje sa WhatsApp-om, WhatsApp je počeo da implementuje _end-to-end_ enkripciju. Prvo je funkcionisala samo ukoliko oba učesnika koriste Android uređaje. Ukoliko enkripcija funkcioniše samo u određenim slučajevima, to znači da kompanija ima neki prekidač koji po potrebi pali ili gasi da uključi enkripciju. Ukoliko kompanija ima neki prekidač koji pali ili gasi da bi enkriptovala nešto, ta enkripcija ima ogromnu manu.

Danas, to više ne važi jer je enkripcija od prije nekih 5-10 dana omogućena za svaki uređaj i više ne zavisi od toga kakav uređaj ljudi koriste. Međutim, sama činjenica da je kompanija nekada u prošlosti imala taj prekidač ne izvlači baš osmjeh na lice ekspertima za sigurnost.

## Razlika između Signal-a i WhatsApp-a

Za razliku od WhatsApp-a, svaki klijent za Signal je open source (od [desktop klijenta](https://github.com/WhisperSystems/Signal-Desktop), preko [iOS klijenta](https://github.com/WhisperSystems/Signal-iOS), do [Android klijenta](https://github.com/WhisperSystems/Signal-Android)). Kod WhatsApp-a, niti jedan klijent nije otvoren, što nas dovodi do sljedećeg problema.

## Ukoliko je kod zatvoren, izbjegavajte proizvod

Iako nije tačno da je svaki enkripcijski proizvod koji je open source automatski siguran, činjenica da je kod dostupan je prva stavka potrebna da bi se svi mogli uvjeriti da je proizvod zaista siguran. Bez ove stavke, sve drugo pada u vodu.

Hajde ovako da objasnim. Recimo da je WhatsApp napravio neki _update_ u kojem se hvalio da je uključio enkripciju, ali je u stvarnosti nije uključio. Ne kažem da je WhatsApp ovo uradio, ali zamislimo da jeste na sekundu. Ko bi, osim samog WhatsApp-a, mogao da garantuje da je kompanija stvarno ovo uradila? Odgovor: niko. Jer niko osim kompanije nema pristup kodu WhatsApp-ovih aplikacija.

Sada zamislimo da NSA, FBI, CIA ili neki drugi sigurnosni kurac dođe do WhatsApp-a i natjera ih da tu istu enkripciju ugase. Uz taj zahtjev od suda stiže i takozvani [_gag order_](https://en.wikipedia.org/wiki/Gag_order) koji zabranjuje kompaniji da na bilo koji način obavijesti svoje korisnike ko im je prišao i šta je od njih zatražio. Vama dolazi normalni _update_ koji tu enkripciju isključuje. Vi toga niste svjesni i i dalje mislite da pričate enkriptovano. Niko ne primjećuje razliku.

Međutim, recimo da živimo u savršenom svijetu u kojem se ovo nikada neće desiti... iako ne živimo i iako se baš ovo prije dvije godine dogodilo [Lavabitu](http://lavabit.com/), email provajderu kojeg je koristio Edward Snowden. U ovom slučaju, Lavabit je dobro postupio i bio je spremniji da ugasi svoj servis nego da laže svoje korisnike o tome kako je njegov servis i dalje siguran dok NSA ima pristup njihovom enkripcijskom ključu, te ga je i ugasio.

Kada se ta ista situacija desi nekoj većoj kompaniji koja posluje solidno i ima veliki broj zaposlenih — na primjer nekome kao što je [reddit](https://www.reddit.com/) — gašenje servisa teško da će se dogoditi.

### Zašto sam spomenuo reddit?

reddit sam spomenuo zato što su oni nedavno javnosti javili da im je prišla neka državna agencija i dostavila im već spomenuti _gag order_. Naravno, da je reddit jednostavno rekao da se to dogodilo imao bi pravne posljedice. Umjesto toga, reddit je u svom izvještaju o transparentnosti za godinu 2014. [ubacio](https://www.reddit.com/wiki/transparency/2014#wiki_government_content_removal_requests) jednu rečenicu koja glasi ovako:

> reddit nije primio nikakav zahtjev od federalne [vlade SAD-a] ili državne vlade [ovdje se pod "državnom vladom" smatra vlada države Kalifornije] za uklanjanje sadržaja u toku 2014. godine.

Kada reddit ovu istu rečenicu nije ponovio u [izvještaju o transparentnosti za 2015. godinu](https://www.reddit.com/wiki/transparency/2015), javnost je bila svjesna da je reddit takav zahtjev primio bez da je iko iz reddit-a to konkretno rekao javnosti.

Vlada ih preko _gag order-a_ može natjerati da ne podijele istinu sa svojim korisnicima, ali ih ne može natjerati da lažu svoje korisnike tako što bi ponovili ovu rečenicu. Slučaj zatvoren.

## WhatsApp vas ne čini sigurnim ukoliko ne uradite i sljedeće

WhatsApp sada ima end-to-end enkripciju, što znači da vi kada šaljete poruku, ona se prvo enkriptuje, šalje se enkriptovana do WhatsApp-ovih servera koristeći HTTPS, dolazi do servera, server nema ključ da je dekriptuje i nema pojma šta ste u poruci napisali, već je enkriptovanu šalje do primaoca preko još jednog enkripcijskog (HTTPS) sloja, i jednom kada poruka dođe do primaoca, on istu dekriptuje i čita.

Međutim, sve ovo pada u vodu kada neko ima pristup vašem uređaju. Na primjer:

1. Kada izgubite vaš uređaj, a niste uključili enkripciju čitavog diska.
2. Kada [FBI provali u vaš iPhone](http://www.foxnews.com/tech/2016/03/29/fbi-breaks-into-san-bernardino-gunmans-iphone-without-apples-help-ending-court-case.html).
3. Kada imate malicioznu aplikaciju (čitaj: virus) na svom telefonu.

Ukoliko ispunjavate jedan od ova tri kriteriuma, end-to-end enkripcija je beskorisna jer poruke nisu enkriptovane unutar vašeg samog uređaja. Onaj ko ima pristup vašem uređaju, ima pristup i vašim porukama. Čitava ideja o enkripciji u tranzitu pada u vodu.

Sada, recimo da ne ispunjavate niti jedan od ova tri kriterijuma i da je vaš uređaj u vašim rukama i niko drugi mu nema pristup. Dolazimo do sljedećih stavki za koje morate da se pobrinete:

1. Brišete poruke sa svog telefona.
2. Ugasite backup svoje chat istorije.
3. Pazite da vam niko ne gleda iza leđa.

Prva od ovih stavki vas uvjerava da i ukoliko neko u budućnosti bude imao pristup vašem uređaju, do poruka neće moći da dođe jer su poruke izbrisane. I dok neke aplikacije kao što su Telegram poruke poslije određenog vremenskog perioda brišu po defaultu, WhatsApp to ne radi, već to morate ručno da radite.

Druga od ovih stavki. Čak i da niko nema pristup vašem uređaju, čak i da redovno brišete svoje poruke, sve to pada u vodu ukoliko vršite backup vaših poruka u cloud-u. Ovo nudi i Apple, i Android, i Windows, i ko sve ne. Poruke se na serveru sa vaših uređaja ne backup-uju enkriptovane na server, tako da ukoliko imate backup uključen, sve ostaje sačuvano u "cloud-u" (takođe poznatom i kao nečiji drugi računar). Ne-enkriptovano. Jedan poziv državnog organa kompaniji i vaše poruke se dijele sa njima.

Da se vratimo na Apple vs. FBI slučaj. Iako je Apple odbio da sarađuje sa FBI-om i da im pomogne da provale u iPhone koji je koristio terorista tokom napada u San Bernandinu, Apple im jeste dostavio backup koji je imao u svojim serverima, od kojih je najnoviji bio mjesec i po star. Dakle, sva sigurnost iPhone uređaja je pala u vodu onda kada je napadač uradio backup na Apple-ovim serverima.

Treća od ovih stavki je sasvim očita. Ukoliko pišete poruke tako da se vide iz sigurnosne kamere u nekom kafiću, ili ako neko gleda šta pišete iza vaših leđa (takozvani [_shoulder surfing_](https://en.wikipedia.org/wiki/Shoulder_surfing_%28computer_security%29)), svaki vid enkripcije pada u vodu.

Čak i da se _svih_ od ovih stavki koje sam do sada naveo poštujete, još uvijek vam ostaje jedno veliko pitanje.

## Da li osoba sa kojom komunicirate poštuje sve ovo?

Možete vi da se pobrinete da sve ovo poštujete koliko god hoćete, ali ako osoba sa kojom komunicirate ne poštuje kompletno jednake zahtjeve, sve što vi radite pada u vodu jer je osoba sa kojom komunicirate ranjiva.

## Zaključak

_End-to-end_ enkripcija je dobra, međutim ukoliko je koristite, ispunjavate tek jedan od ogromne liste zahtjeva koje trebate da ispunite da biste bili sigurni. Iako WhatsApp tvrdi da ima end-to-end enkripciju, niko osim samog WhatsApp-a to ne može da garantuje zato što im je kod zatvoren.

Ne kažem da je WhatsApp loš. Naprotiv, ovo je jedan od glavnih koraka koje WhatsApp može da napravi u pravom smjeru. Međutim, to što ga koristite ne znači da ste automatski sigurni ništa više nego što ste sigurni ukoliko imate nož u džepu dok se šetate sumnjivim ulicama nekog velikog grada. Da, tehnički je u vašem džepu i tehnički ga možete upotrijebiti ukoliko vas neko napadne, međutim beskoristan je ukoliko neko uperi pištolj u vas ili ukoliko vam ga jednostavno oduzme.

Dakle, ukoliko koristite WhatsApp, ispunili ste jedan od zahtjeva i da, na nekoj velikoj skali samo korišćenje WhatsApp-a vas čini malo sigurnijim nego kada koristite Facebook, Skype ili Viber za vašu komunikaciju, ali daleko ste od potpune sigurnosti. Zato je vrijeme da se prestanete praviti da je samo njegovo korišćenje jednako apsolutnoj sigurnosti. Nije.
