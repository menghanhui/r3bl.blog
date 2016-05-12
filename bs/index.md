---
layout: page
title: "Članci koje sam napisao na bosanskom/srpskom/hrvatskom jeziku"
comments: false
share: false
image:
  feature: abstract-1-3
---

## Na drugim sajtovima

<ul>
    <li><a href="http://www.netokracija.com/osnivac-bitcoina-satoshi-nakamoto-117842">Tko je osnivač Bitcoina Satoshi Nakamoto? Još uvijek ne znamo.</a>, objavljeno na <a href="http://www.netokracija.com/">Netokraciji</a> (05.05.2016.)</li>
    <li><a href="http://kompjuteras.com/kratka-setnja-kroz-i3-menadzer-prozora/">Kratka šetnja kroz i3 menadžer prozora</a>, objavljeno na <a href="https://kompjuteras.com/">Kompjuterašu</a> (29.04.2016.)</li>
    <li><a href="https://kompjuteras.com/umjetna-inteligencija/">Umjetna inteligencija (1. dio): Šta je i kad će?</a>, objavljeno na <a href="https://kompjuteras.com/">Kompjuterašu</a> (06.01.2016.)</li>
    <li><a href="https://kompjuteras.com/kako-resetovati-windows-sifru-koristeci-ubuntu-chntpw/">Kako resetovati Windows šifru koristeći Ubuntu (i chntpw)</a>, objavljeno na <a href="https://kompjuteras.com/">Kompjuterašu</a> (21.12.2015.)</li>
    <li><a href="http://www.mreza-mira.net/31229-moja-prica-nema-posustajanja/">Moja priča: nema posustajanja</a>, objavljeno na <a href="http://www.mreza-mira.net/">Mreži mira</a> (20.12.2015.)</li>
    <li><a href="http://kompjuteras.com/lista-20-ak-kul-sajtova-za-koje-bi-trebao-da-znas/">Lista 20-ak kul sajtova za koje bi trebao da znaš</a>, objavljeno na <a href="http://kompjuteras.com">Kompjuterašu</a> (26.09.2015.)</li>
    <li><a href="http://www.linuxzasve.com/uvod-u-github">Uvod u GitHub</a>, objavljeno na <a href="http://linuxzasve.com/">Linux za sve</a> (13.09.2015.)</li>
    <li><a href="http://kompjuteras.com/10-najcescih-zabluda-iliti-mitova-vezanih-za-linux/">10 najčešćih zabluda (iliti mitova) vezanih za Linux</a>, objavljeno na <a href="http://kompjuteras.com">Kompjuterašu</a> (24.08.2015.)</li>
    <li><a href="http://kompjuteras.com/anonimusi-njihova-istorija-ideologija-uticaj-na-svijet-oko-nas/">Anonimusi: njihova istorija, ideologija i uticaj na svijet oko nas</a>, objavljeno na <a href="http://kompjuteras.com">Kompjuterašu</a> (22.07.2015.)</li>
    <li><a href="http://kompjuteras.com/sta-je-deep-dark-web-trebam-li-se-brinuti-kako-da-se-zastitim/">Šta je deep i dark web, trebam li se brinuti i kako da se zaštitim?</a>, objavljeno na <a href="http://kompjuteras.com">Kompjuterašu</a> (15.07.2015.)</li>
    <li><a href="http://www.mi2.ba/vijesti/koga-spijunira-bih-sire-slucaj-hacking-team/">Ko koga špijunira u BiH (a i šire)? Slučaj Hacking Team</a>, objavljeno na <a href="http://www.mi2.ba/">Mi2</a> (14.07.2015.)</li>
    <li><a href="http://www.linuxzasve.com/dva-pogleda-jedna-distribucija-elementary-os-freya">Dva pogleda, jedna distribucija: elementary OS Freya</a>, objavljeno na <a href="http://linuxzasve.com/">Linux za sve</a> (04.07.2015.)</li>
    <li><a href="http://kompjuteras.com/informaticko-obrazovanje-ne-smije-da-zavisi-na-proizvodima-jedne-kompanije/">Informatičko obrazovanje ne smije da zavisi na proizvodima jedne kompanije</a>, objavljeno na <a href="http://kompjuteras.com/">Kompjuterašu</a> (10.06.2015.)</li>
    <li><a href="http://kompjuteras.com/stvari-koje-trebas-da-znas-ukoliko-planiras-da-studiras-informatiku/">Stvari koje trebaš da znaš ukoliko planiraš da studiraš informatiku</a>, objavljeno na <a href="http://kompjuteras.com/">Kompjuterašu</a> (27.05.2015.)</li>
</ul>

## Na mom blogu

<ul>
    {% for post in site.categories.bs %}
        <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%d.%m.%Y." }})</li>
    {% endfor %}
</ul>
