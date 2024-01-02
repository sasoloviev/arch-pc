---
## Front matter
title: "Отчёт по лабораторной работе 2"
subtitle: "Архитектура компьютера"
author: "Соловьев Серафим"

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

Целью работы является изучить идеологию и применение средств контроля версий. Приобрести практические навыки по работе с системой git.

# Выполнение лабораторной работы

Регистрирую аккаунт на GitHub.

![Регистрация профиля](image/01.png){ #fig:001 width=70%, height=70% }

Аккаунт успешно зарегистрирован.

![Профиль создан](image/02.png){ #fig:002 width=70%, height=70% }

Следующий шаг – инициализация нового репозитория. Открываю репозиторий учителя и использую его в качестве основы.

![Использование шаблона](image/03.png){ #fig:003 width=70%, height=70% }

![Использование шаблона](image/04.png){ #fig:004 width=70%, height=70% }

Программа Git установлена на компьютере.

![Команды git](image/05.png){ #fig:005 width=70%, height=70% }

Теперь предстоит настроить личные данные пользователя, конфигурацию ветвления и настройки символов.

![Параметры git](image/06.png){ #fig:006 width=70%, height=70% }

Чтобы авторизоваться, необходимо создать SSH-ключ и добавить его в профиль.

![Создание ключа](image/07.png){ #fig:007 width=70%, height=70% }

![Сохранение ключа](image/08.png){ #fig:008 width=70%, height=70% }

Теперь создам новую директорию и склонирую в неё репозиторий.

![Создание рабочего каталога](image/09.png){ #fig:009 width=70%, height=70% }

В репозитории есть скрипт Make для организации директорий курса. 
Запустим его для создания директорий лабораторных работ.

![Создание рабочего каталога](image/10.png){ #fig:010 width=70%, height=70% }

![Создание рабочего каталога](image/11.png){ #fig:011 width=70%, height=70% }

После создания локальных директорий их можно отправить в удалённый репозиторий.

![push](image/12.png){ #fig:012 width=70%, height=70% }

# Выводы

В ходе выполнения работы изучили работу с GitHub.

