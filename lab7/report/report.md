---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе 7"
subtitle: "Построение различных графиков в языке Octave"
author: "Илья Валерьевич Фирстов"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Ознакомиться с построением графиков различных уравнений в языке Octave.

# Задание

Построить графики заданных уравнений при помощи Octave. 

# Выполнение лабораторной работы

### Параметрические графики

Ввел параметрическое уравнение циклоиды (рис. -@fig:001)

![рис.1 Уравнение циклоиды](image/1.png){ #fig:001 width=70% }

На основе этого уравнения построил график (рис. -@fig:002)

![рис.2 График циклоиды](image/cycloid.png){ #fig:002 width=70% }

### Полярные координаты

Ввел уравнение улитки Паскаля в полярных координатах (рис. -@fig:003)

![рис.3 Уравнение улитки Паскаля](image/2.png){ #fig:003 width=70% }

На основе этого уравнения выполнил преобразование в декартову систему координат(рис. -@fig:004)

![рис.4 Преобразование x = r*cos(t), y = r*sin(t)](image/3.png){ #fig:004 width=70% }

После этого построил график в декартовых координатах (рис. -@fig:005)

![рис.5 Улитка Паскаля в декартовых координатах ](image/limacon.png){ #fig:005 width=70% }

Затем при помощи команды polar построил график без преобразования в декартовы координаты(рис. -@fig:006)

![рис.6 Построение улитки Паскаля в полярных координатах при помощи polar ](image/limacon2.png){ #fig:006 width=70% }


### Графики неявных функций

Ввел предложенную в методичку функцию, неявно определенную уравнением вида f(x,y) = 0 (рис. -@fig:007)

![рис.7 Первая неявная функция ](image/4.png){ #fig:007 width=70% }

Построил ее графику при помощи функции ezplot (рис. -@fig:008)

![рис.8 Построение графика первой функции](image/impl1.png){ #fig:008 width=70% }

Ввел приведенное в методичке уравнение окружности (рис. -@fig:009)

![рис.9 Уравнение окружности](image/5.png){ #fig:009 width=70% }

Построил график функцией ezplot (рис. -@fig:010)

![рис.10 График окружности](image/impl2.png){ #fig:010 width=70% }

Ввел уравнение касательной к этой окружности (рис. -@fig:011)

![рис.11 Уравнение касательной ](image/6.png){ #fig:011 width=70% }

Построил график этой касательной (рис. -@fig:012)

![рис.12 График касательной ](image/impl3.png){ #fig:012 width=70% }

### Комплексные числа

Ознакомился с операциями с комплексными числами в Octave (рис. -@fig:013)

![рис.13 Операции с комплексными числами ](image/7.png){ #fig:013 width=70% }

Построил график комплексных чисел и их линейных комбинаций (рис. -@fig:014)

![рис.14 График комплексных чисел, построенный при помощи команды compass ](image/complex.png){ #fig:014 width=70% }

Ознакомился с поведением Octave при вычислении различных корней (рис. -@fig:015)

![рис.15 График касательной ](image/8.png){ #fig:015 width=70% }

### Специальные функции

Чтобы построить графики гамма-функции и функции факториала, определил n и x (рис. -@fig:016)

![рис.16 Задание n и x ](image/9.png){ #fig:016 width=70% }

Построил в одном пространстве факториал и гамма-функцию (рис. -@fig:017)

![рис.17 Факториал и гамма-функция ](image/gamma.png){ #fig:017 width=70% }

Чтобы избавиться от артефактов построения в виде вертикальных асимптот, определил несколько отрезков и построил гамма-функцию на этих отрезках (рис. -@fig:018)

![рис.18 Функции построения графиков на нескольких отрезках ](image/10.png){ #fig:018 width=70% }

Итоговый вид графиков получился следующий. (рис. -@fig:019)

![рис.19 Факториал и гамма-функция, окончательный вид ](image/gamma2.png){ #fig:019 width=70% }

# Выводы

Я ознакомился с построением графиков различных матемтических функций в языке Octave.

# Использованные материалы

Методичка к лабораторной работе
