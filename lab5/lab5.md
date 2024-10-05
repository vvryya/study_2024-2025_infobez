---
## Front matter
title: "Лабораторная работа №5"
author: "Павлова Варвара Юрьевна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# Ход работы

**1.** Войдите в систему от имени пользователя guest.

**2.** Создайте программу simpleid.c:: (рис. [-@fig:001]) (рис. [-@fig:002])

![touch](image/1.png){ #fig:001 width=70% }

![simpleid.c](image/2.png){ #fig:002 width=70% }

**3.** Скомплилируйте программу и убедитесь, что файл программы создан: (рис. [-@fig:003])

![компиляция](image/3.png){ #fig:003 width=70% }

**4.** Выполните программу simpleid: (рис. [-@fig:004])

![выполнение](image/4.png){ #fig:004 width=70% }
  
**5.** Выполните системную программу id: (рис. [-@fig:005])

![id](image/5.png){ #fig:005 width=70% }

**6.**  Усложните программу, добавив вывод действительных идентификаторов: (рис. [-@fig:006])

![simpleid2](image/6.png){ #fig:006 width=70% }

**7.** Скомпилируйте и запустите simpleid2.c: (рис. [-@fig:007])

![компиляция](image/7.png){ #fig:007 width=70% }

**8.** От имени суперпользователя выполните команды: (рис. [-@fig:008])

![команды](image/8.png){ #fig:008 width=70% }

**9.** Выполните проверку правильности установки новых атрибутов и смены владельца файла simpleid2: (рис. [-@fig:009])

![ls -l](image/9.png){ #fig:009 width=70% }

**10.** Запустите simpleid2 и id: (рис. [-@fig:010])

![запуск](image/10.png){ #fig:010 width=70% }

**11.** Создайте программу readfile.c:(рис. [-@fig:011])

![readfile.c](image/11.png){ #fig:011 width=70% }

**12.** Откомпилируйте её. (рис. [-@fig:012])

![компиляция](image/12.png){ #fig:012 width=70% }

**13.**  Смените владельца у файла readfile.c (или любого другого текстового файла в системе) и измените права так, чтобы только суперпользователь (root) мог прочитать его, a guest не мог. (рис. [-@fig:013])

![chmod](image/13.png){ #fig:013 width=70% }

**14.** Проверьте, что пользователь guest не может прочитать файл readfile.c.(рис. [-@fig:014])

![cat](image/14.png){ #fig:14 width=70% }

**15.** Смените у программы readfile владельца и установите SetU’D-бит. (рис. [-@fig:015])

![chmod](image/15.png){ #fig:015 width=70% }

**16.** Проверьте, может ли программа readfile прочитать файл readfile.c? (рис. [-@fig:016])

![readfile](image/16.png){ #fig:016 width=70% }

**17.**   Проверьте, может ли программа readfile прочитать файл /etc/shadow? (рис. [-@fig:017])

![readfile](image/17.png){ #fig:017 width=70% }

**18.**  Выясните, установлен ли атрибут Sticky на директории /tmp (рис. [-@fig:018])

![ls](image/18.png){ #fig:018 width=70% }

**19.** От имени пользователя guest создайте файл file01.txt в директории /tmp со словом test: (рис. [-@fig:019])

![echo](image/19.png){ #fig:019 width=70% }

**20.** Просмотрите атрибуты у только что созданного файла и разрешите чтение и запись для категории пользователей «все остальные»: (рис. [-@fig:020])

![chmod](image/20.png){ #fig:020 width=70% }

**21.** От пользователя guest2 (не являющегося владельцем) попробуйте прочитать файл /tmp/file01.txt:(рис. [-@fig:021])

![cat](image/21.png){ #fig:021 width=70% }

**22.** От пользователя guest2 попробуйте дозаписать в файл /tmp/file01.txt слово test2 (рис. [-@fig:022])

![echo](image/22.png){ #fig:022 width=70% }

**23.** Проверьте содержимое файла командой(рис. [-@fig:023])

![cat](image/23.png){ #fig:023 width=70% }

**24.** От пользователя guest2 попробуйте записать в файл /tmp/file01.txt слово test3(рис. [-@fig:024])

![chmod](image/24.png){ #fig:024 width=70% }

**25.** Проверьте содержимое файла командой(рис. [-@fig:025])

![cat](image/25.png){ #fig:025 width=70% }

**26.** От пользователя guest2 попробуйте удалить файл /tmp/file01.txt командой (рис. [-@fig:026])

![rm](image/26.png){ #fig:026 width=70% }

**27.** Повысьте свои права до суперпользователя и выполните после этого команду, снимающую атрибут t (Sticky-бит) с директории /tmp:(рис. [-@fig:027])

![chmod](image/27.png){ #fig:027 width=70% }

**28.** От пользователя guest2 проверьте, что атрибута t у директории /tmp нет: (рис. [-@fig:028])

![ls](image/28.png){ #fig:028 width=70% }

**29.** Удалось ли вам удалить файл от имени пользователя, не являющегося его владельцем?(рис. [-@fig:029])

![rm](image/29.png){ #fig:029 width=70% }

**30.** Повысьте свои права до суперпользователя и верните атрибут t на директорию /tmp: (рис. [-@fig:030])

![chmod](image/30.png){ #fig:030 width=70% }

# Вывод

В ходе выполнения данной лабораторной работы я изучила механизмы изменения идентификаторов, применения SetUID- и Sticky-битов. Получила практические навыки работы в консоли с дополнительными атрибутами. Рассмотрела работу механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.