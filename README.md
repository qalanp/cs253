
CS253 Интеллектуальные системы
=
Индивидуальные задания курса CS253 "Интеллектуальные системы" Института математики, механики и компьютерных наук Южного федерального университета.


**Задания:**

1. [**Поиск**](../../tree/master/search_in_state_space) решения в пространстве состояний. Решить вводные задачи поиска:
- Даны два целых числа – например, 2 и 100, а также две операции – «прибавить 3» и «умножить на 2». Найти минимальную последовательность операций, позволяющую получить из первого числа второе.
- То же самое, что и в пункте 1, однако добавляется операция «вычесть 2».
- Реализовать задание из пункта 1 методом обратного поиска – от целевого состояния к начальному. Сравнить эффективность.
- Дополнительное задание. Реализовать метод двунаправленного поиска для решения задачи из пункта 1.
       
 2. [**Пятнашки**](../../tree/master/fifteen):
Базовым является задание на решение игры «[Пятнашки](https://ru.wikipedia.org/wiki/%D0%98%D0%B3%D1%80%D0%B0_%D0%B2_15)» (15 фишек, поле 4x4), однако при возникновении сложностей с решением можно для начала попробовать найти решение для игры «8» (то же самое, фишки от 1 до 8, поле 3x3).
Напоминаю, что половина позиций являются нерешаемыми, условие решаемости позиции можно найти по ссылке выше.  
Общая схема работы программы выглядит следующим образом:  
	1. Пользователь вводит начальную расстановку. Для «15» начальную расстановку удобно задавать в шестнадцатеричном виде, где 0 – пустая ячейка, значения от 1 до F соответствуют фишкам с номерами от 1 до 15. Собранная позиция – 123456789ABCDEF0.
	2.  Программа проверяет введённую расстановку, и указывает, является ли она решаемой (если нет, то выход).
	3.  Ищем решение – минимальная по длине последовательность ходов, приводящая к решению (если находится не минимальная по длине последовательность, то решение не засчитывается!).
	4.  Выдаётся решение, по ходам, после каждого хода указывать очередную полученную позицию. Т.к. решения могут содержать довольно большое число ходов (поищите, чем равно «Число Бога» для «Пятнашек»), решение можно выводить не в консоль, а в текстовый файл.
