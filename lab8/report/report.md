---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе 8"
subtitle: "Собственные значения и цепи Маркова"
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

Научиться находить собственные значения матрицы в Octave и работать с цепями Маркова.

# Задание

Ознакомиться с командой eig для нахождения собственных значений в языке Octave, а затем применить полученные знания для решения цепей Маркова.


# Выполнение лабораторной работы

### Собственные значения

Ввел в Octave матрицу, приведенную в примере.  (рис. -@fig:001)

![рис.1 Ввод матрицы](image/1.png){ #fig:001 width=70% }

Вычислил матрицу собственных векторов и матрицу собственных значений (рис. -@fig:002)

![рис.2 При помощи команды eig вычислил матрицу s собственных векторов и матрицу \Lambda собственных значений по диагонали](image/2.png){ #fig:002 width=70% }

Затем, приведя матрицу к симметричной форме, вычислил действительные собственные значения (рис. -@fig:003)

![рис.3 При помощи умножения на транспонированную матрицу, привел ее к симмутричной форме, затем при помощи eig вычислил действительные собственные значения](image/3.png){ #fig:003 width=70% }

### Цепи Маркова

Теперь, когда я научился работать с вычислением собственных значений, можно работать в языке Octave с цепями Маркова. 

Для работы с цепями Маркова задал несколько начальных векторов и матрицу перехода. (рис. -@fig:004)

![рис.4 Начальные векторы a,b,c,d и матрица перехода T ](image/4.png){ #fig:004 width=70% }

Затем вычислил вектор конечного состояния после 5 переходов для всех векторов начальных состояний (рис. -@fig:005)

![рис.5 При помощи умножения матрицы Т в степени n на вектор начального состояния, где n - количество переходов, получаем векторы конечного состояния ](image/5.png){ #fig:005 width=70% }

Переходим к вычислению векторов равновесного состояния, задал матрицу перехода Т, после чего вычислил вектор х, являющийся вектором равновесия для этой матрицы. (рис. -@fig:006)

![рис.6 Задал матрицу Т, вычислил собственные значения, после чего нашел вектор равновесия х ](image/6.png){ #fig:006 width=70% }

Проверил полученный вектор равновесия. Результаты совпали с ожидаемыми. (рис. -@fig:007)

![рис.7 По условию, вектор х является вектором равновесного состояния, если при любом количестве переходов конечный вектор совпадает с исходным. При проверке условие выполняется, а значит, вектор х - вектор равновесного состояния. ](image/7.png){ #fig:007 width=70% }


# Выводы

Я ознакомился с нахождением собственных значений в Octave и применил это для решения цепей Маркова при помощи Octave.

# Использованные материалы

Методичка к лабораторной работе
