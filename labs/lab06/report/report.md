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

# Цель работы

 Целью данной лабораторной работы является приобретение практических навыков работы Midnight Commander. Освоение инструкций языка ассемблера mov и int.
 
# Титульный лист

                                                                                          РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
                                                                                      Факультет физико-математических и естественных наук
                                                                                      Кафедра прикладной информатики и теории вероятностей





                                                                                                           ОТЧЕТ 
                                                                                                   по лабораторной работе № 6
                                                                                             дисциплина:   Архитектура компьютера	









                                                                                                                                     Студент: Яковин И.А

	                                                                                                                             Группа: НПИбд-02-22







                                                                                                          МОСКВА
                                                                                                          2022 г.

# Выполнение лабораторной работы

1. Открою Midnight Commander

![Открытие Midnight Commander](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/1.%D0%9E%D1%82%D0%BA%D1%80%D1%8B%D1%82%D0%B8%D0%B5%20mc.png)


2. Перейду в каталог ~/work/arch-pc

![Окно Midnight Commander. Смена текущего каталога](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/2.%20%D0%9F%D0%B5%D1%80%D0%B5%D1%85%D0%BE%D0%B4%20%D0%B2%20%D0%BA%D0%B0%D1%82%D0%B0%D0%BB%D0%BE%D0%B3%20arch-pc.png)


3. С помощью функциональной клавиши F7 создам папку lab06

![Создание каталога lab06](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/3.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BF%D0%B0%D0%BF%D0%BA%D0%B8%20lab06.png)


4. Пользуясь строкой ввода и командой touch создам файл lab1.asm

![Создание файла lab6.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/4.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20lab6.asm.png)


5. С помощью функциональной клавиши F4 открою файл lab6.asm с помощью редактора mcedit.

![Открытие файла lab6.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/5.%20%D0%9E%D1%82%D0%BA%D1%80%D0%BE%D1%8E%20%D1%84%D0%B0%D0%B9%D0%BB%20%D0%B4%D0%BB%D1%8F%20%D1%80%D0%B5%D0%B4%D0%B0%D0%BA%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F.png)


6. Введу текст программы из листинга 6.1, затем сохраню изменения 

![Ввод текста программы](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/6.%20%D0%92%D0%B2%D0%BE%D0%B4%20%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B.png)


7. С помощью функциональной клавиши F3 откроою файл lab6.asm для просмотра. Убежусь в том, что файл содержит текст программы.

![Открытие файла с помощью функциональной клавиши F3](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/7.%20F3%20%D1%83%D0%B1%D0%B5%D0%B6%D1%83%D1%81%D1%8C%20%D0%B2%20%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B8%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0.png)


8. Оттранслирую текст программы lab6.asm в объектный файл.Затем выполню компоновку объектного файла и запущу получившийсся исполняемый файл.

![Запуск исполняемого файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/8.%20%D0%9E%D1%82%D1%82%D1%80%D0%B0%D0%BD%D1%81%D0%BB%D0%B8%D1%80%D1%83%D1%8E%20%D1%82%D0%B5%D0%BA%D1%81%D1%82.png)


** Подлдключение внешнего файла in_out.asm **

9. Скачаю файл in_out.asm со страницы курса в ТУИС. После этого скопирую файл in_out.asm в каталог с файлом lab6.asm с помощью функциональной клавиши F5.

![Копирование файла in_out.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/9.%20%D0%9F%D0%B5%D1%80%D0%B5%D0%BD%D0%BE%D1%81%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20in_out.png)


10. С помощью функциональной клавиши F6 создам копию файла lab6.asm с именем lab6-2.asm и нажму клавишу Enter.

![Создание копии файла lab1.asm](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/10.%20%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BA%D0%BE%D0%BF%D0%B8%D0%B8%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%20lab6.png)


11. Исправлю текст программы в файле lab6-2.asm с использованием программ из внешнего файла in_out.asm. 

![Исправление текста файла](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/11.%20%D0%98%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D1%8E%20%D1%82%D0%B5%D0%BA%D1%81%D1%82%20%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D1%8B.png)


12. Создам исполняемый файл и проверю его работу.

![Создание исполняемого файла и его запуск](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab06/report/image/12.%20%D0%9F%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D1%8E%20%D0%B5%D0%B3%D0%BE%20%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%83.png)


# Выводы

В ходе выполнения лабораторной работы я приобрёл практические навыки работы в Midnight Commander и освоил инструкции языка ассемблера mov и int.


