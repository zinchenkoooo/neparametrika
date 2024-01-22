# parametrika
Параметрика - один из методов статистики. 
Параметрика обозначает набор переменных, которые определяют состояние или характеристики системы или процесса. В математике и физике параметрика может использоваться для описания кривых, поверхностей или других геометрических объектов. В программировании параметрика может относиться к передаваемым значениям или настройкам, которые влияют на поведение программы или функции. В общем смысле, параметрика используется для описания зависимостей между переменными и другими элементами в различных областях науки и техники.
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
# 1)вначале рассчитывается среднее значение, 
# затем берется разница между каждым исходным и средним значением, 
# возводится в квадрат, складывается 
# и затем делится на количество значений в данной совокупности(дисперсия) 
# 2)извлекаем квадратный корень(среднее квадратичное отклонение)
```
Среднее квадратическое отклонение — статистическая характеристика распределения случайной величины, показывающая среднюю степень разброса значений величины относительно математического ожидания.

     Создание алгоритма классификации:
1) Подготовка данных
- Собрать данные о росте, длине волос и поле человека.
- Подготовить данные путем масштабирования и нормализации, если необходимо.
```python
import matplotlib

import matplotlib.pyplot as plt
x_girls = (158, 171, 163, 164, 162, 170, 160, 166, 175, 162, 165, 162, 167)
y_girls = (50, 43, 32, 36, 60, 45, 25, 34, 71, 63, 25, 32, 31)
plt.scatter(x_girls, y_girls)
x_boys = (182, 172, 168, 181, 186, 175, 180, 171, 177, 188)
y_boys = (5, 3, 2, 3, 6, 4, 10, 5, 2, 15)
plt.scatter(x_boys, y_boys)
plt.show()
```
![parametrika scatters](https://github.com/zinchenkoooo/neparametrika/assets/143995863/450b48b1-041d-4249-8fa2-77e45a38bec3)
2)Разделение данных
- Разделить данные на обучающий и тестовый наборы.

```python
import matplotlib

import matplotlib.pyplot as plt
x_girls = (158, 171, 163, 164, 162, 170, 160, 166, 175, 162, 165, 162, 167)
y_girls = (50, 43, 32, 36, 60, 45, 25, 34, 71, 63, 25, 32, 31)
plt.scatter(x_girls, y_girls)
x_boys = (182, 172, 168, 181, 186, 175, 180, 171, 177, 188)
y_boys = (5, 3, 2, 3, 6, 4, 10, 5, 2, 15)
plt.scatter(x_boys, y_boys)
x_girls1 = (173, 175)
y_girls1 = (23,44)
plt.scatter(x_girls1, y_girls1)
x_boys1 = (178, 175, 195)
y_boys1 = (10, 7, 8)
plt.scatter(x_boys1, y_boys1)
plt.show()
```
![photo1705959619](https://github.com/zinchenkoooo/neparametrika/assets/143995863/409d012a-f601-4059-b002-9ddfb9616849)
3) Построение модели
- Создать модель линейной регрессии, где рост, длина волос и пол будут использоваться в качестве независимых переменных (факторов), а классификация (мужчина/женщина) в качестве зависимой переменной.
- Обучить модель на обучающем наборе данных.
```python
import matplotlib
import matplotlib.pyplot as plt
x_girls = (158, 171, 163, 164, 162, 170, 160, 166, 175, 162, 165, 162, 167)
y_girls = (50, 43, 32, 36, 60, 45, 25, 34, 71, 63, 25, 32, 31)
plt.scatter(x_girls, y_girls)
x_boys = (182, 172, 168, 181, 186, 175, 180, 171, 177, 188)
y_boys = (5, 3, 2, 3, 6, 4, 10, 5, 2, 15)
plt.scatter(x_boys, y_boys)
x_girls1 = (173, 175)
y_girls1 = (23,44)
plt.scatter(x_girls1, y_girls1)
x_boys1 = (178, 175, 195)
y_boys1 = (10, 7, 8)
plt.scatter(x_boys1, y_boys1)
plt.show()
import numpy as np
from sklearn.linear_model import LinearRegression
#Создание обучающих данных
x_girls = np.array([[158], [171], [163], [164], [162], [170], [160], [166], [175], [162], [165],[162], [167]])
y_girls = np.array([50, 43, 32, 36, 60, 45, 25, 34, 71, 63, 25, 32, 31])
model = LinearRegression()
model.fit(x_girls, y_girls)
x_boys = ([[182], [172], [168], [181], [186], [175], [180], [171], [177], [188]])
y_boys = ([5, 3, 2, 3, 6, 4, 10, 5, 2, 15])
#Создание и обучение модели линейно регрессии
model = LinearRegression()
model.fit(x_boys, y_boys)
#Получение предсказаний
predictions = model.predict([[168], [2]])
```

