---
## Front matter
title: "Отчет по лабораторной работе № 6"
subtitle: "Арифметические операции в NASM. "
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

Освоение арифметических инструкций языка ассемблера NASM.




# Выполнение лабораторной работы

**Символьные и численные данные в NASM**

Создадим каталог для программ лабораторной работы № 6, перейдем в него и создадим файл lab6-1.asm (рис. [-@fig:001]).

![Создаем каталог и файл](image/61.png){#fig:001 width=70%}


Откроем файл lab6-1.asm в Midnight Commander и заполним его в соответствии с листингом (рис. [-@fig:002]).

![Переписываем код](image/62.png){#fig:002 width=70%}


Создадим исполняемый файл и запустим его.  (рис. [-@fig:003]).

![Запускаем файл и смотрим на его работу](image/63.png){#fig:003 width=70%}


Далее изменим текст программы и вместо символов, запишем в регистры числа.Открываем файл для редактирования и убиравем кавычки с числовых значений  (рис. [-@fig:004]).

![Изменяем файл](image/64.png){#fig:004 width=70%}


Создадим исполняемый файл и запустите его. (рис. [-@fig:005]).

![Проверяем работу прораммы](image/65.png){#fig:005 width=70%}


Создаем новый файл в каталоге. (рис. [-@fig:006]).

![Создаем файл](image/66.png){#fig:006 width=70%}


Заполняем файл в соответствии с листингом 6.2 (рис. [-@fig:007]).

![Заполняем файл](image/67.png){#fig:007 width=70%}


Создаем исполняемый файл и запускаем его. (рис. [-@fig:008]).

![Смотрим на работу программы](image/68.png){#fig:008 width=70%}


Снова открываем файл для редактирования и убираем кавычки с числовых значений (рис. [-@fig:009]).

![Изменяем файл](image/69.png){#fig:009 width=70%}


Создаем исполняемый файл и запускаем его (рис. [-@fig:010]).

![Проверяем работу программы](image/610.png){#fig:010 width=70%}


Снова открываем файл для редактирования и меняем iprintLF на iprint (рис. [-@fig:011]).

![Изменяем файл](image/611.png){#fig:011 width=70%}


Создаем исполняемый файл и запускаем его (рис. [-@fig:012]).

![Смотрим на работу программы](image/612.png){#fig:012 width=70%}

Вывод функций iprintLF и iprint отличаются только тем, что LF переносит на новую строку.


**2. Выполнение арифметических операций в NASM**


Создадим файл lab6-3.asm в каталоге ~/work/arch-pc/lab06 (рис. [-@fig:013]).

![Создаем файл](image/613.png){#fig:013 width=70%}



Изучим текст программы из листинга 6.3 и введем в lab6-3.asm. (рис. [-@fig:014]).

![Заполняем файл](image/614.png){#fig:014 width=70%}


Создаем исполняемый файл и запускаем его.  (рис. [-@fig:015]).

![Смотрим на результат работы программы](image/615.png){#fig:015 width=70%}


Изменим текст программы для вычисления выражения 
f(x) = (4 ∗ 6 + 2)/5 (рис. [-@fig:016]).

![Редактируем код](image/616.png){#fig:016 width=70%}


Создадим исполняемый файл и проверим его работу. (рис. [-@fig:017]).

![Смотрим на результат работы программы](image/617.png){#fig:017 width=70%}


Создадим файл variant.asm в каталоге ~/work/arch-pc/lab06 (рис. [-@fig:018]).

![Создаем файл](image/618.png){#fig:018 width=70%}


Открываем файл и редактируем в соответствии с листингом 6.4 (рис. [-@fig:019]).

![Заполняем файл](image/619.png){#fig:019 width=70%}


Компилируем файл и запускаем его (рис. [-@fig:020]).

![Запускаем программу](image/620.png){#fig:020 width=70%}


**Ответы на вопросы к программе**

1. Какие строки листинга 6.4 отвечают за вывод на экран сообщения ‘Ваш вариант:’?
Строки “mov eax,rem” и  “call sprint” 

2. Для чего используется следующие инструкции?
Эти инструкции используются для чтения строки с вводом данных от пользователя. Начальный адрес строки сохраняется в регистре ecx, а количество символов в строке (максимальное количество символов, которое может быть считано) сохраняется в регистре edx. Затем вызывается процедура sread, которая выполняет чтение строки. 
mov ecx, x 
mov edx, 80 
call sread 

3. Для чего используется инструкция “call atoi”? 
 Инструкция “call atoi” используется для преобразования строки в целое число. Она принимает адрес строки в регистре eax и возвращает полученное число в регистре eax. 
 	
4. Какие строки листинга 6.4 отвечают за вычисления варианта? 
Строка “xor edx,edx” обнуляет регистр edx перед выполнением деления. Строка “mov ebx,20” загружает значение 20 в регистр ebx. Строка “div ebx” выполняет деление регистра eax на значение регистра ebx с сохранением частного в регистре eax и остатка в регистре edx. 

5. В какой регистр записывается остаток от деления при выполнении инструкции “div ebx”? 
Остаток от деления записывается в регистр edx. 


6. Для чего используется инструкция “inc edx”? 
Инструкция “inc edx” используется для увеличения значения в регистре edx на 1. В данном случае, она увеличивает остаток от деления на 1. 

7. Какие строки листинга 6.4 отвечают за вывод на экран результата вычислений? 
Строка “mov eax,edx” передает значение остатка от деления в регистр eax. Строка “call iprintLF” вызывает процедуру iprintLF для вывода значения на экран вместе с переводом строки. 
	
	
	
**Задание для самостоятельной работы**


Создаем новый файл в каталоге. (рис. [-@fig:021]).

![Создаем файл ](image/621.png){#fig:0021 width=70%}


Открываем его и заполняем, чтобы решалось выражение f(x)=5(х-1)^2 (рис. [-@fig:022]).

![Заполняем файл](image/622.png){#fig:022 width=70%}


Компилируем программу и проверяем для x=3 (рис. [-@fig:023]).

![Проверяем работу программы](image/623.png){#fig:023 width=70%}


Меняем программу  для x=1 и проверяем как она работает (рис. [-@fig:024]).

![Проверяем работу программы](image/624.png){#fig:024 width=70%}


# Выводы

Мы приобрели навыки создания исполнительных файлов для решения выра жений и освоили арифметические инструкции в NASM.

