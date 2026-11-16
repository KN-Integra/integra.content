---
lastmod: 2026-11-16T8:12:00Z
head:
  meta:
    - name: keywords
      content: project, wheel-e, in-progress, robots, balancing robots
    - name: robots
      content: index follow
    - name: author
      content: Adam Maciuga
    - name: copyright
      content: © 2026 KN Integra
    - name: createdAt
      lastmod: 2026-11-16T8:12:00Z
---

# Wheel-E

<!-- markdownlint-disable MD003 MD007 -->

::image-carousel
---

images:

- src: ./img/wysuniety.jpg
  alt: Wheel-E z wysuniętą nogą
- src: ./img/zlozony.jpg
  alt: Wheel-E ze złożoną nogą

---

::

<!-- markdownlint-enable MD003 MD007 -->

Wheel-E to robot o nietypowej, trudnej w sterowaniu konstrukcji.
Taki też miał być, jednym z głównym celów tego projektu było sworznie platformy, która będzie wymagała implementacji zaawansowanych algorytmów sterowania.
Konstrukcja robota składa się z 4 głównych komponentów:

- Koło jezdne (pozwala na poruszanie się robota, oraz na utrzymanie równowagi w osi przód-tył)
- Korpus dolny (element konstrukcyjny, przymocowane do niego jest koło jezdne, jeden z elementów nogi )
- Korpus górny (element konstrukcyjny, do niego przymocowane jest większość pomniejszych komponentów robota, ruch górnego korpusu, względem dolnego, ma pozwalać na wykonywanie skoków i amortyzację nierówności terenu)
- Koła Reakcyjne (pozwalają na utrzymanie równowagi w osi lewo-prawo)

## Serwomechanizm

Jako elementy wykonawcze, w robocie zostały zastosowane serwomechanizmy oparte na silnikach BLDC, przekładniach cykloidalnych oraz autorskich sterowników FOC.

<!-- markdownlint-disable MD003 MD007 -->

::picture-component
---

image:
  src: ./img/przekladnia.jpg
  size: md

alt: Przekładnia Cykloidalna

---

::

<!-- markdownlint-enable MD003 MD007 -->

## Elektronika

Ze względu na dużą częstotliwość i jakość sterowania wymaganą do prawidłowego funkcjonowania robota,
Stworzyliśmy autorskie obwody drukowane.

### Sterownik główny

<!-- markdownlint-disable MD003 MD007 -->

::picture-component
---

image:
  src: ./img/main_pcb.jpg
  size: md

alt: Sterownik główny

---

::

<!-- markdownlint-enable MD003 MD007 -->

Sterownik ten, oparty na dwurdzeniowej STM32H7, pozwala na szybie zebranie wszystkich potrzebnych danych z czujników, i przeprowadzenia niezbędnych obliczeń w czasie rzeczywistym.
Oprócz mikrokontrolera na płytce znajduje się między innymi żyroskop akcelerometr moduł BLE służący do telemetrii oraz transceiver magistrali CAN. Całość, ze względu na zastosowanie systemu czasu rzeczywistego FreeRTOS pozwala na zapewnienie czasu rzeczywistego, niezbędnego do poprawnego działania robota.

### Sterowniki Silników

<!-- markdownlint-disable MD003 MD007 -->

::picture-component
---

image:
  src: ./img/bldc_pcb.jpg
  size: md

alt: Sterownik silników BLDC

---

::

<!-- markdownlint-enable MD003 MD007 -->

Stworzyliśmy również sterowniki do silników BLDC 60 A / 60 V. Pozwalają one na dokładne dostosowanie programu pod wymagania postawione przez projekt oraz ułatwią wykorzystywanie silników BLDC w przyszłych projektach realizowanych przez koło.
