---
## Front matter
title: "Индивидуальный проект. Этап №5"
subtitle: "Использование nikto"
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

Использование Burp Suite.

# Ход работы

**1.** Проверка установки Burp Suite (рис. [-@fig:001])

![Установка](image/1.png){ #fig:001 width=70% }

**2.** При попытке запуска вылезает ошибка и поэтому к сожалению изучить Burp Suite удается только в теории.
**3.** Нахожу кнопку Proxy->Options и проверяю настройки в разделе Proxy Listeners. 
**4.** Настраиваю работу браузера для работы с Burp Suite 
**5.** Изучаю перехват запросов с Burp Suite 
**6.** Изучаю остальные возможности Burp Suite(анализ и модификация запросов, повторное отправление запросов)

# Вывод

Мы научились пользоваться Burp Suite.