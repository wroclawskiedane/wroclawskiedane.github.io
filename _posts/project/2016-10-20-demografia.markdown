---
layout: project
title:  "Demografia Wrocławia 2014"
date:   2014-04-25 16:54:46
author: Marcel Newman
categories:
- project
img: demografia.jpg
tagged: Demografia Wrocławia 2014 wg. rejonów BREC
client: GUS, Geoportal Wrocław
website: https://niedakh.carto.com/tables/demografia_wroclawia_2014_wg_rejonow_brec_2011/public/map
---

Bardzo często istnieje potrzeba zestawienia jakiegoś zjawiska we Wrocławiu z danymi o tym, ilu ludzi mieszka na danym obszarze. Dane demograficzne można pobrać z systemu informacji przestrzennej Wrocławia — <a href="http://geoportal.wroclaw.pl/www/mapa-demografia.shtml" data-href="http://geoportal.wroclaw.pl/www/mapa-demografia.shtml">mapy demograficznej</a>.

Znajdziemy tam 579 obszarów, do każdego przypisana populacja z podziałem na wiek. Można te dane dość łatwo zaznaczyć, ułożyć w tabelę i wyeksportować jako CSV. Niestety, nie da się wyeksportować w wygodny sposób danych geograficznych o obszarach. Znamy jedynie numery rejonów statystycznych GUS do których są przyporządkowane. Rejony statystyczne pochodzą z systemu <em>BREC </em>rejestru <a href="http://bip.stat.gov.pl/dzialalnosc-statystyki-publicznej/rejestr-teryt/zakres-rejestru-teryt/" data-href="http://bip.stat.gov.pl/dzialalnosc-statystyki-publicznej/rejestr-teryt/zakres-rejestru-teryt/"><em>TERYT</em></a> zebranego przez <em>GUS</em>. Ostatni raz system ten był aktualizowany w 2011 roku.

Dane z systemu <em>BREC</em> dostępne są przez portal realizujący europejską dyrektywę <a href="http://www.akademiainspire.pl/dyrektywa-inspire" data-href="http://www.akademiainspire.pl/dyrektywa-inspire"><em>INSPIRE</em></a> dot. danych GIS. Link do archiwum ZIP zawierającym shapefiles (SHP) z rejonami statystycznymi systemu <em>BREC</em> w projekcji EPSG:2180 znajdziecie <a href="http://geo.stat.gov.pl/atom_web-0.1.0/download/?fileId=006840865be32b80182bccd2806d8d3d&amp;name=PD_BREC_2011_REJ.zip" data-href="http://geo.stat.gov.pl/atom_web-0.1.0/download/?fileId=006840865be32b80182bccd2806d8d3d&amp;name=PD_BREC_2011_REJ.zip">tutaj</a>.

<strong>Naszym celem jest posiadanie jednolitego zbioru zawierającego zarówno obszary jak i dane demograficzne. Taki zbiór danych, w projekcji EPSG:4326 udostępniam w serwisie <a href="https://niedakh.cartodb.com/tables/demografia_wroclawia_2014_wg_rejonow_brec_2011">CartoDB</a> jak również w postaci noty publikacyjnej w portalu Research Gate: <a href="https://www.researchgate.net/publication/291820771_Wroclaw_demography_per_BREC_statistical_region_of_the_city">DOI: 10.13140/RG.2.1.3848.2967</a>·</strong>
<div class="graf--mixtapeEmbed">Zbiór zawiera wiersze z następującymi danymi:</div>
<ul>
	<li>nr rejonu statystycznego</li>
	<li>liczbę zameldowanych osób w tym rejonie</li>
	<li>gęstość zaludnienia w tym rejonie</li>
	<li>liczbę zameldowanych osób w tym rejonie w podziale wedle wieku: 0–2, 3–6, 7–12, 13–15, 16–18, 19–24, 25–34, 35–44, (45–59 dla kobiet / 45–64 dla mężczyzn), (od 60 dla kobiet / 65 dla mężczyzn do 79) i od 80 lat w górę</li>
	<li>zapisany w formie <a href="https://en.wikipedia.org/wiki/Well-known_text" data-href="https://en.wikipedia.org/wiki/Well-known_text">WKT</a> obszar geograficzny tego rejonu — wielokąt (<em>POLYGON</em>) w projekcji EPSG:4326 najpopularniejszej w globalnych narzędziach mapowych w sieci</li>
</ul>

