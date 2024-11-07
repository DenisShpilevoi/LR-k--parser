#include "5_7.cpp"

Реализация LR(k)-парсера.


Выполнена в соответствии с представленными алгоритмами в сборнике А. Ахо и Дж. Ульмана - Теория синтаксического анализа, перевода и компеляции, том 1

Реализация поделена на 6 алгоритмов, представленных в разделе пособия 5.2, названия cpp-файлов соответствуют номерам алгоритмов

Краткое описание алгоритмов:
- А л г о р и т м  5 5   -  Построение множества FIRST_k и EFF_k для произвольного k.
- А л г о р и т м  5 7   -  LR(k)-разбор входной цепочки w в имеющейся управляющей таблице.
- А л г о р и т м  5 8   -  Построение V_k_G - множества допустимых ситуаций для активного префикса.
- А л г о р и т м  5 9   -  Построение системы множеств допустимых ситуаций.
- А л г о р и т м  5 10  -  Проверка LR(k)-условия - нахождение наименьшего подходящего k для грамматики.
- А л г о р и т м  5 11  -  Построение управляющей таблицы (т.е. системы LR(k)-таблиц).


Формат ввода:

- Ввести набор правил через перенос строки;
- Эпсилон-правило - после "->" не писать ничего (пример: S-> );
- После последнего правила написать на новой строке символ '/';
- Терминалы - маленькие латинские символы, нетерминалы - большие латинские символы;
- Первый символ первого правила считается стартовым;

- Дальше ввести цепочку из терминальных символов. Программа выведет последовательность номеров правил, являющихся правым разбором входной цепочки;
- Вывод: последовательность номеров правил если слово есть в языке или -1 если слова нет;
- Слов можно разберать сколько угодно. При желании сменить грамматику перезапустить программу;
- По алгоритму добавляется системное правило $->S имеющее 0-вой номер, в конце каждого разбора будет записан номер 0.



Примеры:

1)

S->SaSb

S->

/ 

abab 

aabb

aaaaabaabbabaabaabbabbabaaabaabbaabbaabbabbaababbabbabbabbabbabaababbb

2)

S->C

S->D

C->aC

C->b

D->aD

D->c

/

b

aab

ac

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaab

