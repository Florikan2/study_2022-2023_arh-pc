---
## Front matter
title: "Шаблон отчёта по лабораторной работе"
subtitle: "Простейший вариант"
author: "Дмитрий Сергеевич Кулябов"

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

# Титульный лист 
		РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
		Факультет физико-математических и естественных наук
		Кафедра прикладной информатики и теории вероятностей





			ОТЧЕТ 
		по лабораторной работе № 11
	дисциплина:	Архитектура компьютера









						Студент: Яковин И.А

						Группа: НПИбд-02-22







				МОСКВА
				2022 г.


# Цель работы

Целью данной лабораторной работы является приобритение навыков написания программ для работы с файлами.


# Выполнение лабораторной работы

1. Создам каталог для программ лабораторной работы номер 11. Перейду в него и создам файл lab11-1.asm и readme.txt

![Рис.1 Создание каталога для программ лабораторной работы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab11/report/image/1.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BC%20%D1%84%D0%B0%D0%B9%D0%BB%20lab11-1.jpg.png)

2. Введу в файл lab11-1.asm текст программы из листинга 11.1.


![Рис.2 Ввод текста программы из листинга 11.1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab11/report/image/2.%20%D0%92%D0%B2%D0%B5%D0%B4%D1%83%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%2011.1.png)


3. Создам исполняемый файл и проверю его работу.

![Рис.3 Создам исполняемый файл и запущу его](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab11/report/image/3.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BC%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D0%BD%D1%8F%D0%B5%D0%BC%D1%8B%D0%B9%20%D1%84%D0%B0%D0%B9%D0%BB%20%D0%B8%20%D0%B7%D0%B0%D0%BF%D1%83%D1%89%D1%83%20%D0%B5%D0%B3%D0%BE.png)


4. С помощью chmod изменю права доступа к исполняемому файлу lab11-1, запретив его выполнение. Попытаюсь выполнить файл. Это не получится т.к я уже запретил выполнение файлу.

![Рис.4 Изменение прав доступа для lab11-1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab11/report/image/4.%20%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D1%8E%20%D0%BF%D1%80%D0%B0%D0%B2%D0%B0%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20%D0%B4%D0%BB%D1%8F%20lab11-1.png)


5. С помощью команды chmod изменю права доступа к файлу lab11-1.asm с исходным текстом программы, добавив права на исполнение. Запустить всё так же не получится, ведь запрет на выполнение на lab11-1 ещё действует.

![Рис.5 Изменение прав доступа для файла lab11-1.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab11/report/image/5.%20%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D1%8E%20%D0%BF%D1%80%D0%B0%D0%B2%D0%B0%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20%D0%B4%D0%BB%D1%8F%20lab11-1.asm.png)


6. Предоставлю права доступа к файлу readme.txt в соответствии с вариантом в таблице. (Вариант 2 в символьном виде --x -wx rwx). Проверю на правильность выполнения с помощью команды ls -l.

![Рис.6 Предоставление файла доступа в соответствии с вариантом](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab11/report/image/6.%20%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D1%8E%20%D0%BF%D1%80%D0%B0%D0%B2%D0%B0%20%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0%20%D0%B2%20%D1%81%D0%BE%D0%BE%D1%82%D0%B2%D0%B5%D1%82%D1%81%D1%82%D0%B2%D0%B8%D0%B8%20%D1%81%20%D0%B2%D0%B0%D1%80%D0%B8%D0%B0%D0%BD%D1%82%D0%BE%D0%BC.png)

# Выводы

Я приобрёл навыки написания программ для работы с файлами.
