---
layout: project
title:  "YOUR PROJECT NAME"
date:   2014-04-25 16:54:46
author: Marcel Newman
categories:
- project
img: portfolio_10.jpg
thumb: thumb02.jpg
carousel:
- single01.jpg
- single02.jpg
- single03.jpg
tagged: Flat, UI, Development
client: Wonder Corp.
website: http://blacktie.co
---
####Przestrzenne dane demograficzne Wrocławia

<blockquote>Jeśli jesteś tu tylko po dane, znajdziesz je w <a style="color: #000;" href="https://niedakh.cartodb.com/tables/demografia_wroclawia_2014_wg_rejonow_brec_2011">CartoDB</a> oraz Research Gate - <a style="color: #000;" href="https://www.researchgate.net/publication/291820771_Wroclaw_demography_per_BREC_statistical_region_of_the_city">DOI: 10.13140/RG.2.1.3848.2967</a>·</blockquote>

<h4>Dane po Wrocławsku</h4>
Do robienia analizy miejskich potrzebne jest przygotowanie pewnego warsztatu, a w szczególności danych, czasem będą to dane bezpośrednio ze świetnej inicjatywy <a href="http://www.wroclaw.pl/open-data/" data-href="http://www.wroclaw.pl/open-data/">OpenData </a>okraszone szerszym opisem i przykładami użycia, innym razem będę udostępniał te dane w postaci przetworzonego zbioru danych — np. kiedy wymagał on chwili pracy nad integracją pomiędzy systemami różnych instytucji (np. wrocławskiego SIP-u i danych z GUS-u).

Na samym początku chcę opowiedzieć i zgromadzić dla wrocławskich (i nie tylko) <em>data scientists </em>dane, które często są potrzebne do analiz. Będę je udostępniać w łatwych do załadowania i przetwarzania formatach. Najczęściej będę je umieszczał na ogólnodostępnych platformy jak np. cartodb.com lub inne platformy jeśli akurat będą oferować sensowną wartość dodaną. Przetworzonym zbiorom danych będą towarzyszyć noty publikacyjne z ResearchGate, które posiadają unikatowy numer identyfikacyjny (<a href="https://pl.wikipedia.org/wiki/DOI_(identyfikator_cyfrowy)">DOI</a>) dzięki czemu można go w prosty i szybki sposób cytować w pracach naukowych.

Chcę docelowo zgromadzić następujący bazowy zestaw danych:
<ul>
	<li>dane demograficzne z podziałem na wiek oraz obszarami wedle rejonów statystycznych</li>
	<li>pełne dane o możliwościach ruchu w mieście, tj. złączone ze sobą dane o trasach pieszych, rowerowych i samochodowych z openstreemapy (wysoka jakość we Wrocławiu) połączone z danymi z GTFS udostępnionymi z OpenData, a także ruchu kolejowego (jeśli się uda)</li>
	<li>dendryty i obciążenia ruchem — uzyskane za pomocą systemu <a href="https://github.com/mk45/pankus" data-href="https://github.com/mk45/pankus">pankus</a> autorstwa Macieja Kamińskiego oraz prof. T. Zipsera z Katedry Planowania Przestrzennego</li>
	<li>szczególnie poszukuję danych o mobilności pasażerów, korkach i wszelkiej maści podobnych rzeczach, jeśli macie takie dane — piszcie na <a href="http://niedakh@gmail.com" data-href="http://niedakh@gmail.com">niedakh@gmail.com</a></li>
	<li>jestem również otwarty na propozycje, a także na nadsyłanie danych - serdecznie zachęcam wszystkich do dzielenia się danymi</li>
</ul>
Cykl zaczynam od danych demograficznych.
<h4>Dane demograficzne</h4>
Bardzo często istnieje potrzeba zestawienia jakiegoś zjawiska we Wrocławiu z danymi o tym, ilu ludzi mieszka na danym obszarze. Dane demograficzne można pobrać z systemu informacji przestrzennej Wrocławia — <a href="http://geoportal.wroclaw.pl/www/mapa-demografia.shtml" data-href="http://geoportal.wroclaw.pl/www/mapa-demografia.shtml">mapy demograficznej</a>.

