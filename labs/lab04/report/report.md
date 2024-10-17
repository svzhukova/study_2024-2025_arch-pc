---
## Front matter
title: "Отчет  по лабораторной работе №4."
subtitle: "Создание и процесс обработки программ на языке ассемблера NASM"
author: "Жукова София Викторовна"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Освоить процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Задание

Написать прораграммы на языке ассемблер


# Выполнение лабораторной работы

Создадим каталог для работы с программами на языке ассемблера NASM:  (рис. [-@fig:001]).


![Создаем каталог](image/41.png){#fig:001 width=70%}


Перейдем в созданный каталог (рис. [-@fig:002]).


![Переходим в каталог](image/42.png){#fig:002 width=70%}


Создадим текстовый файл с именем hello.asm  (рис. [-@fig:003]).


![Создаем файл](image/43.png){#fig:003width=70%}


Откроем этот файл с помощью текстового редактора и введем в него следующий текст: (рис. [-@fig:004]).


![Открываем и заполняем файл](image/44.png){#fig:004 width=70%}


Превратим текст программы в объектный код. (рис. [-@fig:005]).

![](image/45.png){#fig:005 width=70%}


Проверяем создался ли объектный файл (рис. [-@fig:006]).


![](image/46.png){#fig:006 width=70%}


Выполним следующую команду: (рис. [-@fig:007]).


![](image/47.png){#fig:007 width=70%}


Проверим, что файлы были созданы. (рис. [-@fig:008]).


![](image/48.png){#fig:008 width=70%}


Передаем объектный файл на обработку компоновщику (рис. [-@fig:009]).


![](image/49.png){#fig:009 width=70%}


Проверяем создался ли исполняемый файл hello (рис. [-@fig:010]).


![](image/410.png){#fig:010 width=70%}


Выполним следующую команду: (рис. [-@fig:011]).


![](image/411.png){#fig:011 width=70%}


Проверяем создался ли исполняемый файл hello (рис. [-@fig:012]).


![](image/412.png){#fig:012 width=70%}


Наберем в командной строке:  (рис. [-@fig:013]).

![](image/413.png){#fig:013 width=70%}


Создаем копию файла hello.asm (рис. [-@fig:014]).


![](image/414.png){#fig:014 width=70%}


С помощью  текстового редактора внесем изменения в текст программы в файле lab4.asm так, чтобы вместо Hello world! на экран выводилась строка с фамилией и именем. 


Открываем и редактируем файл (рис. [-@fig:015]).


![](image/415.png){#fig:015 width=70%}


(рис. [-@fig:016]).


![](image/416.png){#fig:016 width=70%}


Оттранслируем полученный текст программы lab4.asm в объектный файл.	Выполним компоновку объектного файла и запустим получившийся исполняемый файл. (рис. [-@fig:017]).


![](image/417.png){#fig:017 width=70%}


Скопируем файлы hello.asm и lab4.asm в наш локальный репозиторий в каталог (рис. [-@fig:018]).


![](image/418.png){#fig:018 width=70%}


Загрузим файлы на Github.  (рис. [-@fig:019]).


![](image/419.png){#fig:019 width=70%}


# Выводы

Мы освоили процедуры компиляции и сборки программ, написанных на ассемблере NASM. Создали две программы на языке ассемблер.

