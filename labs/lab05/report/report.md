---
## Front matter
title: "Лабораторная работа №5. Создание и процесс обработки программ на язвке ассемблера NASM"
subtitle: "Архитектура компьютера"
author: "Яковин Илья"

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
Целью работы является освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM

# Выполнение лабораторной работы
# ** 5.1 Программа Hello world!**
Создам каталог для работы с программами на языке ассемблера NASM:
![Рис. 5.1 Создание каталога](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/1.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0.png?raw=true){ #fig:001 width=70% }
Перейду в созданный каталог
![Рис 5.2 Каталог lab05](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/2.%20%D0%9F%D0%B5%D1%80%D0%B5%D1%85%D0%BE%D0%B4%20%D0%B2%20%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%B9%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3.png?raw=true){ #fig:001 width=70% }
Далее я создам текстовый файл с именем hello.asm и открою его с помощью текстового редактора
![Рис. 5.3 Создание текстового файла hello.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/3.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BC%20%D0%B8%20%D0%BE%D1%82%D0%BA%D1%80%D0%BE%D1%8E%20hello.asm.png?raw=true){ #fig:001 width=70% }
Далее я введу в него текст,который предоставлен в Лабораторной работе №5.
![Рис. 5.4Ввод текста](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/4.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B.png?raw=true){ #fig:001 width=70% }
# ** 5.1.1 Транслятор NASM **
Далее необходимо выполнить компиляцию текста программы. Затем с помощью команды ls проверю, что объектный файл был создан.
![Рис. 5.5 Компиляция текста программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/%D0%9A%D0%BE%D0%BC%D0%BF%D0%B8%D0%BB%D1%8F%D1%86%D0%B8%D1%8F%20%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0.png?raw=true){ #fig:001 width=70% }
# ** 5.1.2 Расширенный синтаксис командной строки NASM **
Проведу компиляцию исходного файла hello.asm в obj.o
![Рис. 5.6 Компиляция исходного файла hello.asm в obj.o](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/6.%20%D0%9A%D0%BE%D0%BC%D0%BF%D0%B8%D0%BB%D1%8F%D1%86%D0%B8%D1%8F%20hello.asm%20%D0%B2%20obj.0.png?raw=true){ #fig:001 width=70% }
С помощью команды ls проверю, что файлы были созданы
![Рис. 5.7 Проверка создания файлов](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/7.%20C%20%D0%BF%D0%BE%D0%BC%D0%BE%D1%89%D1%8C%D1%8E%20ls%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D1%8E%20%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%84%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2.png?raw=true){ #fig:001 width=70% }
# ** 5.2 Компоновщик LD **
Передам объектный файл на обработку компоновщику
![Рис. 5.8 Обработка компоновщиком](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/8.%20%D0%9F%D0%B5%D1%80%D0%B5%D0%B4%D0%B0%D1%87%D0%B0%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20%D0%BD%D0%B0%20%D0%BE%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D1%83%20%D0%BA%D0%BE%D0%BC%D0%BF%D0%BE%D0%BD%D0%BE%D0%B2%D1%89%D0%B8%D0%BA%D1%83.png?raw=true){ #fig:001 width=70% }
# ** 5.2.1 Запуск исполняемого файла **
Наберу в командной строке ./hello для запуска исполняемого файла.
![Рис. 5.9 Запуск на выполнениессозданного исполняемого файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/9.%20%D0%97%D0%B0%D0%BF%D1%83%D1%81%D0%BA%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D0%BD%D1%8F%D0%B5%D0%BC%D0%BE%D0%B3%D0%BE%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0.png?raw=true){ #fig:001 width=70% }
# ** 5.3 Задания для самостоятельной работы **
1. СОздам копию файла hello.asm с именем lab05.asm
![Рис. 5.10 Создание копии файла hello.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%201.png?raw=true){ #fig:001 width=70% }
2. С помощью текстового редактора внесу изменения в текст программы в файле lab5.asm так, чтобы вместо Hello world! на экран выводились моё имя и фамилия.
![Рис. 5.11 Вывод имени и фамилии](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%202.png?raw=true){ #fig:001 width=70% }
4. Скопирую файлы hello.asm и lab5.asm в мой локальный репозиторий и загружу файлы на Github
![Рис. 5.12 Копирование hello.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%204.1.png?raw=true){ #fig:001 width=70% }
![Рис. 5.13 Копирование lab5.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%204.2.png?raw=true){ #fig:001 width=70% }
![Рис. 5.14 Проверка](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab05/presentation/image/%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%204%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0.png?raw=true){ #fig:001 width=70% }


# Вывод
Я освоил процедуры компиляции и сборки программ, написанных на ассемблере NASM.

