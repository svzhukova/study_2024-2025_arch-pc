---
## Front matter
title: "ОТЧЕТ ПО ЛАБОРАТОРНОЙ РАБОТЕ №2"
subtitle: "Github"
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

Изучить идеологию и применение средств контроля версий. Приобрести
практические навыки по работе с системой git.

# Задание

В соответствующем каталоге сделать отчет по лабораторной работе 2 в формате Markdown.


# Выполнение лабораторной работы

Создадим учётную запись на сайте https://github.com/ и заполним
основные данные.
Базовая настройка git
Сначала сделаем предварительную конфигурацию git. Откроем терминал
и введем следующие команды, указав имя и email. (рис. [-@fig:014]).

![](image/Снимок экрана от 2024-09-27 23-19-17.png){#fig:014 width=70%}

Настроим utf-8 в выводе сообщений git (рис. [-@fig:015]).

![](image/Снимок экрана от 2024-09-27 23-22-45.png){#fig:015 width=70%}

Зададим имя начальной ветки (будем называть её master), параметры
autocrlf и safecrlf (рис. [-@fig:001]). 

![](image/Снимок экрана от 2024-09-27 23-33-54.png){#fig:001 width=70%}

Создание SSH ключа
Для последующей идентификации пользователя на сервере репозиториев
сгенерируем пару ключей (приватный и открытый): (рис. [-@fig:002]).

![](image/Снимок экрана от 2024-09-27 23-28-10.png){#fig:002 width=70%}

Ключи сохраняться в каталоге ~/.ssh/.
Далее необходимо загрузить сгенерённый открытый ключ.
Введем команду в терминал (рис. [-@fig:003]).

![](image/Снимок экрана от 2024-09-28 01-27-39.png){#fig:003 width=70%}

Далее перейдем в настройки в github и загрузим сгенерённый открытый
ключ.
Скопировав из локальной консоли ключ в буфер обмена вставляем ключ в
появившееся на сайте поле и указываем для ключа имя (Title). (рис. [-@fig:004]).

![](image/Снимок экрана от 2024-09-28 01-19-08.png){#fig:004 width=70%}

Сознание рабочего пространства и репозитория курса на основе
шаблона
Откроем терминал и создадим каталог для предмета «Архитектура
компьютера»: (рис. [-@fig:005]).

![](image/Снимок экрана от 2024-09-28 01-30-00. png){#fig:005 width=70%}

Создание репозитория курса на основе шаблона
Перейдите на станицу репозитория с шаблоном курса и выберем Use this
template
В открывшемся окне зададим имя репозитория (Repository name)study_2024–2025_arh и создадим репозиторий . (рис. [-@fig:006]).

![](image/Снимок экрана от 2024-09-28 01-35-20.png){#fig:006 width=70%}

Откроем терминал и перейдем в каталог курса (рис. [-@fig:007]).

![](image/Снимок экрана от 2024-09-28 02-34-31.png){#fig:007 width=70%}

Клонируем созданный репозиторий (рис. [-@fig:008]).

![](image/Снимок экрана от 2024-09-28 02-55-40.png){#fig:008 width=70%}. Настройка каталога курса

Перейдем в каталог курса: (рис. [-@fig:009]).

![](image/Снимок экрана от 2024-09-28 03-01-34.png){#fig:009 width=70%}

Удалим лишние файлы (рис. [-@fig:010]).

![](image/Снимок экрана от 2024-09-28 03-03-23.png){#fig:010 width=70%}

Cоздадим необходимые каталоги (рис. [-@fig:011]).

![](image/Снимок экрана от 2024-09-28 03-08-54.png){#fig:011 width=70%}

Отправим файлы на сервер: (рис. [-@fig:012]).

![](image/Снимок экрана от 2024-09-28 03-51-34.png){#fig:012 width=70%}

Проверим правильность создания иерархии рабочего пространства в
локальном репози тории и на странице github. (рис. [-@fig:0133]).

![](image/Снимок экрана от 2024-09-28 21-12-39.png){#fig:0133 width=70%}

Загрузим файлы на github (рис. [-@fig:013]).

![](image/Снимок экрана от 2024-09-28 04-14-06.png){#fig:013 width=70%}
 

# Выводы
Мы изучили идеологию и применение средств контроля версий.
Приобрели практические навыки по работе с системой git. Мы создали свой
репозиторий в github, в нем мы будем хранит свои работы в даьнейшем
