---
author: Aleksandar Todorović
comments: true
date: 2015-07-01 22:40:00+01:00
layout: post
slug: kako-rade-browseri
title: "Kako rade browseri: Šta se dešava iza koda modernih web browsera"
categories: bs
tags:
image:
  feature: abstract-1-3
description:
---

## Uvod

Web browseri su najšire korišćeni tipovi softvera. U ovom tekstu, objasnićemo kako tačno funckionišu iza zavjesa. Vidjećemo šta se tačno dešava od trenutka kada ukucate `google.com` do trenutka kada vidite Google-ovu početnu stranicu na vašem ekranu.

## Browseri o kojima ćemo da govorimo

Postoji pet glavnih browsera korišćenih na desktop uređajima danas: Chrome, Internet Explorer, Firefox, Safari i Opera. Na mobilnim uređajima, najprošireniji su Android Browser, iPhone, Opera Mini i Opera Mobile, UC Browser, Nokia S40/S60 browseri i Chrome--od koji su svi, osim Opera browsera, bazirani na WebKit-u. Daćemo primjere iz Firefox-a, Chrome-a i Safari-ja (koji je djelomično open source softver). Prema [StatCounter statistici](http://gs.statcounter.com/) (mjerenje za jun 2013. godine) Chrome, Firefox i Safari zajedno dijele oko 71% globalnog korišćenja desktop browsera. Na mobilnim uređajima, Android Browser, iPhone i Chrome dijele oko 54% korišćenja na globalnoj skali.

## Glavna funkcionalnost browsera

Glavna funkcionalnost browsera jeste da prezentuju web sadržaj koji vi izaberete, tako što traže pristup od servera i prikazuju ga u prozoru browsera. Resurs je obično HTML dokument, ali isto tako može da bude i PDF, slika ili neki drugi tip sadržaja. Lokaciju resursa bira korisnik tako što kuca URI (eng. _Uniform Resource Identifier_).

Na ovaj način, browser sakuplja i prikazuje HTML datoteke naglašene u HTML i CSS specifikacijama. Ove specifikacije se održavaju od strane W3C (eng. _World Wide Web Consortium_) organizacije, organizacije koja se bavi web standardima. Godinama su browseri bili kompatibilni sa samo jednim dijelom specifikacija i na osnovu tog dijela kreirali sopstvene ekstenzije. Ovo je dovelo do ozbiljne nekompatibilnosti između autora web sadržaja. Danas se većina browsera manje-više prilagođava specifikacijama.

Korisnički interfejsi browsera dijele mnogo toga sličnog. Neki od najčešće viđenih elemenata su:

* Adresna linija gdje se unosi URI
* Tasteri za naprijed i nazad
* Opcije za bookmark-ovanje sadržaja
* Refreš i stop tasteri za refrešovanje ili stopiranje učitavanja trenutnog dokumenta
* Home taster koji vas vodi na vašu početnu stranicu

Ono što je čudno jeste što korisnički interfejs nije opisan ni u jednoj formalnoj specifikaciji. Nastao je iz dobrih iskustava sakupljenih tokom godina i tako što su browseri kopirali jedni druge. HTML5 specifikacija ne definiše elemente korisničkog interfejsa koje browser mora da ima, ali navodi nekoliko najčešće korišćenih elemenata. Među njima su adresna linija, linija statusa i linija sa alatima. Postoje, naravno, funkcionalnosti specifične za neki browser kao što je Firefox-ov menadžer za preuzimanja.

Glavne komponente browsera su (slika 1.1):

1. **Korisnički interfejs**: uključuje adresnu liniju, naprijed i nazad tastere, meni za bookmark-ove i tako dalje. Ovdje spada svaki dio prikaza browsera osim prozora gdje se prikazuje tražena stranica.
2. **Browser engine**: upravlja akcijama između korisničkog interfejsa i renderning engine-a.
3. **Rendering engine**: zadužan za prikazivanje traženog sadržaja. Kao primjer, ukoliko je zatražen HTML sadržaj, rendering engine obrađuje HTML i CSS, te prikazuje obrađeni rezultat na ekranu.
4. **Umrežavanje**: za mrežne funkcije kao što su HTML zahtjevi, koristeći različite implementacije za različite platforme iza interfejsa koji nije zavisan za platformu.
5. **Backend korisničkog interfejsa**: korišćen za crtanje osnovnih elemenata kao što su combo kutije i prozori. Ovaj backend prikazuje generički interfejs koji nije specifičan za platformu. Iza njega se kriju metode sistemskog korisničkog interfejsa.
6. **Interpreter JavaScript-a**: korišćen za obradu i izvršavanje JavaScript koda.
7. **Spremač sadržaja**: moguće je da browser treba da sačuva razne tipove podataka lokalno kao što su kolačići.
