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
                		  по лабораторной работе № 10
               		       дисциплина: Архитектура компьютера









                                          	   		Студент: Яковин И.А

	                                   	  		 Группа: НПИбд-02-22







                             			МОСКВА
			     			2022 г.




# Цель работы

Целью данной лабораторной работы является приобритение навыков написания программ с использованием подпрограмм. Познакомиться с методами отладки при помощи GDB и его основными возможностями.


# Выполнение лабораторной работы
**Реализация подпрограмм в NASM**

1. Создам каталог для выполнения лабораторной работый №10, перейду в него и создам файл lab10-1.asm

![Рис.1 Создание файла lab10-1.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/1.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20lab10.png)

Рис.1 Создание файла lab10-1.asm


2. Внимательно изучу текст программы из листинга 10.1 и введу его в файл lab10-1.asm

![Рис.2 Ввод программы из листинга 10.1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/2.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0%2010.1.png)

Рис.2 Ввод программы из листинга 10.1


3. Запущу программу листинга 10.2

![Рис.3 Запуск программы из листинга 10.2](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/3.%20%D0%9B%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%2010.1%20%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA.png)

Рис.3 Запуск программы из листинга 10.2


**Отладка программ с помощью GDB**

4. Создам файл lab10-2.asm с текстом программы из Листинга 10.2

![Рис.4 Ввод программы из листинга 10.2 ](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/5.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0%2010.2.png)

Рис.4 Ввод программы из листинга 10.2


5. Получу исполняемый файл

![Рис.5 Получениие исполняемого файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/6.%20%D0%9F%D0%BE%D0%BB%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D0%BD%D1%8F%D0%B5%D0%BC%D0%BE%D0%B3%D0%BE%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0.png)

Рис.5 Получениие исполняемого файла


6. Загружу исполняемый файл в отладчик gdb

![Рис.6 Загрузка исполняемого файла в отладчик GDB](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/7.%20%D0%97%D0%B0%D0%B3%D1%80%D1%83%D0%B7%D0%BA%D0%B0%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D0%BD%D0%B3%D1%8F%D0%B5%D0%BC%D0%BE%D0%B3%D0%BE%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20%D0%B2%20gdb.png)

Рис.6 Загрузка исполняемого файла в отладчик GDB

7. Проверю работу программы, запустив её в оболочке GDB с помощью команды run

![Рис.7 Проверка работы программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/8.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B.png)

Рис.7 Проверка работы программы


8. Установлю брейкпоинт на метку _start для более быстрого анализа программы.Затем посмотрю дисассимилированный код программы с помощью команды disassemble начиная с метки _start

![Рис.8 Установка брейкпоинта на метку _start и просмотр дисассимблированного кода](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/9.%20%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BB%D1%8E%20%D0%B1%D1%80%D0%B5%D0%B9%D0%BA%D0%BF%D0%BE%D0%B8%D0%BD%D1%82%20%D0%B8%20%D0%BF%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80%D1%8E%20%D0%B4%D0%B8%D1%81%D1%81%D0%B0%D0%BC%D0%B1%D0%BB%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B9%20%D0%BA%D0%BE%D0%B4.png)

Рис.8 Установка брейкпоинта на метку _start и просмотр дисассимблированного кода


9. Переключусь на отображение команд с intel'овским синтаксисом. Для этого введу команду set disassembly-flavor intel

