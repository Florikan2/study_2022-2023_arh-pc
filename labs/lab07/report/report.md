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
                                                                     по лабораторной работе № 7
                                                               дисциплина:  Архитектура компьютера	 









                                                                                                   Студент: Яковин И.А                      
                                                                                                   Группа: НПИбд-02-22







                                                                              МОСКВА
                                                                              2022 г.
# Цель работы

Освоение арифметических инструкций языка ассеблера NASM.

# Выполнение лабораторной работы

**Символьные и численные данные в NASM**

1. Создам каталог для программ лабораторной работы номер 7, перейду в него и создам файл lab7-1.asm

![Рис. 1.1 Создание файла lab7-1.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/1.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0%20.png)


2. Введу в файл lab7-1.asm текст программы из листинга 7.1.

![Рис. 1.2 Ввод текста программы из листинга 7.1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/2.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0.png)

3. Создам исполняемый файл и запущу его.

![Рис. 1.3 Создание и запуск исполняемого файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/3.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%B8%20%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA.png)


4. Изменю текст программы и вместо символов запишу в регистре числа. Создам исполняемый файл и запущу его.Символ не отображается на экране.

![Рис. 1.4 Запуск изменённого файла lab7-1](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/4.%20%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F%20%D1%81%20%D0%BE%D1%82%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5%D0%BC.png)


5. Создам файл lab7-2.asm в каталоге ~/work/arch-pc/lab07 и введу в него текст программы из листинга 7.2.

![Рис. 1.5 Ввод текста программы из листинга 7.2](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/5.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0%207.2.png)


6. Создам исполняемый файл и запущу его.

![Рис. 1.6 Создание и запуск исполняемого файла lab7-2](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/6.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%B8%20%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA.png)


7. Как и в прошлом примере изменю символы на числа. Создам исполняемый файл и запущу его. Результат изображён на рисунке снизу.

![Рис. 1.7 Изменение файла и вывод результата](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/7.%20%D0%98%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F.png)


8. Заменю функцию iprintLF на iprint. Создам исполняемый файл и запущу его. Различие в выводе между этими функциями состоит в том,что iprintLF работает аналогично iprint, но при выводе на экран после числа добавляет к символ перевода строки. Cоздам исполняемый файл и запущу его

![Рис. 1.8 Замена iprintLF на iprint](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/8.%20iprint.png)


**Выполнение арифметических операций в NASM**

9. Создам файл lab7-3.asm в каталоге ~/work/arch-pc/lab07. Внимательно прочитаю текст программы и введу его в lab7-3.asm

![Рис. 1.9 Ввод текста в файл lab7-3.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/9.%20%D0%9B%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%207.3.png)


10. Создам исполняемый файл и запущу его.

![Рис. 1.10 Создание и запуск исполняемого файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/10.%20%D0%97%D0%B0%D0%BF%D1%83%D1%81%D0%BA%20%D0%B0%D1%80%20%D1%83%D1%80.png)


11. Изменю текст программы для выражения f(x)=(4*6+2)/5. Создам исполняемый файл и проверю его работу.

![Рис. 1.11 Изменение выражения](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/11.%20%D0%94%D1%80%D1%83%D0%B3%D0%BE%D0%B5%20%D1%83%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5.png)


12. Создам файл variant.asm в каталоге ~/work/arch-pc/lab07/variant.asm.

![Рис. 1.12 СОздание файла variant.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/12.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20variant.asm.png)


13. Внимательно изучу текст программы из листинга 7.4 и введу в файл variant.asm.

![Рис. 1.13 Ввод текста программы из листинга 7.4](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/13.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D0%BB%D0%B8%D1%81%D1%82%D0%B8%D0%BD%D0%B3%D0%B0%207.4.png)


14. Создам исполняемый файл и запущу его. После чего проверю результат работы программы вычислив номер варианта аналитически. Всё сходится.

![Рис. 1.14 Вывод результата](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab07/report/image/14.%20%D0%A4%D0%B8%D0%BD%D0%B8%D1%88.png)


15. Ответы на вопросы.

15.1 Какие строки листинга 7.4 отвечают за вывод на экран сообщения 'Ваш вариант: ' ?.
Ответ: Строки mov eax,rem
              call sprint
              mov eax,edx
              call iprintLF
              
15.2 Для чего используется инструкция "call atoi" ?
Ответ: Функция "call atoi" используется для преобразования символов в числа.

15.3 Какие строки листинга 7.4 отвечают за вычисления варианта?
Ответ: mov eax,x
       call atoi
       
       xor edx,edx
       mov ebx,20
       div ebx
       inc edx
       
15.4 В какой регистр записывается остаток от деления при выполнении инструкции "div ebx"?
Ответ: EAX

15.5 Для чего используется инструкция "inc edx"?
Ответ: Для инкремента edx

15.6 Какие строки листинга 7.4 отвечают за вывод на экран результата вычислений? 
Ответ: mov eax,rem
       call sprint
       mov eax,edx
       call iprintLF

# Выводы
Я освоил арифметические инструкции языка ассемблера NASM.

