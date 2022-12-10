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
					по лабораторной работе № 9
				    дисциплина: Архитектура компьютера	









									Студент: Яковин И.А

									Группа: НПИбд-02-22







						МОСКВА
						2022 г.
# Цель работы

Целью данной лабораторной работы является приобретение навыков написания программ с использованием циклов и обработкой аргументов командной строки.

# Выполнение лабораторной работы

**Реализация циклов в NASM**

Создам каталог для программ лабораторной работы №9, затем перейду в него и создам файл lab9-1.asm

![Рис. 1 Создание файла lab9-1.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/1.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20lab9-1.asm.png)

Рис. 1 Создание файла lab9-1.asm


Внимательно изучу текст программы. Введу текст программы из листинга 9.1.

![Рис. 2 Ввод листинга 9.1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/2.%20%D0%9B%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%209.1%20%D0%B2%D0%B2%D0%BE%D0%B4.png)

Рис. 2 Ввод листинга 9.1


Далее я создам исполняеый файл и проверю его работу.

![Рис. 3 Проверка работы программы из листинга 9.1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/3.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20lab9-1.png)

Рис. 3 Проверка работы программы из листинга 9.1


После чего я изменю текст программы добавив изменение значения регистра ecx в цикле.

![Рис. 4 Изменение программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/4.%20%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0%209.1.png)

Рис. 4 Изменение программы

Проверю работу изменённой программы.

![Рис. 5 Запуск изменённой программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/5.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B%20%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D1%91%D0%BD%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0.png)

Рис. 5 Запуск изменённой программы


Снова внесу изменения в текст программы добавив команды push и pop для сохранения значения счётчика цикла loop.

![Рис. 6 Внесение изменениё в программу](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/6.%20%D0%92%20%D0%BE%D1%87%D0%B5%D1%80%D0%B5%D0%B4%D0%BD%D0%BE%D0%B9%20%D1%80%D0%B0%D0%B7%20%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D1%8E%20%D1%82%D0%B5%D0%BA%D1%81%D1%82%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B.png)

Рис. 6 Внесение изменениё в программу


Создам исполняемый файл и проверю его работу. В данном случае число проходов цикла не соответствует значению N введённому с клавиатуры.

![Рис. 7 Запуск исполняеиого файла с внесёнными изменениями](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/7.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BC%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D0%BD%D1%8F%D0%B5%D0%BC%D1%8B%D0%B9%20%D1%84%D0%B0%D0%B9%D0%BB%20%D0%B8%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D1%8E%20%D0%B5%D0%B3%D0%BE%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%83.png)

Рис. 7 Запуск исполняеиого файла с внесёнными изменениями


**Обработка аргументов командной строки**

Внимательно изучу текст программы из листинга 9.2, после чего создам файл lab9-2.asm и введу в него текст программы.

![Рис. 8 Ввод листинга 9.2](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/9.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0%209.2.png)

Рис. 8 Ввод листинга 9.2


Создам исполняемый файл и запущу его, предварительно указав аргументы. Программой было обработано три аргумента.

![Рис. 9 Запуск программы из листинга 9.3](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/10.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B.png)

Рис. 9 Запуск программы из листинга 9.3


Теперь создам файл lab9-3.asm в каталоге ~/work/arch-pc/lab09 и введу в него текст программы из листинга 9.3.

![Рис. 10 Ввод программы из листинга 9.3](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/11.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BC%20%D1%84%D0%B0%D0%B9%D0%BB%20lab9-3%20%D0%B8%20%D0%B2%D0%B2%D0%B5%D0%B4%D1%83%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%209.3.png)

Рис. 10 Ввод программы из листинга 9.3


Создам исполняемый файл и запущу его, указав аргументы: 12,13,7,10,5. В результате получу 47, что является правильным результатом.

![Рис. 11 Запуск программы из листинга 9.3](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab09/report/image/12.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B.png)

Рис. 11 Запуск программы из листинга 9.3


# Выводы

Я приобрёл навыки написания программ с использованием циклов и обработкой аргументов командной строки.
