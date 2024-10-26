---
## Front matter
lang: ru-RU
title: Лабораторная работы №7
author: Павлова В.Ю.
institute: RUDN University, Moscow, Russian Federation

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

## Цель работы

Освоить на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом.

---

## Ход работы

Задаю данные, перевожу их в байты и задаю ключ. (рис. [-@fig:001])

![данные](image/1.png){ #fig:001 width=70% }

---

## Ход работы

Пишу функцию для шифрования(рис. [-@fig:002])

![функция](image/2.png){ #fig:002 width=70% }

---

## Ход работы

Шифрование P1 и P2. (рис. [-@fig:003])

![шифрование](image/3.png){ #fig:003 width=70% }

---

## Ход работы

Находим P2, зная C1, C2 и P1 (рис. [-@fig:004])

![P2](image/4.png){ #fig:004 width=70% }

---

## Вывод

В ходе выполнения данной лабораторной работы я освоила на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом.