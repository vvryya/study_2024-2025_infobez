---
## Front matter
title: "Лабораторная работа №3"
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

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Ход работы

**1.** . В установленной операционной системе создайте учётную запись пользователя guest (использую учётную запись администратора): (рис. [-@fig:001])

![Создание учетной записи](image/1.png){ #fig:001 width=70% }

**2.** 2. Задайте пароль для пользователя guest (использую учётную запись администратора)(рис. [-@fig:002])

![Задание пароля](image/2.png){ #fig:002 width=70% }

**3.** Аналогично создайте второго пользователя guest2.(рис. [-@fig:003])

![Создание пользователя](image/3.png){ #fig:003 width=70% }

**4.** Осуществите вход в систему от двух пользователей на двух разных консолях: guest на первой консоли и guest2 на второй консоли. (рис. [-@fig:004])

![Вход в систему](image/4.png){ #fig:004 width=70% }
  
**5.** Осуществите вход в систему от двух пользователей на двух разных консолях: guest на первой консоли и guest2 на второй консоли. (рис. [-@fig:005])

![pwd](image/5.png){ #fig:005 width=70% }

**6.** Уточните имя вашего пользователя, его группу, кто входит в неё и к каким группам принадлежит он сам.  (рис. [-@fig:006; -@fig:007; -@fig:008; -@fig:009])

![groups guest](image/6.png){ #fig:006 width=70% }

![groups guest2](image/7.png){ #fig:007 width=70% }

![вывод команд](image/8.png){ #fig:008 width=70% }

![вывод команд](image/9.png){ #fig:009 width=70% }

**7.** Сравните полученную информацию с содержимым файла /etc/group. (рис. [-@fig:010])

![просмотр содержимого файла](image/10.png){ #fig:010 width=70% }

**8.** От имени пользователя guest измените права директории /home/guest, разрешив все действия для пользователей группы. (рис. [-@fig:011])

![изменение прав доступа](image/11.png){ #fig:011 width=70% }

**9.** От имени пользователя guest снимите с директории /home/guest/dir1 все атрибуты командой (рис. [-@fig:012])

![снятие атрибутов](image/12.png){ #fig:012 width=70% }

# Вывод

В ходе выполнения данной лабораторной работы я получила практические навыки работы в консоли с атрибутами файлов для групп пользователей.