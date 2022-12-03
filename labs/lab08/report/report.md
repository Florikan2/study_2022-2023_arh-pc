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
                             по лабораторной работе № 8
                         дисциплина: Архитектура компьютера	









                                             Студент: Яковин И.А                                       

	                                     Группа: НПИбд-02-22







                                      МОСКВА
                                      2022 г.
                                      

# Цель работы

 Целью данной работы является изучение команд условного и безусловного переходов. Приобретение навыков написания программ с использованием переходов. Знакомство с назначением и структурой файла листинга.

# Выполнение лабораторной работы

**Реализация переходов в NASM**

1. Создам каталог для программ лабораторной работы №8, перейду в него и создам файл lab8-1.asm


![ Рис. 1 Создание файла lab8-1.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/1.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0.png) 


2. Введу в файл lab8-1.asm текст программы из листинга 8.1

![ Рис. 2 Вводи текста программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/2.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0.png) 


3. Создам исполняемый файл и запущу его. Проверю результат программы.

![ Рис. 3 Проверка результата программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/3.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%B8%20%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA.png)


4. Изменю программу таким образом,чтобы она выводила сначала "Сообщение № 2" потом "Сообщение №3" и завершала работу. Для этого изменю текст программы в соответсвтвии с листингом 8.2

![ Рис. 4 Изменение программы ](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/4.%20%D0%9B%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%202.png)


![ Рис. 5 Проверка результата ](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/5.%20%D0%9F%D1%80%D0%BE%D0%B2%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0.png)


5. Изменю текст программы добавив инструкцию jmp, чтобы вывод программы начинался с сообщения номер 3 и заканчивался сообщением номер 1.

![ Рис. 6 Вывод сообщений в обратном порядке ](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/5.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0.png)


6. Создам файл lab8-2.asm в каталоге ~/work/arch-pc/lab08. Внимательно изучу текст программы из листинга 8.3 и введу его в lab8-2.asm

![ Рис. 7 Ввод текста программы из листинга 8.3](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/6..%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BC%20lab7-2%20%D0%B8%20%D0%B2%D0%B2%D0%B5%D0%B4%D1%83%20%D1%82%D0%B5%D0%BA%D1%81%D1%82%20%D0%B8%D0%B7%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0.png)


7. Создам исполняемый файл и проверю его работу для разных значений B.

![ Рис. 8 Проверка работы программы из листинга 8.3](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/7.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B0%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B.png)

**Изучение структуры файлы листинга**

8. Создам файл листинга для программы из файла lab8-2.asm

![ Рис. 9 Создание файла листинга](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/8.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0.png)


9. Открою файл листинга lab8-2.lst с помощью текстового редакора mcedit

![ Рис. 10 Открытие файла листинга lab8-2.lst](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab08/report/image/9.%20%D0%9E%D1%82%D0%BA%D1%80%D0%BE%D1%8E%20%D1%84%D0%B0%D0%B9%D0%BB%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0.png)

10. Внимательно ознакомлюсь с его форматом и содержимым. Объясню содержимое трёх строк файла листинга по выбору.
Строка 5. A dd '20' присваивает А значение 20.
Строка 6. C dd '50' аналогично строке 5 присваивает B значение 50.
Строка 24. mov [B],eax запись преообразованного числа в 'B'
# Выводы

Я изучил команды условного и безусловного переходов. Приобрёл навыки написания программ с использованием переходов. Познакомился с назначением и структурой файла листинга.


