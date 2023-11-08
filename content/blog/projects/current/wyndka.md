---
lastmod: 2023-08-07T20:15:00Z
head:
  meta:
    - name: keywords
      content: project, wwe, wyndka, in-progress,
    - name: robots
      content: index follow
    - name: author
      content: Jakub Mazur
    - name: copyright
      content: © 2023 KN Integra
    - name: createdAt
      content: 2023-03-21T21:26:00Z
---

# Wędka Wspomagana Elektrycznie "WWE Sumołów 2000"

<p style="text-align:justify">
W połowie roku 2022 do naszego koła zgłosił się Pan Michał, który w wypadku stracił władność w cześci swojego ciała, w tym w jednej z rąk. Pomimo tego, chciał on kontynuować swoje hobby, jakim jest łowienie ryb.

Głównym założeniem projektu jest stworzenie wędki, którą będzie się dało obsługiwać jedną ręką. Jest to realizowane przy pomocy silnika wyzwalanego przyciskiem - pozwala to na samoczynne zwijanie się żyłki. Dodatkowo, w celu kontroli prędkości zwijania powstaje aplikacja mobilna, łącząca się ze sterownikiem przy pomocy Bluetooth LE.

## Wykorzystane Technologie

Modele 3D całej konstrukcji zostały stworzone przy pomocy programu Autodesk Inventor, a dwuwarstwowa Płytka PCB została wykonana w programie Altium Designer. Cały hardware został oparty o płytkę prototypową nRF52840 Dongle, któa to jest fizycznie wlutowana w płytkę PCB. Firmware opiera się o Zephyr RTOS. Aplikacja mobilna (kompilowana na Androida) jest napisana w Pythonie 3, we frameworku Kivy. Komunikacja między procesorem a telefonem odbywa się przy pomocy Bluetoth LE, a konkretnie za pomocą serwisu GATT.
</p>

## Obecni członkowie

- **Koordynator**: Jakub Mazur
- Maciej Baczmański
- Jakub Sikora
- Sebastian Soczawa
- Michał Kawiak
- Maciej Wojtyś

## Byli Członkowie
- Gabriel Maj


<!-- markdownlint-disable MD003 MD007 -->
::image-carousel
---

images:

- src: https://raw.githubusercontent.com/eSqadron/integra.content/main/img/wyndka-1.jpeg
  alt: wwe 1
---
::
<!-- markdownlint-enable MD003 MD007 -->
