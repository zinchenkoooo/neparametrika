# parametrika
Параметрика - один из методов статистики. 
Парметрическая статсистика 
Параметрический анализ данных – математический подход, используемый для определения параметров статистической модели на основе данных. Это позволяет нам получить более точную информацию о характеристиках выборки и определить, насколько вероятны результаты нашей модели.
1) Параметрика - это один из методов статистики, необходимый для распределения данных Статистические методы делятся на параметрику и на непараметрику.
2) Сравнить параметрику и непараметрику параметрика - данные, подчиненные определенному закону распределения непараметрика (закон распределения данных неизвестен).
3) Создать массив из 10 случайных чисел найти медиану.


```python
from random import randint # импорт метода 'randint' из библиотеки 'random' для генерации случайного числа в промежутке от а до b

a = [] # создание массива
for i in range(10): # цикл который сделает то что в нём 10 раз
    b = randint(-5, 5) # генерация случайного числа
    a.append(b)   # добавление его в массив
a.sort() # сортировка масссива по возрастанию
print((a[4] + a[5]) / 2) # вывод медианы массива(нахождение среднего арифметического двух средних чисел медианы массива)
```
                среднее арифметическое и дисперсия и среднее квадратинчое отклонение 
```python
numbers = [175, 162, 177, 165, 162, 167]
average = sum(numbers) / len(numbers)
print(average) # среднее арифметическое 
a = numbers[0] - average
b = numbers[1] - average
c = numbers[2] - average
d = numbers[3] - average
e = numbers[4] - average
f = numbers[5] - average
print(((a ** 2 + b ** 2 + c ** 2 + d ** 2 + e ** 2 + f ** 2) / len(numbers) **0.5))
# То есть вначале рассчитывается среднее значение, затем берется разница между каждым исходным и средним значением, возводится в квадрат, складывается и затем делится на количество значений в данной совокупности(дисперсия)
```
Среднеквадратическое отклонение — статистическая характеристика распределения случайной величины, показывающая среднюю степень разброса значений величины относительно математического ожидания.
нужно сделать гистаграму из значений 
Этап 5: Извлекаем квадратный корень.