![Рис.9 Переключение на отображение команд intel'овским способом](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/10.%20%D0%9F%D0%B5%D1%80%D0%B5%D0%BA%D0%BB%D1%8E%D1%87%D1%83%D1%81%D1%8C%20%D0%BD%D0%B0%20%D1%81%D0%B8%D0%BD%D1%82%D0%B0%D0%BA%D1%81%D0%B8%D1%81%20intel.png)

Рис.9 Переключение на отображение команд intel'овским способом

10. Включу режим псевдографики для более удобного анализа программы.

![Рис.10 Включение режима псевдографики](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/11.%20%D0%92%D0%BA%D0%BB%D1%8E%D1%87%D1%83%20%D1%80%D0%B5%D0%B6%D0%B8%D0%BC%20%D0%BF%D1%81%D0%B5%D0%B2%D0%B4%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B8.png)

Рис.10 Включение режима псевдографики


**Добавление точек останова**

11. Просмотрю информацию о установленных брейкпоинтах

![Рис.11 Просмотр установленных брейкпоинтов ](image/placeimg_800_600_tech.jpg)

Рис.11 Просмотр установленных брейкпоинтов


12. Определю адрес предпоследней инструкции и установлю точку останова.

![Рис.12 Установка точки остановы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/13.%20%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BB%D1%8E%20%D0%B5%D1%89%D1%91%20%D0%BE%D0%B4%D0%BD%D1%83%20%D1%82%D0%BE%D1%87%D0%BA%D1%83%20%D0%BE%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B8.png)

Рис. 12 Установка точки остановы


**Работа с данными программы в GDB**

13. Посмотрю содержимое регистров 

![Рис.13 Просмотр регистров](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/14.%20%D0%98%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D1%8F%20%D0%BE%20%D1%80%D0%B5%D0%B3%D0%B8%D1%81%D1%82%D1%80%D0%B0%D0%B7.png)

Рис.13 Просмотр регистров

14. Посмотрю значение переменной msg1 по имени

![Рис.14 Просмотр значения переменной msg1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/15.%20%D0%9F%D1%80%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80%20%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B8%D0%BC%D0%BE%D0%B3%D0%BE%20%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D0%BE%D0%B9%20msg1%20%D0%BF%D0%BE%20%D0%B8%D0%BC%D0%B5%D0%BD%D0%B8.png)

Рис.14 Просмотр значения переменной msg1


15. Изменю первый символ переменной msg1

![Рис.15 Изменение символа переменной msg1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/16.%20%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D1%8E%20%D0%BF%D0%B5%D1%80%D0%B2%D1%83%D1%8E%20%D0%B1%D1%83%D0%BA%D0%B2%D1%83%20%D0%B2%20msg1.png)

Рис.15 Изменение символа переменной msg1


16.  Аналогично заменю первый символ во второй переменной msg2

![Рис. 16 Изменение символа переменной msg2](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/17.%20%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D1%8E%20%D0%BF%D0%B5%D1%80%D0%B2%D1%8B%D0%B9%20%D1%81%D0%B8%D0%BC%D0%B2%D0%BE%D0%BB%20%D0%B2%20msg2.png)

Рис. 16 Изменение символа переменной msg2


17. Выведу в различных форматах значения регистра edx

![Рис.17 Вывод значения регистра edx](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/18.%20%D0%92%D1%8B%D0%B2%D0%B5%D0%B4%D1%83%20%D0%B2%20%D1%80%D0%B0%D0%B7%D0%BB%D0%B8%D1%87%D0%BD%D1%8B%D1%85%20%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%82%D0%B0%D1%85%20edx.png)

Рис.17 Вывод значения регистра edx


18. С помощью команды set изменю значение регистра ebx

![Рис.18 Изменение значения регистра ebx](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/19.%20%D0%A1%20%D0%BF%D0%BE%D0%BC%D0%BE%D1%89%D1%8C%D1%8E%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B%20set%20%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D1%8E%20%D0%B7%D0%BD%D0%B0%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%20edx.png)

Рис.18 Изменение значения регистра ebx



19. Завершу выполнение программы с помощью команды stepi и выйду из GDB с помощью команды quit.

![Рис.19 Завершение программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/20.%20%D0%97%D0%B0%D0%B2%D0%B5%D1%80%D1%88%D1%83%20%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B.png)

Рис.19 Завершение программы


**Обработка аргументов командной строки в GDB**

20. Скопирую файл lab9-2.asm в файл с именем lab10-3.asm

![Рис.20 Копирование файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/21.%20%D0%A1%D0%BA%D0%BE%D0%BF%D0%B8%D1%80%D1%83%D1%8E%20%D1%84%D0%B0%D0%B9%D0%BB%20lab9-2.asm.png)


Рис.20 Копирование файла


21. Создам исполняемый файл 

![Рис.21 Создание исполняемого файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/22.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BC%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D0%BD%D1%8F%D0%B5%D0%BC%D1%8B%D0%B9%20%D1%84%D0%B0%D0%B9%D0%BB.png)

Рис.21 Создание исполняемого файла


22. Загружу исполняемый файл в отладчик, указав аргументы 

![Рис.22 Загрузка файла в отладчик](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/23.%20%D0%97%D0%B0%D0%B3%D1%80%D1%83%D0%B6%D1%83%20%D0%B2%20gdb.png)

Рис.22 Загрузка файла в отладчик

23. Установлю точку останова перед первой инструкцией в программе и запущу её

![Рис.23 Установка точки останова](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/24.%20%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BB%D1%8E%20%D1%82%D0%BE%D1%87%D0%BA%D1%83%20%D0%BE%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B0%20%D0%B8%20%D0%B7%D0%B0%D0%BF%D1%83%D1%89%D1%83%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%83.png)

Рис.23 Установка точки останова


24. Найду адрес вершины стека.

![Рис.24 Адрес вершины стека](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab10/report/image/25.%20%D0%9D%D0%B0%D0%B9%D0%B4%D1%83%20%D0%B0%D0%B4%D1%80%D0%B5%D1%81%20%D0%B2%D0%B5%D1%80%D1%88%D0%B8%D0%BD%D1%8B%20%D1%81%D1%82%D0%B5%D0%BA%D0%B0.png)

Рис.24 Адрес вершины стека


# Выводы

Я приобрёл навыки написания программ с использованием подпрограмм. ПОзнакомился с методами отладки при помощи GDB и его основными возможностями. 


