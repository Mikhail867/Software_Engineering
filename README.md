# Тема 5. Базовые коллекции: множества, списки
Отчет по Теме #5 выполнил(а):
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
Друзья предложили вам поиграть в игру “найди отличия и убери повторения (версия для программистов)”. Суть игры состоит в том, что на вход программы поступает два множества, а ваша задача вывести все элементы первого, которых нет во втором. А вы как раз недавно прошли множества и знаете их возможности, поэтому это не составит для вас труда.

  ```python
set_1={'White','Black','Red','Pink'}
set_2={'Red','Green','Blue','Red'}
print(set_1 - set_2 )
```
  ### Результат
  ![1](https://github.com/Mikhail867/Software_Engineering/assets/144737787/a9b16ee8-7edf-40b5-b984-eb623c70cc3d)

 
## Краткий вывод:
Исходные множества:

set_1: {'White', 'Black', 'Red', 'Pink'}
set_2: {'Red', 'Green', 'Blue', 'Red'}
Результат операции set_1 - set_2:

В set_1 есть 'White', 'Black', 'Pink'
'Red' есть в обоих множествах, поэтому он не включается в результат.
Таким образом, на экран будет выведено множество {'White', 'Black', 'Pink'}.


   ## Лабараторная работа 2
Напишите две одинаковые программы, только одна будет использовать set(), а вторая frozenset() и попробуйте к исходному множеству добавить несколько элементов, например, через цикл. 

  ```python
a = set('abcdefg')
print(a)
for i in range(1, 5):
    a.add(1)
print(a)

```
  ### Результат
  ![2](https://github.com/Mikhail867/Software_Engineering/assets/144737787/f9eadd41-d54c-4151-9474-b0c369d68c98)

 
## Краткий вывод:
В этом коде создается множество a, содержащее элементы 'a', 'b', 'c', 'd', 'e', 'f', 'g'. Затем в цикле добавляется элемент '1' в это множество несколько раз.


   ## Лабараторная работа 3
На вход в программу поступает список (минимальной длиной 2 символа). Напишите программу, которая будет менять первый и последний элемент списка

  ```python
def replace(input_list):
    memory = input_list[0]
    input_list[0]=input_list[-1]
    
    return input_list 

print(replace([1,2,3,4,5]))
```
  ### Результат
  ![3](https://github.com/Mikhail867/Software_Engineering/assets/144737787/19e83a8a-29b2-4e22-b2d2-45aa3d83c957)

 
## Краткий вывод:
Этот код определяет функцию replace, которая принимает на вход список (input_list). Внутри функции первый элемент списка (input_list[0]) сохраняется в переменной memory. Затем первый элемент списка заменяется последним (input_list[0] = input_list[-1]). Функция возвращает измененный список.


   ## Лабараторная работа 4
На вход в программу поступает список (минимальной длиной 10 символов). Напишите программу, которая выводит элементы с индексами от 2 до 6. В программе необходимо использовать “срез”

  ```python
a =[12,54,32,843,2346,765,75,25,234,756,23]
print(a[2:6])

```
  ### Результат
  ![5](https://github.com/Mikhail867/Software_Engineering/assets/144737787/5e513068-733d-4404-b85d-3ae2632fcd2f)

 
## Краткий вывод:
В данном коде создается список a, и затем выводится подсписок этого списка, начиная с элемента с индексом 2 и заканчивая элементом с индексом 5 (не включая элемент с индексом 6).


   ## Лабараторная работа 5
Иван задумался о поиске «бесполезного» числа, полученного из списка. Суть поиска в следующем: он берет произвольный список чисел, находит самое большое из них, а затем делит его на длину списка. Студент пока не придумал, где может пригодиться подобное значение, но ищет у вас помощи в реализации такой функции useless()

  ```python
ef useless(lst):
    return max(lst) / len(lst)
print(useless([3,5,7,3,33]))
print(useless([-12.5,54,77.3,0,-36,98.2,-63,21.7,47,-89.6]))
print(useless([-25.8,86,12.5,-56,73.2,0,43,-91.5,65.9,-7]))
```
  ### Результат
  ![5](https://github.com/Mikhail867/Software_Engineering/assets/144737787/7c3ae0ba-2853-46c6-a905-1979b458e0ff)

 
## Краткий вывод:

Этот код определяет функцию useless, которая принимает на вход список (lst). Функция возвращает результат деления максимального значения в списке на его длину.

   ## Лабараторная работа 6
 Ребята не могут определится каким супергероем они хотят стать. У них есть случайно составленный список супергероев, и вы должны определить кто из ребят будет каким супергероем. Необходимо использовать разделение списков

  ```python
superheroes =['superman','spiderman','batman']
nikolay,vasiliy,ivan = superheroes

print('Николай -', nikolay)
print('Василий -', vasiliy)
print('Иван -', ivan)
```
  ### Результат
  ![6](https://github.com/Mikhail867/Software_Engineering/assets/144737787/bfc85472-ae36-4b18-b35a-da65cfa6bfc9)

 
## Краткий вывод:
В данном коде создается список superheroes с тремя строковыми элементами. Затем эти элементы распаковываются в три переменные: nikolay, vasiliy, и ivan. И, наконец, значения этих переменных выводятся на экран.

   ## Лабараторная работа 7
Вовочка, насмотревшись передачи “Слабое звено” решил написать программу, которая также будет находить самое слабое звено (минимальный элемент) и удалять его, только делать он это хочет не с людьми, а со списком. Помогите Вовочке с реализацией программы. Подсказка: для этого вам необходимо отсортировать список и удалить значение при помощи pop()

  ```python
a =[-25.8,86,12.5,-56,73.2,0,43,-91.5,65.9,-7]
a.sort()
print("Отсортированный список:\n",a)
a.pop(0)
print("Отсортированный список без наименьшого элемента:
```
 
# Результат
  ![7](https://github.com/Mikhail867/Software_Engineering/assets/144737787/0957027a-fd1a-42b5-b326-983d8f84ea4d)

 
## Краткий вывод:
a = [-25.8, 86, 12.5, -56, 73.2, 0, 43, -91.5, 65.9, -7]: Создается список a с десятью числовыми элементами.

a.sort(): Список a сортируется в порядке возрастания. После этой операции a будет [ -91.5, -56, -25.8, -7, 0, 12.5, 43, 65.9, 73.2, 86].

print("Отсортированный список:\n", a): Выводится отсортированный список.

a.pop(0): Удаляется первый элемент списка. Теперь a будет [ -56, -25.8, -7, 0, 12.5, 43, 65.9, 73.2, 86].

print("Отсортированный список без наименьшего элемента: \n", a): Выводится отсортированный список без удаленного элемента.


   ## Лабараторная работа 8
Михаил решил создать большой n-мерный список, для этого он случайным образом создал несколько списков, состоящих минимум из 3, а максимум из 10 элементов и поместил их в один большой список. Он также как и Иван не знает зачем ему это сейчас нужно, но надеется на то, что это пригодится ему в будущем.

  ```python
from random import  randint

def list_maker():
    a =[randint(1,100)]*randint(3,10)
    return a
if __name__ =='__main__':
    result = []
    for i in range(randint(1,5)):
        result.append(list_maker())

    print(result)

```
  ### Результат
  ![8](https://github.com/Mikhail867/Software_Engineering/assets/144737787/382136c1-1cb0-497b-88f6-14f967bef361)

 
## Краткий вывод:
В этом коде определена функция list_maker(), которая создает список случайной длины от 3 до 10 элементов, где каждый элемент - случайное число от 1 до 100. Затем в основной части программы создается список result, в который добавляются результаты вызова функции list_maker() несколько раз (от 1 до 5 раз).


   ## Лабараторная работа 9
Вы работаете в ресторане и отвечает за статистику покупок, ваша задача сравнить между собой заказы покупателей, которые указаны в разном порядке. Реализуйте функцию superset(), которая принимает 2 множества. Результат работы функции: вывод в консоль одного из сообщений в зависимости от ситуации: 1 - «Супермножество не обнаружено»
2 – «Объект {X} является чистым супермножеством» 
3 – «Множества равны

  ```python
def superset(set_1,set_2):
    if set_1 > set_2:
        print(f'Объект {set_1} вляется чистым супермножством')
    elif set_1==set_2:
        print(f"Множества равны")
    elif set_1<set_2:
        print(f'Объект {set_2} является чистым супермножеством')
    else:
        print("Супермножество не обнаружено")

if __name__ == '__main__':
    superset({1,8,3,5},{3,5})
    superset({1, 8, 3, 5}, {5, 3,8,1})
    superset({3,5}, {5,3,8,1})
    superset({90,100}, {3, 5})
```
  ### Результат
  ![9](https://github.com/Mikhail867/Software_Engineering/assets/144737787/19db60d1-3549-4259-b5f7-08a89af01b94)

 
## Краткий вывод:
def superset(set_1, set_2):: Определяется функция superset, которая сравнивает два множества и выводит информацию о том, является ли одно из них супермножеством другого.

if set_1 > set_2:: Если set_1 является супермножеством set_2 (все элементы set_2 также присутствуют в set_1), то выводится сообщение о том, что set_1 является чистым супермножеством.

elif set_1 == set_2:: Если множества равны, выводится сообщение об этом.

elif set_1 < set_2:: Если set_2 является супермножеством set_1, выводится сообщение о том, что set_2 является чистым супермножеством.

else:: Если ни одно из вышеперечисленного не выполняется, выводится сообщение о том, что супермножество не обнаружено.

if __name__ == '__main__':: Проверяется, запущен ли скрипт напрямую (а не импортирован как модуль).

Вызывается функция superset несколько раз с разными множествами.


   ## Лабараторная работа 10
Предположим, что вам нужно разобрать стопку бумаг, но нужно начать работу с нижней, “переверните стопку”. Вам дан произвольный список. Представьте его в обратном порядке. Программа должна занимать не более двух строк в редакторе кода.

  ```python
my_list=[2,5,8,3]
print(my_list[::-1])
```
  ### Результат
  ![10](https://github.com/Mikhail867/Software_Engineering/assets/144737787/d03336a2-39b5-4c39-97b4-3da92c3ca0ae)

 
## Краткий вывод:
my_list = [2, 5, 8, 3]: Создается список my_list с элементами 2, 5, 8, 3.

my_list[::-1]: Используется срез для создания нового списка, который является обратным порядком элементов из списка my_list. [::-1] означает "взять все элементы с шагом -1", что приводит к обратному порядку.

print(my_list[::-1]): Выводится новый список, который является обратным порядком исходного списка.

# Самостоятельные работы
   ## Самотоятельная работа 1


  ```python

```
  ### Результат
  
 
## Краткий вывод:

  ## Самотоятельная работа 2


  ```python

```
  ### Результат
  
 
## Краткий вывод:

  ## Самотоятельная работа 3


  ```python

```
  ### Результат
  
 
## Краткий вывод:

  ## Самотоятельная работа 4


  ```python

```
  ### Результат
  
 
## Краткий вывод:

  ## Самотоятельная работа 5


  ```python

```
  ### Результат
  
 
## Краткий вывод:
