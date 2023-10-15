# Тема 4. Функции и модули 
Отчет по Теме #4 выполнил(а):
- Глушков Михамл Сергеевич
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | |
| Задание 7 | + | |
| Задание 8 | + |  |
| Задание 9 | + |  |
| Задание 10 | + |  |

# Лабараторные работы 
   ## Лабараторная работа 1
Напишите функцию, которая выполняет любые арифметические действия и выводит результат в консоль. Вызовите функцию используя “точку входа”.

  ```python
def main():
    print(2+2)
if __name__ =="__main__":
    main()
```
  ### Результат
  ![1](https://github.com/Mikhail867/Software_Engineering/assets/144737787/a9cf8add-f429-496c-b6d0-115c65824997)

 
## Краткий вывод:
def main(): - Здесь определена функция main. Это просто блок кода, который можно вызвать позже.

print(2+2) - Эта строка выводит результат сложения 2 и 2 на экран. В данном случае, это будет 4.

if __name__ =="__main__": - Это условие проверяет, запущен ли скрипт напрямую, а не импортирован ли он в другой скрипт. Если скрипт запущен напрямую, то выполняется следующий блок кода.

main() - Здесь вызывается функция main(), которая, в свою очередь, выполняет команду print(2+2).


   ## Лабараторная работа 2
Напишите функцию, которая выполняет любые арифметические действия, возвращает при помощи return значение в место, откуда вызывали функцию. Выведите результат в консоль. Вызовите функцию используя “точку входа”.

  ```python
def main():
    return (2+2)
if __name__ =="__main__":
    print(main())
```
  ### Результат
  ![2](https://github.com/Mikhail867/Software_Engineering/assets/144737787/33df444f-4c00-4809-9330-75fd813b69fc)

 
## Краткий вывод:
def main(): - Определена функция main.

return (2+2) - В этот раз функция возвращает результат сложения 2 и 2. То есть, она возвращает значение 4.

if __name__ =="__main__": - Это условие проверяет, запущен ли скрипт напрямую.

print(main()) - Если скрипт запущен напрямую, то вызывается функция main() и ее результат (в данном случае, число 4) выводится на экран.


   ## Лабараторная работа 3
Напишите функцию, в которую передаются два аргумента, над ними производится арифметическое действие, результат возвращается туда, откуда эту функцию вызывали. Выведите результат в консоль. Вызовите функцию в любом небольшом цикле. На скриншоте ниже приведен пример программы, в которой аргумент функции “x“превращается в параметр “one”, то же самое происходит

  ```python
def main(one,two):
    result = one+two
    return result
for i in range(5):
    x=1
    y=10
    answer=main(x,y)
    print(answer)
```
  ### Результат
  ![3](https://github.com/Mikhail867/Software_Engineering/assets/144737787/3d467d6c-f7b1-46e4-8fc5-7ba4fa159d4e)

 
## Краткий вывод:
ef main(one, two): - Определена функция main с двумя параметрами one и two.

result = one + two - Внутри функции происходит сложение параметров one и two, результат сохраняется в переменной result.

return result - Функция возвращает значение переменной result.

for i in range(5): - Этот цикл for выполняется 5 раз (от 0 до 4).

x = 1 и y = 10 - В каждой итерации цикла создаются переменные x и y с соответствующими значениями.

answer = main(x, y) - Функция main вызывается с аргументами x и y, результат сохраняется в переменной answer.

print(answer) - Результат выводится на экран.


   ## Лабараторная работа 4
Напишите функцию, на вход которой подается какое-то изначальное неизвестное количество аргументов, над которыми будет производится арифметические действия. Для выполнения задания необходимо использовать кортеж “*args”. На скриншоте ниже приведен пример такой программы с комментариями. Для закрепления понимания работы с кортежами настоятельно рекомендуем поменять аргументы вызова функции, вручную посчитать результат, только потом запустить программу с новыми значениями и проверить себя, насколько вы поняли данный аспект программирования.

  ```python
def main(x,*args):
    one = x
    two =sum(args)
    three=float(len(args))
    print(f"one={one}\ntwo={two}\nthree={three}")
    return x + sum(args)/ float(len(args))

if __name__ =="__main__":
    result = main(10,0, 1, 2, -1, 0, -1, 1 ,2)
    print(f"\nresult={result}")
```
  ### Результат
  ![4](https://github.com/Mikhail867/Software_Engineering/assets/144737787/2cbf59d3-a5e6-432c-8931-9f3e92324623)

 
## Краткий вывод:
def main(x, *args): - Определена функция main с параметром x и *args, что позволяет функции принимать произвольное количество позиционных аргументов.

one = x - Переменной one присваивается значение параметра x.

two = sum(args) - Переменной two присваивается сумма всех позиционных аргументов (args).

three = float(len(args)) - Переменной three присваивается длина списка args в виде числа с плавающей точкой.

print(f"one={one}\ntwo={two}\nthree={three}") - Выводятся значения переменных one, two, и three.

return x + sum(args) / float(len(args)) - Функция возвращает результат сложения x и среднего значения аргументов args.

if __name__ =="__main__": - Это условие проверяет, запущен ли скрипт напрямую.

result = main(10, 0, 1, 2, -1, 0, -1, 1, 2) - Функция main вызывается с аргументами, и результат сохраняется в переменной result.

print(f"\nresult={result}") - Результат выводится на экран.

Таким образом, программа выводит значения переменных one, two, и three, а затем выводит результат вычислений функции main с конкретными аргументами.


   ## Лабараторная работа 5
Напишите функцию, которая на вход получает кортеж “**kwargs” и при помощи цикла выводит значения, поступившие в функцию. На скриншоте ниже указаны два варианта вызова функции с “**kwargs” и два варианта работы с данными, поступившими в эту функцию. Комментарии в коде и теоретическая часть помогут вам разобраться в этом нелегком аспекте. Вызовите функцию используя “точку входа”

  ```python
def main(**kwargs):
    for i in kwargs.items():
        print(i[0], i[1])
    print()
    for key in kwargs:
        print(f"{key}= {kwargs[key]}")
if __name__ == "__main__":
    main(x=[1,2,3], y=[3,3,0], z=[2,3,0], q=[3,3,0], w=[3,3,0])
    print()
    main(**{"x": [1,2,3], "y":[3,3,0]})
```
  ### Результат
  ![5](https://github.com/Mikhail867/Software_Engineering/assets/144737787/b99bf24a-40a1-441f-b9de-7002a095bc02)


## Краткий вывод:
def main(**kwargs): - Определена функция main с **kwargs, позволяющим передавать произвольное количество именованных аргументов.

for i in kwargs.items(): - В этом цикле происходит перебор элементов словаря kwargs, представленного в виде пар ключ-значение. Каждая пара выводится на экран.

print(i[0], i[1]) - Выводится ключ (i[0]) и значение (i[1]) каждого элемента kwargs.

print() - Пустая строка для создания отступа между двумя частями вывода.

for key in kwargs: - Второй цикл перебирает ключи в kwargs.

print(f"{key}= {kwargs[key]}") - Выводится каждый ключ и соответствующее значение.

if __name__ == "__main__": - Это условие проверяет, запущен ли скрипт напрямую.

main(x=[1,2,3], y=[3,3,0], z=[2,3,0], q=[3,3,0], w=[3,3,0]) - Функция main вызывается с именованными аргументами, представляющими собой словарь.

print() - Пустая строка для создания отступа.

main(**{"x": [1,2,3], "y":[3,3,0]}) - Функция main вызывается с использованием двойной звездочки для распаковки словаря в именованные аргументы. 


   ## Лабараторная работа 6
Напишите две функции. Первая – получает в виде параметра “**kwargs”. Вторая считает среднее арифметическое из значений первой функции. Вызовите первую функцию используя “точку входа” и минимум 4 аргумента.

  ```python
def main (**kwargs):
    for i,j in kwargs.items():
        print(f"{i}. Mean = {mean(j)}")
def mean(data):
    return sum(data)/float(len(data))
if __name__ == '__main__':
    main(x=[1,2,3], y=[3,3,0])
```
  ### Результат
  ![6](https://github.com/Mikhail867/Software_Engineering/assets/144737787/d9c5e02b-be73-4f1c-b15a-c322ac9fab9e)

 
## Краткий вывод:
def main(**kwargs): - Определена функция main с **kwargs, что позволяет передавать произвольное количество именованных аргументов.

for i, j in kwargs.items(): - В этом цикле переменные i и j получают значения ключа и соответствующего значения из словаря kwargs.

print(f"{i}. Mean = {mean(j)}") - Для каждой пары ключ-значение вызывается функция mean(j), которая рассчитывает среднее значение для значения аргумента, и выводится результат.

def mean(data): - Определена функция mean, которая принимает список чисел и возвращает их среднее значение.

return sum(data)/float(len(data)) - Функция mean рассчитывает среднее значение как сумму элементов списка, деленную на количество элементов.

if __name__ == '__main__': - Это условие проверяет, запущен ли скрипт напрямую.

main(x=[1,2,3], y=[3,3,0]) - Функция main вызывается с двумя именованными аргументами, представляющими собой словарь.

   ## Лабараторная работа 7
Создайте дополнительный файл .py. Напишите в нем любую функцию, которая будет что угодно выводить в консоль, но не вызывайте ее в нем. Откройте файл main.py, импортируйте в него функцию из нового файла и при помощи “точки входа” вызовите эту функцию

  ```python
from for_import import say_hello
if __name__== "__main__":
    say_hello()

def say_hello():
    print('Hello studends')
```
  ### Результат
  ![7](https://github.com/Mikhail867/Software_Engineering/assets/144737787/e51c78e5-4266-4c3b-bf89-b40d6c849bcb)

 
## Краткий вывод:
from for_import import say_hello - Импортируется функция say_hello из модуля (или файла) for_import.

if __name__== "__main__": - Это условие проверяет, запущен ли скрипт напрямую (а не импортирован как модуль в другом скрипте). Если скрипт запущен напрямую, выполняется следующий блок кода.

say_hello() - Вызывается функция say_hello(), которая была импортирована из модуля for_import. Таким образом, выводится приветственное сообщение или выполняется код, который находится внутри функции say_hello.


   ## Лабараторная работа 8
апишите программу, которая будет выводить корень, синус, косинус полученного от пользователя числа.

  ```python
import math
def main():
    value = int(input('Введите значение'))
    print(math.sqrt(value))
    print(math.sin(value))
    print(math.cos(value))
if __name__=='__main__':
    main()

```
  ### Результат
  ![8](https://github.com/Mikhail867/Software_Engineering/assets/144737787/45557ffd-6ea9-4c72-a80e-3e129853dcd8)

 
## Краткий вывод:

import math - Импортируется модуль math, который предоставляет математические функции.

def main(): - Определена функция main.

value = int(input('Введите значение')) - Программа запрашивает у пользователя ввод значения, преобразует его в целое число и сохраняет в переменной value.

print(math.sqrt(value)) - Выводится квадратный корень из введенного значения, используя функцию sqrt из модуля math.

print(math.sin(value)) - Выводится значение синуса угла в радианах, рассчитанное для введенного значения, используя функцию sin из модуля math.

print(math.cos(value)) - Выводится значение косинуса угла в радианах, рассчитанное для введенного значения, используя функцию cos из модуля math.

if __name__=='__main__': - Это условие проверяет, запущен ли скрипт напрямую.

main() - Если скрипт запущен напрямую, вызывается функция main(), и пользователь вводит значение. Затем программа выводит квадратный корень, синус и косинус этого значения.

   ## Лабараторная работа 9
Напишите программу, которая будет рассчитывать какой день недели будет через n-нное количество дней, которые укажет пользователь

  ```python
from  datetime import  datetime as dt
from  datetime import  timedelta as td
def main():
    print(
        f'Сегодня {dt.today().date()}'
        f'День недели {dt.today().isoweekday()}'
    )
    n = int(input("Введите количество дней"))
    today = dt.today()
    result = today + td(days=n)
    print(
        f'Через {n} дней будет {result.date()}'
        f'День недели - {result.isoweekday()}'
    )
if __name__== "__main__":
    main()

```
  ### Результат
  ![9](https://github.com/Mikhail867/Software_Engineering/assets/144737787/d814c6be-deb4-4a4f-81c7-c65b2f731006)

 
## Краткий вывод:
from datetime import datetime as dt и from datetime import timedelta as td - Импортируются класс datetime из модуля datetime и класс timedelta из того же модуля, а также дается им короткое псевдонимы dt и td соответственно.

def main(): - Определена функция main.

print(f'Сегодня {dt.today().date()} День недели {dt.today().isoweekday()}') - Выводится текущая дата и день недели, используя методы today().date() и today().isoweekday() из класса datetime.

n = int(input("Введите количество дней")) - Пользователь вводит количество дней (целое число).

today = dt.today() - Получается текущая дата и время.

result = today + td(days=n) - Создается новая дата, которая представляет собой текущую дату, увеличенную на введенное количество дней, используя класс timedelta.

print(f'Через {n} дней будет {result.date()} День недели - {result.isoweekday()}') - Выводится дата через указанное количество дней и соответствующий день недели, используя методы result.date() и result.isoweekday().

if __name__== "__main__": - Это условие проверяет, запущен ли скрипт напрямую.

main() - Если скрипт запущен напрямую, вызывается функция main(), и пользователю предлагается ввести количество дней. Затем программа выводит текущую дату, день недели, а также дату и день недели через указанное количество дней.


   ## Лабараторная работа 10

Напишите программу с использованием глобальных переменных, которая будет считать площадь треугольника или прямоугольника в зависимости от того, что выберет пользователь. Получение всей необходимой информации реализовать через input(), а подсчет площадей выполнить при помощи функций.
  ```python
global result
def rectangle():
    a=float(input("Ширина "))
    b = float(input("Высота "))
    global result
    result = a*b
def tritangle():
    a=float(input("снование "))
    h = float(input("Высота "))
    global result
    result = 0.5 * a * h
figure = input("1-прямоугольние, 2- треугольник ")
if figure == "1":
    rectangle()
elif figure == "2":
    tritangle()
print(f"Площадь {result}")
```
  ### Результат
  ![10](https://github.com/Mikhail867/Software_Engineering/assets/144737787/d3017b47-07be-4bd7-bbbf-f0862d4f843b)

 
## Краткий вывод:
global result - Это объявление глобальной переменной result, которая будет использоваться для хранения результата вычислений площади.

def rectangle(): - Определена функция rectangle, которая запрашивает у пользователя ширину и высоту прямоугольника, а затем вычисляет и сохраняет площадь в глобальной переменной result.

def triangle(): - Определена функция triangle, которая запрашивает у пользователя основание и высоту треугольника, а затем вычисляет и сохраняет площадь в глобальной переменной result.

figure = input("1-прямоугольник, 2-треугольник ") - Запрашивается у пользователя ввод для выбора фигуры.

if figure == "1": - Если пользователь выбрал прямоугольник, вызывается функция rectangle().

elif figure == "2": - Если пользователь выбрал треугольник, вызывается функция triangle().

print(f"Площадь {result}") - Выводится площадь рассчитанной фигуры, сохраненная в глобальной переменной result.

# Самостоятельные работы
   ## Самотоятельная работа 1
Дайте подробный комментарий для кода, написанного ниже. Комментарий нужен для каждой строчки кода, нужно описать что она делает. Не забудьте, что функции комментируются по-особенному

  ```python
from datetime import datetime: Импорт модуля datetime для измерения времени выполнения программы.
from math import sqrt: Импорт функции sqrt из модуля math для вычисления квадратного корня.
def main(**kwargs): Определение функции main с переменным числом именованных аргументов.
for key in kwargs.items(): Итерация по элементам словаря kwargs.
result = sqrt(key[1][0] ** 2 + key[1][1] ** 2): Вычисление длины вектора по формуле sqrt(x^2 + y^2).
print(result): Вывод результатов.
if __name__ == '__main__':: Проверка, запущен ли скрипт напрямую (а не импортирован в другой скрипт).
start_time = datetime.now(): Засекаем начальное время выполнения программы.
Вызов функции main с набором векторов в качестве аргументов.
time_costs = datetime.now() - start_time: Вычисление времени выполнения программы.
print(f"Время выполнения программы - {time_costs}"): Вывод времени выполнения.
```
  ### Результат
  ![11](https://github.com/Mikhail867/Software_Engineering/assets/144737787/7b4395ba-3dda-4a20-8f32-1aad786ebfd7)

 
## Краткий вывод:
Код эффективно использует возможности Python для работы с временем и математическими вычислениями.

  ## Самотоятельная работа 2
Напишите программу, которая будет заменять игральную кость с 6 гранями. Если значение равно 5 или 6, то в консоль выводится «Вы победили», если значения 3 или 4, то вы рекурсивно должны вызвать эту же функцию, если значение 1 или 2, то в консоль выводится «Вы проиграли». При этом каждый вызов функции необходимо выводить в консоль значение “кубика”. Для выполнения задания необходимо использовать стандартную библиотеку random. Программу нужно написать, используя одну функцию и “точку входа”

  ```python
from datetime import datetime
from math import sqrt
import random

def play_dice():
    # Бросаем кубик с 6 гранями
    dice_result = random.randint(1, 6)
    print(f"Вы бросили кубик: {dice_result}")

    # Определяем результат в зависимости от значения на кубике
    if dice_result in [5, 6]:
        print("Вы победили!")
    elif dice_result in [3, 4]:
        print("Продолжаем игру...")
        play_dice()  # Рекурсивный вызов функции
    else:
        print("Вы проиграли.")

if __name__ == "__main__":
    play_dice()
```
  ### Результат
  ![12](https://github.com/Mikhail867/Software_Engineering/assets/144737787/15ac2d77-13d2-48d2-8a60-f1d044abf994)

 
## Краткий вывод:
В этой программе play_dice рекурсивно вызывается в случае, если на кубике выпало значение 3 или 4. Игра продолжается до тех пор, пока не выпадут значения 5 или 6 (победа) или 1 или 2 (поражение). Каждый бросок кубика выводится в консоль.

  ## Самотоятельная работа 3
Напишите программу, которая будет выводить текущее время, с точностью до секунд на протяжении 5 секунд. Программу нужно написать с использованием цикла. Подсказка: необходимо использовать модуль datetime и time, а также вам необходимо как-то “усыплять” программу на 1 секунду.

  ```python
import datetime
import time

def display_current_time():
    for _ in range(5):
        current_time = datetime.datetime.now().strftime("%H:%M:%S")
        print(f"Текущее время: {current_time}")
        time.sleep(1)

if __name__ == "__main__":
    display_current_time()

```
  ### Результат
  ![13](https://github.com/Mikhail867/Software_Engineering/assets/144737787/a8a0b29c-1614-48c5-8819-7243353be23b)

 
## Краткий вывод:

В этой программе используются модули datetime для получения текущего времени и time для "усыпления" программы на 1 секунду с помощью time.sleep(1). Цикл for повторяется 5 раз, выводя текущее время с точностью до секунды.

  ## Самотоятельная работа 4
Напишите программу, которая считает среднее арифметическое от аргументов вызываемое функции, с условием того, что изначальное количество этих аргументов неизвестно. Программу необходимо реализовать используя одну функцию и “точку входа"

  ```python
def calculate_average(*args):
    if not args:
        print("Нет аргументов для вычисления среднего.")
        return

    total = sum(args)
    average = total / len(args)

    print(f"Среднее арифметическое: {average}")

if __name__ == "__main__":
    # Пример вызова функции с разным количеством аргументов
    calculate_average(1, 2, 3, 4, 5)
    calculate_average(10, 20, 30, 40, 50, 60)
    calculate_average(2, 4, 6, 8, 10)
    calculate_average()

```
  ### Результат
  ![14](https://github.com/Mikhail867/Software_Engineering/assets/144737787/ac266acd-7b9d-4253-8510-dd69c11242c5)

 
## Краткий вывод:
В этой программе используется *args, чтобы функция могла принимать переменное количество аргументов. Если не передано ни одного аргумента, программа сообщает об этом. В противном случае, она вычисляет и выводит среднее арифметическое переданных значений.

  ## Самотоятельная работа 5
Создайте два Python файла, в одном будет выполняться вычисление площади треугольника при помощи формулы Герона (необходимо реализовать через функцию), а во втором будет происходить взаимодействие с пользователем (получение всей необходимой информации и вывод результатов). Напишите эту программу и выведите в консоль полученную площадь.

  ```python
def calculate_triangle_area(a, b, c):
    # Формула полусуммы периметра и формулы Герона для вычисления площади треугольника
    s = (a + b + c) / 2
    area = (s * (s - a) * (s - b) * (s - c)) ** 0.5
    return area

if __name__ == "__main__":
    print("Программа вычисления площади треугольника.")
    a = float(input("Введите длину стороны a: "))
    b = float(input("Введите длину стороны b: "))
    c = float(input("Введите длину стороны c: "))

    triangle_area = calculate_triangle_area(a, b, c)

    print(f"Площадь треугольника: {triangle_area}")

from for_import import calculate_triangle_area


def get_user_input():
    a = float(input("Введите длину стороны a: "))
    b = float(input("Введите длину стороны b: "))
    c = float(input("Введите длину стороны c: "))
    return a, b, c


if __name__ == "__main__":
    print("Программа взаимодействия с пользователем для вычисления площади треугольника.")
    sides = get_user_input()

    # Распаковываем значения сторон и передаем их в функцию для вычисления площади
    triangle_area = calculate_triangle_area(*sides)

    print(f"Площадь треугольника: {triangle_area}")



```
  ### Результат
  ![15](https://github.com/Mikhail867/Software_Engineering/assets/144737787/7d5e760f-0b1f-4630-9933-167e725124e4)

 
## Краткий вывод:
Определена функция calculate_triangle_area(a, b, c), которая принимает длины сторон треугольника и вычисляет его площадь с использованием формулы Герона.

Внутри if __name__ == "__main__": программа запрашивает у пользователя длины сторон треугольника (a, b, c), вызывает функцию calculate_triangle_area для вычисления площади и выводит результат в консоль.

user_interaction.py:

Импортирована функция calculate_triangle_area из файла triangle_area_calculator.

Определена функция get_user_input(), которая запрашивает у пользователя длины сторон треугольника и возвращает их в виде кортежа.

Внутри if __name__ == "__main__": программа вызывает get_user_input для получения длин сторон треугольника, передает их в функцию calculate_triangle_area и выводит результат (площадь треугольника) в консоль.

Таким образом, вторая программа взаимодействует с пользователем, получает необходимые данные и использует функцию из первого файла для вычисления и вывода площади треугольника.
 # Общий вывод
 Функции:

Функции в Python облегчают организацию кода, разбивая его на более мелкие и логические блоки.


Модуль  выступает в роли набора функций, предназначенных для выполнения конкретной задачи .
Взаимодействие с пользователем:

Функция get_user_input в user_interaction.py демонстрирует взаимодействие с пользователем, запрашивая ввод данных.

Организация кода:

Разделение программы на модули улучшает структуру и управляемость кода.
Применение if __name__ == "__main__": позволяет определить точку входа в программу и выполнять дополнительные действия при запуске файла напрямую.
Реализация функциональности:

Программы демонстрируют примеры использования функций для выполнения конкретных задач (вычисление площади треугольника).
Разделение функциональности на модули делает код более поддерживаемым и легким для внесения изменений.
В целом, использование функций и модулей в этих программах способствует более чистой, структурированной и повторно используемой кодовой базе.
