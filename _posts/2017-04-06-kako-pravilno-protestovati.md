---
author: Aleksandar Todorović
comments: false
date: 2017-04-06 11:30:00+01:00
layout: post-bs
slug: sigurno-protestovanje
redirect_from: /bs/kako-pravilno-protestovati/
title: "Kako sigurno protestovati: vodič za pomalo paranoične"
categories: bs
tags:
- tutorial
- technology
- advocacy
image:
  feature: abstract-1-3
---

Sa ovim studentskim protestima koji se održavaju u Srbiji, iskočio je i sajt [sigurno.org](https://sigurno.org/), koji daje neke tipove o tome kako pravilno protestovati. Tekst na tom sajtu je prepun kvalitetnih savjeta, međutim, malo su mi razbacani, tako da sam odlučio da ih nadopunim u ovom članku. Uzimam u obzir isti nivo paranoje kao i autor tog sajta dok pišem ovaj tekst.

![revolucijski alati]({{ site.url }}/images/misc/revolution-tools.jpg)

## 1. Prilagodi svoj telefon situaciji prije nego što odeš na protest.

* Android: obavezno Settings -> Security -> Encryption -> Encrypt Phone (iOS (verzija 9+) ovo ima automatski uključeno).

* Prijedlog sa Sigurno.org stoji, omogući PIN ili šifru za otključavanje telefona, osam ili više karaktera / brojeva. _Swipe pattern_ i autentikacija skeniranjem otiska prsta nije prihvatljiva za ovu situaciju i moraš mijenjati lakoću korišćenja sa poboljšanjem sigurnosti.
* Omogući automatski upload slika i snimaka na Dropbox / Google Drive / Nextcloud / šta-god (za slučaj da izgubiš pristup telefonu (tj. ukoliko ti ga policija oduzme)). Neka se slike / snimci čuvaju na internoj memoriji telefona, ne na memorijskoj kartici.
* Kupi neku VPN licencu ili iskoristi _trial_ nekog VPN provajdera koji nudi samo plaćenu opciju (moja preporuka je [Freedome](https://www.f-secure.com/en/web/home_global/freedome) ukoliko nisi vezan za Linux desktop i [Private Internet Access](https://www.privateinternetaccess.com/) ukoliko jesi).
* Izvadi SIM karticu iz telefona prije nego što odeš na protest. Dok si na protestu, sačekaj da prođete pored neke trafike ili prodavnice i kupi _prepaid_ karticu nekog drugog provajdera<sup>1</sup>. Plati je kešom (ni slučajno kreditnom karticom).

<sup>1</sup> Nažalost, svaki telefon ima fizički IMEI broj koji je dostupan mobilnim mrežama. Ne možeš se ovoga riješiti sa drugim brojem (moguće je konektovati tačke i reći da se IMEI ove kartice poklapa sa IMEI-em ove druge kartice koja je došla online sat vremena nakon što je prva diskonektovana), ali ukoliko uzmeš karticu nekog drugog provajdera, manje su šanse da kompanije dijele IMEI podatke između sebe.

## 2. Dok si na protestu...

* Internet pristup je zajebana opcija, jer bi ga trebao imati konstantno (da praviš backup svega što snimiš na protestu), ali opet, ukoliko ga aktiviraš preko mobilne mreže, izložen si tim da mobilna mreža zna gdje si. Moja preporuka bi bila da kupiš mobilni Internet na novoj prepaid kartici i da, čim ga aktiviraš, konektuješ se na VPN. Korišćenjem WiFi mreža postoji mala šansa da neko ko kontroliše veći broj WiFi mreža može da to iskoristi da bi pratio tvoje kretanje, pa bih preporučio da je WiFi kompletno isključen.
* VPN mora konstantno biti uključen, od trenutka kada dobiješ Internet pristup pa na dalje (i ovo se komplikuje korišćenjem WiFi-a, jer pri svakom prelazu na drugu WiFi mrežu potrebno je ponovo uspostaviti konekciju sa VPN-om).

## 3. Sigurna komunikacija i pretraživanje tokom samog protesta.

* Pošto si već konektovan na VPN, pretraživanje Interneta koristeći Google je sasvim prihvatljivo u zemljama regiona. Gledajući Google-ov [Transparency Report](https://www.google.com/transparencyreport/userdatarequests/countries/), iako su Makedonija i Srbija pokušale da izvuku neke informacije o Google korisnicima, nisu to uradili kako treba i Google je svaki zahtjev odbio.
* O Tor-u ni ne pomišljaj. Iako za Tor ima itekako dobrih situacija kada je njegovo korišćenje potrebno, protesti nisu jedni od njih.
* Koristi _end-to-end_ enkripciju da komuniciraš sa drugim ljudima na protestima. [Signal](https://whispersystems.org/) je preporučen. Ukoliko nisi u mogućnosti da koristiš njega, koristi WhatsApp. Ukoliko nisi u mogućnosti ni WhatsApp da koristiš, koristi [secret conversation](https://www.facebook.com/help/messenger-app/1084673321594605/?helpref=hc_fnav) opciju unutar Facebook-ovog Messenger-a kao zadnju opciju. Kloni se što dalje od SMS poruka i telefonskih poziva. Trivijalno je lako doći do sadržaja tih poruka i garantujem da policija ima [stingray uređaje](https://www.aclu.org/issues/privacy-technology/surveillance-technologies/stingray-tracking-devices)<sup>2</sup>.

<sup>2</sup> Stingray uređaji su uređaji koji se predstavljaju kao mobilni tornjevi, sa ciljem da zavaraju tvoj telefon da se konektuje na njega i preko njega odvija komunikaciju. Jednom uključen, Stingray uređaj dobija pristup svakoj SMS poruci u okruženju. Telefonski pozivi su na neki način enkriptovani, međutim ta enkripcija je trivijalna za probiti.

## 4. Korišćenje društvenih mreža tokom protesta.

* Uopšteno, nije preporučljivo. Barem ne tokom protesta na računima koji si direktno vezani sa tvojim imenom i prezimenom.
* Geolokacija na tweet-ovima i Facebook statusima je početnička greška, nemoj je napraviti.
* Budi siguran da imaš dvo-faktorsku autentikaciju. Sigurnosni ključ (tipa [Yubikey](https://www.yubico.com/)) je preferiran. [Google Authenticator](https://support.google.com/accounts/answer/1066447?hl=en) je drugi u nizu. SMS verifikacija nije dopuštena (zbog Stingray uređaja iz prošlog savjeta), međutim, bolja je nego nikakva dvo-faktorska authentikacija.

## 5. Sigurno ponašanje tokom protesta.

Potpisujem svaku riječ iz savjeta broj 4, 5, 6, 7 i 8 sa [Sigurno.org](https://sigurno.org/). Vrlo dobro su smišljeni i razrađeni.

Što se tiče kamere, preporučujem snimanje što je više moguće stvari i njihov automatski upload na cloud servis. Nakon što ti je pristup sirovim snimcima dostupan i u slučaju da izgubiš pristup svome telefonu, posluži se savjetima iz savjeta broj 9 prije upload-a na društvene mreže. Ukratko:

* Isključi ili izbriši geolokacijske podatke.
* Koristi [ObscuraCam](https://guardianproject.info/apps/obscuracam/) na Androidu ili sličan program na drugim platformama da maskiraš lica drugih koji učestvuju u protestu.
* Razmisli o tome trebaš li ukloniti ton iz videa.

## Disclaimer

Iako sam u naslovu članka iskoristio izraz "za pomalo paranoične", ne smatram da je to negativna osobina. Što se paranoje tiče, tvoj stepen paranoje treba uvijek da bude malo veći nego što je realna prijetnja. Prevelika paranoja dovodi do toga da gubiš vrijeme pokušavajući da ostaneš siguran protiv nerealne prijetnje. Premala paranoja znači da si pao na testu sigurnosti. Malo veća paranoja u odnosu na realnu prijetnju znači da si korak ispred onih koji te žele ugroziti sigurnost.
