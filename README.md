# ADS-3 Исследование последовательности Коллатца


![GitHub pull requests](https://img.shields.io/github/issues-pr/NNTU-CS/ADS-3)
![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed/NNTU-CS/ADS-3)

Срок выполнения задания:

**по 30.03.2025** ![Relative date](https://img.shields.io/date/1743368400)


## Задание

> Написать программу, которая находит в диапазоне целых чисел от 2 до 1.000.000 число, формирующее самую длинную последовательность Коллатца

## Пояснение

Последовательностью Коллатца называют числовой ряд, каждый элемент которого формируется в зависимости от чётности/ нечётности предыдущего по закону:

1. n→(3n+1), если n - нечётное.
2. n→(n/2), если n - чётное

Начав отсчет с любого числа у нас формируется последовательность Коллатца, например:

```
1
2,1
3,10,5,16,8,4,2,1
4,2,1
5,
..
```

Генерация членов последовательности заканчивается, когда в конце ряда появляется единица. Количество элементов и составляет длину последовательности. В задаче надо перебирать в цикле числа от 2 до миллиона и для каждого считать длину последовательности. В конце необходимо вывести число, формирующего самую длинную последовательность, максимальное полученное число в ряду и длину этой последовательности.


**Состав проекта**

```C++
- unsigned int seqCollatz(unsigned int *maxlen, uint64_t lbound, uint64_t rbound) - функция, возвращающая число num, формирующую самую длинную последовательность и записывающую по адресу maxlen ее длину в диапазоне от lbound до rbound включительно
- unsigned int collatzLen(uint64_t num) - функция, возвращающая длину последовательности Коллатца для числа num 
- uint64_t collatzMaxValue(uint64_t num) - функция, возвращающая максимальное число в последовательности Коллатца для числа num
 ```



Функции должны располагаться в файле **src/alg.cpp**.