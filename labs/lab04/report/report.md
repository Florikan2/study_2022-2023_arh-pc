---
## Front matter
title: "Отчёт по лабораторной работе номер 4"
subtitle: "дисциплина: архитектура компьютера"
author: "Яковин ИЛья Андреевич"

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
Целью работы является освоение процедуры оформления отчётов с помощью легковесного языка разметки Markdown

# Задание

Здесь приводится описание задания в соответствии с рекомендациями
методического пособия и выданным вариантом.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно об Unix см. в [@gnu-doc:bash;@newham:2005:bash;@zarrelli:2017:bash;@robbins:2013:bash;@tannenbaum:arch-pc:ru;@tannenbaum:modern-os:ru].

# Выполнение лабораторной работы

**4.2 ВЫполнение лабораторной работы.**
4.2.1 Для начала открою терминал и перейду в каталог курса,который был создан при выполнении лабораторной работы номер 3. После этого я обновлю локальный репозиторий, скачав изменения из удалённого репозитория с помощью команды.
![Обновление локального репозитория](https://github.com/Florikan2/study_2022-2023_arh-pc/blob/master/labs/lab04/report/image/dit.png) { #fig:001 width=70% }

4.2.2  Дальше я перейду в каталлог с шаблоном отчёта по лабораторной номер 4.
![Каталог с шаблоном отчёта лабораторной работы номер 4](i/home/iayakovin/Изображения/Снимки экрана/kat.jpg){ #fig:001 width=70% }

4.2.3 Попытаюсь провести компиляцию шаблона с использованием Makefile (К сожалению выдаёт ошибку)
![Попытка компиляции шаблона](/home/iayakovin/Изображения/Снимки экрана/make.jpg){ #fig:001 width=70% }

4.2.4 Открою файл report.md с помощью текстового редактора. Внимательну изучу структуру этого файла.
![Файл report.md](/home/iayakovin/Изображения/Снимки экрана/report.jpg){ #fig:001 width=70% }


4.2.5 Загружу файлы на Github



# Выводы

Я освоил процедуры оформления отчётов с помощью легковесного языка разметки Markdown.

# Список литературы{.unnumbered}

::: {#refs}
:::
