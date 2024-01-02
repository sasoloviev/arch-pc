---
## Front matter
title: "Отчёт по лабораторной работе 4"
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

Целью работы является освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Выполнение лабораторной работы

Сформировал директорию lab04 используя mkdir, затем вошел в нее через cd и создал файл hello.asm для написания кода программы.
Удостоверился в наличии созданного файла при помощи ls.

![Создан каталог для работы и файл для программы](image/01.png){ #fig:001 width=70%, height=70% }

Составил программный код согласно заданию на языке ассемблера.

![Программа в файле hello.asm](image/02.png){ #fig:002 width=70%, height=70% }

NASM представляет собой ассемблер, который переводит ассемблерский текст программы в объектный код.
При отсутствии ошибок в исходнике, компилятор конвертирует текст из файла hello.asm в объектный код, сохраняемый в файле hello.o.

Командная строка nasm в полном виде принимает следующий вид:

```nasm [-@ косвенный_файл_настроек] [-o объектный_файл] [-f формат_объектного_файла] [-l листинг] [параметры...] [--] исходный_файл```

Использовал команду nasm с дополнительными параметрами для трансляции файла.
С параметром -l создал листинг в файле list.lst, с параметром -f сгенерировал объектный файл obj.o, а с параметром -g внедрил в программу отладочные данные.

![Трансляция программы c разными опциями](image/03.png){ #fig:003 width=70%, height=70% }

Для получения исполнимого файла необходимо передать объектный файл компоновщику.

Применил команду ld для создания исполнимого файла hello из объектного файла hello.o.
Повторно использовал ld для объектного файла obj.o, что привело к созданию исполнимого файла main.

![Компоновка программы c разными опциями](image/04.png){ #fig:004 width=70%, height=70% }

Запустил исполнимые файлы на выполнение.

![Запуск программы](image/05.png){ #fig:005 width=70%, height=70% }

## Задание для самостоятельной работы

Переместил содержимое файла hello.asm в файл lab4.asm.

![Скопировал файл](image/06.png){ #fig:006 width=70%, height=70% }

Заменил текст "Hello world" на свое имя.

![Программа в файле lab4.asm](image/07.png){ #fig:007 width=70%, height=70% }

Выполнил программу и осуществил проверку ее работы.

![Проверка программы lab4.asm](image/08.png){ #fig:008 width=70%, height=70% }

# Выводы

Освоил процесс компиляции и сборки программ, написанных на ассемблере nasm.