Znajdziemy tam 579 obszarów, do każdego przypisana populacja z podziałem na wiek. Można te dane dość łatwo zaznaczyć, ułożyć w tabelę i wyeksportować jako CSV. Niestety, nie da się wyeksportować w wygodny sposób danych geograficznych o obszarach. Znamy jedynie numery rejonów statystycznych GUS do których są przyporządkowane. Rejony statystyczne pochodzą z systemu <em>BREC </em>rejestru <a href="http://bip.stat.gov.pl/dzialalnosc-statystyki-publicznej/rejestr-teryt/zakres-rejestru-teryt/" data-href="http://bip.stat.gov.pl/dzialalnosc-statystyki-publicznej/rejestr-teryt/zakres-rejestru-teryt/"><em>TERYT</em></a> zebranego przez <em>GUS</em>. Ostatni raz system ten był aktualizowany w 2011 roku.

Dane z systemu <em>BREC</em> dostępne są przez portal realizujący europejską dyrektywę <a href="http://www.akademiainspire.pl/dyrektywa-inspire" data-href="http://www.akademiainspire.pl/dyrektywa-inspire"><em>INSPIRE</em></a> dot. danych GIS. Link do archiwum ZIP zawierającym shapefiles (SHP) z rejonami statystycznymi systemu <em>BREC</em> w projekcji EPSG:2180 znajdziecie <a href="http://geo.stat.gov.pl/atom_web-0.1.0/download/?fileId=006840865be32b80182bccd2806d8d3d&amp;name=PD_BREC_2011_REJ.zip" data-href="http://geo.stat.gov.pl/atom_web-0.1.0/download/?fileId=006840865be32b80182bccd2806d8d3d&amp;name=PD_BREC_2011_REJ.zip">tutaj</a>.

<strong>Naszym celem w tym odcinku jest posiadanie jednolitego zbioru zawierającego zarówno obszary jak i dane demograficzne. Taki zbiór danych, w projekcji EPSG:4326 udostępniam w serwisie <a href="https://niedakh.cartodb.com/tables/demografia_wroclawia_2014_wg_rejonow_brec_2011">CartoDB</a> jak również w postaci noty publikacyjnej w portalu Research Gate: <a href="https://www.researchgate.net/publication/291820771_Wroclaw_demography_per_BREC_statistical_region_of_the_city">DOI: 10.13140/RG.2.1.3848.2967</a>·</strong>
<div class="graf--mixtapeEmbed">Zbiór zawiera wiersze z następującymi danymi:</div>
<ul>
	<li>nr rejonu statystycznego</li>
	<li>liczbę zameldowanych osób w tym rejonie</li>
	<li>gęstość zaludnienia w tym rejonie</li>
	<li>liczbę zameldowanych osób w tym rejonie w podziale wedle wieku: 0–2, 3–6, 7–12, 13–15, 16–18, 19–24, 25–34, 35–44, (45–59 dla kobiet / 45–64 dla mężczyzn), (od 60 dla kobiet / 65 dla mężczyzn do 79) i od 80 lat w górę</li>
	<li>zapisany w formie <a href="https://en.wikipedia.org/wiki/Well-known_text" data-href="https://en.wikipedia.org/wiki/Well-known_text">WKT</a> obszar geograficzny tego rejonu — wielokąt (<em>POLYGON</em>) w projekcji EPSG:4326 najpopularniejszej w globalnych narzędziach mapowych w sieci</li>
</ul>
<h4>Gorąco zachęcam do korzystania, kopiowania i bawienia się tym jakże długo oczekiwanym zbiorem danych!</h4>
Zbiór danych można cytować w następujący sposób:

<cite>Szymański P., „Wrocław demography per BREC statistical region of the city”, ResearchGate, 25 stycznia 2016 [dostęp: dzień miesiąc rok], &lt;http://dx.doi.org/10.13140/RG.2.1.3848.2967&gt;, DOI: 10.13140/RG.2.1.3848.2967.
</cite>

lub za pomocą narzędzia bibtex:
<code></code>
<pre>@misc{10.13140/RG.2.1.3848.2967,
    author = {Piotr Szymański},
    title = {Wrocław demography per BREC statistical region of the city},
    doi = {10.13140/RG.2.1.3848.2967},
    howpublished= {\url{http://dx.doi.org/10.13140/RG.2.1.3848.2967}
}
</pre>
Na apetyt, wizualizacja liczby zameldowanych we Wrocławiu, z rejonami pogrupowanymi wedle gęstości zaludnienia metodą <a href="https://en.wikipedia.org/wiki/Jenks_natural_breaks_optimization">Jenksa</a>:

<iframe src="https://niedakh.cartodb.com/viz/fe92f4b0-c071-11e5-b331-0ecd1babdde5/embed_map" width="100%" height="520" frameborder="0" allowfullscreen="allowfullscreen"></iframe>