---
lastmod: 2023-11-8T4:21:00Z
head:
  meta:
    - name: keywords
      content: kraksat, cosmos, satellite, iss
    - name: robots
      content: noindex nofollow
    - name: author
      content: Andrzej Piotrowski
    - name: copyright
      content: © 2023 KN Integra
    - name: createdAt
      content: 2023-11-8T4:21:00Z
---

# EVE
<p style="text-align:justify">
Głównym powodem rozpoczęcia prac nad sterownikiem do pojazdu autonomicznego było wznowienie projektu dotyczącego jednoosobowego pojazdu elektrycznego EVE. Pojazd ten powstał w roku 2008 jako platforma pokazowa firmy Delphi (obecnie Aptiv), następnie w roku 2014 trafił na AGH, jako projekt studencki powstający przy współpracy z firmą Delphi. Rozwijano pojazd w oparciu o MicroAutoBox firmy dSPACE oraz RACAM firmy Delphi. Korzystając z wyżej wymienionych podzespołów opracowywano algorytmy śledzenia ludzi. Programowanie systemu Micro Auto Box odbywało się za pomocą wewnętrznych narzędzi firmy dSPACE oraz pakietu Matlab Simulink wraz z bibliotekami dSPACE. Niestety po wygaśnięciu licencji na oprogramowanie dalsze prace nad pojazdem zostały zaniechane na dwa lata.

We wrześniu 2017 roku wznowiono prace nad EVE. Postanowiono oprzeć całą architekturę o narzędzia open-source, aby uniknąć problemów z licencjami na oprogramowania. Jako framework roboczy do opracowywania algorytmów sterowania oraz fuzji przyjęto ROS (Robot Operating System) pracujący pod systemem Ubuntu 16.04. ROS to prężnie rozwijający się framework, służący do tworzenia oprogramowania robotów oraz robotów mobilnych. Staje się szeroko stosowanym oprogramowaniem nie tylko w platformach studenckich, ale także w robotach przemysłowych, również ze względu na opracowywaną wersję ROS2, która jest frameworkiem czasu rzeczywistego. ROS także jest wykorzystywany przez koncern BMW w pracach nad autonomicznymi pojazdami. Założono również, że kompatybilność sterownika nie powinna być ograniczona tylko do współpracy z oprogramowaniem ROS. Komunikacja części hardwarowej z ROS odbywa się za pomocą kodowanej znakami ASCII komunikacji w standardzie USB CDC (Communications Device Class – widziane z poziomu systemu operacyjnego jako port COM), dzięki czemu sterownik można obsługiwać potencjalnie z każdego oprogramowania będącego w stanie wysyłać komendy ASCII za pomocą USB CDC.

Choć projekt znajduje się w fazie utrzymania, to planujemy wznowić działania nad nim. Aktualnie największym wyzwaniem w dalszym rozwoju projektu jest zaimplementowanie fuzji danych, która połączy IMU (Inertial Measurement Unit), enkodery zamontowane na kołach oraz bardzo dokładny GPS geodezyjny firmy Leica. Połączenie danych z tych sensorów ma zapewnić dobrą estymację położenia samochodu w każdych warunkach. Sam GPS jest wystarczająco dokładny, ale tylko wtedy, gdy znajduje się on w zasięgu widoczności wystarczającej ilości satelit oraz stacji referencyjnej. Dlatego wymagane są dodatkowe sensory, które pozwalają na wyznaczenie pozycji pojazdu w pozostałych miejscach terenu. Atkualnie poszukujemy osób, które znają podstawy ROS, języka Python, są ambitne i mają ochotę zmierzyć się z fuzją danych.
</p>
