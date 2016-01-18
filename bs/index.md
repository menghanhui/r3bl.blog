---
layout: page
title: "Content I wrote in Bosnian/Serbian/Croatian"
comments: false
share: false
image:
  feature: abstract-1-3
---

## On other websites

<ul>
    <li><a href="https://kompjuteras.com/umjetna-inteligencija/">Umjetna inteligencija (1. dio): Šta je i kad će?</a>, published on <a href="https://kompjuteras.com/">Kompjuteraš</a> (January 6, 2016)</li>
    <li><a href="https://kompjuteras.com/kako-resetovati-windows-sifru-koristeci-ubuntu-chntpw/">Kako resetovati Windows šifru koristeći Ubuntu (i chntpw)</a>, published on <a href="https://kompjuteras.com/">Kompjuteraš</a> (December 21, 2015)</li>
    <li><a href="http://www.mreza-mira.net/31229-moja-prica-nema-posustajanja/">Moja priča: nema posustajanja</a>, published on <a href="http://www.mreza-mira.net/">Mreža mira</a> (December 20, 2015)</li>
    <li><a href="http://kompjuteras.com/lista-20-ak-kul-sajtova-za-koje-bi-trebao-da-znas/">Lista 20-ak kul sajtova za koje bi trebao da znaš</a>, published on <a href="http://kompjuteras.com">Kompjuteraš</a> (September 26, 2015)</li>
    <li><a href="http://www.linuxzasve.com/uvod-u-github">Uvod u GitHub</a>, published on <a href="http://linuxzasve.com/">Linux za sve</a> (September 13, 2015)</li>
    <li><a href="http://kompjuteras.com/10-najcescih-zabluda-iliti-mitova-vezanih-za-linux/">10 najčešćih zabluda (iliti mitova) vezanih za Linux</a>, published on <a href="http://kompjuteras.com">Kompjuteraš</a> (August 24, 2015)</li>
    <li><a href="http://kompjuteras.com/anonimusi-njihova-istorija-ideologija-uticaj-na-svijet-oko-nas/">Anonimusi: njihova istorija, ideologija i uticaj na svijet oko nas</a>, published on <a href="http://kompjuteras.com">Kompjuteraš</a> (July 22, 2015)</li>
    <li><a href="http://kompjuteras.com/sta-je-deep-dark-web-trebam-li-se-brinuti-kako-da-se-zastitim/">Šta je deep i dark web, trebam li se brinuti i kako da se zaštitim?</a>, published on <a href="http://kompjuteras.com">Kompjuteraš</a> (July 15, 2015)</li>
    <li><a href="http://www.mi2.ba/vijesti/koga-spijunira-bih-sire-slucaj-hacking-team/">Ko koga špijunira u BiH (a i šire)? Slučaj Hacking Team</a>, published on <a href="http://www.mi2.ba/">Mi2</a> (July 14, 2015)</li>
    <li><a href="http://www.linuxzasve.com/dva-pogleda-jedna-distribucija-elementary-os-freya">Dva pogleda, jedna distribucija: elementary OS Freya</a>, published on <a href="http://linuxzasve.com/">Linux za sve</a> (July 4, 2015)</li>
    <li><a href="http://kompjuteras.com/informaticko-obrazovanje-ne-smije-da-zavisi-na-proizvodima-jedne-kompanije/">Informatičko obrazovanje ne smije da zavisi na proizvodima jedne kompanije</a>, published on <a href="http://kompjuteras.com/">Kompjuteraš</a> (June 10, 2015)</li>
    <li><a href="http://kompjuteras.com/stvari-koje-trebas-da-znas-ukoliko-planiras-da-studiras-informatiku/">Stvari koje trebaš da znaš ukoliko planiraš da studiraš informatiku</a>, published on <a href="http://kompjuteras.com/">Kompjuteraš</a> (May 27, 2015)</li>
</ul>

## On my own blog

<ul>
    {% for post in site.categories.bs %}
        <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%B %d, %Y" }})</li>
    {% endfor %}
</ul>
