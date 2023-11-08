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


  ```python
class Car:
    def __init__(self,make,model):
        self.make=make
        self.model=model

my_car = Car("Toyota","Corolla")
```
  ### Результат
  ![1](https://github.com/Mikhail867/Software_Engineering/assets/144737787/1b5009e5-2df2-44e1-a16c-68b68d18fcc0)

 
## Краткий вывод:
тот код создает класс Car с конструктором __init__, который принимает два аргумента: make (марка) и model (модель). Внутри конструктора эти значения присваиваются атрибутам self.make и self.model объекта класса.

Затем создается экземпляр класса my_car с аргументами "Toyota" и "Corolla". Таким образом, my_car становится объектом типа Car с маркой "Toyota" и моделью "Corolla".


   ## Лабараторная работа 2


  ```python
class Car:
    def __init__(self,make,model):
        self.make=make
        self.model=model
    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car("Toyota","Corolla")
my_car.drive()
```
  ### Результат
  ![2](https://github.com/Mikhail867/Software_Engineering/assets/144737787/2198a38b-bf9c-460d-b0b2-86622d12515b)

 
## Краткий вывод:
Этот код также создает класс Car с конструктором __init__, который принимает два аргумента: make (марка) и model (модель). Внутри конструктора эти значения присваиваются атрибутам self.make и self.model объекта класса.

Однако в этом случае класс также имеет метод drive. Метод drive выводит сообщение о том, что происходит при вождении данного автомобиля, используя значения марки и модели, сохраненные в атрибутах.

Затем создается экземпляр класса my_car с аргументами "Toyota" и "Corolla". После этого вызывается метод drive() для объекта my_car, что приводит к выводу сообщения "Driving the Toyota Corolla".


   ## Лабараторная работа 3


  ```python
# Определение класса Car
class Car:
    def __init__(self, make, model):
        # Инициализация атрибутов make и model
        self.make = make
        self.model = model

    def drive(self):
        # Вывод сообщения о вождении с использованием марки и модели
        print(f"Driving the {self.make} {self.model}")

# Создание объекта my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")
# Вызов метода drive для объекта my_car
my_car.drive()

# Определение подкласса ElectricCar, наследующего от класса Car
class ElectricCar(Car):
    def __init__(self, make, model, battery_capacity):
        # Вызов конструктора родительского класса с помощью super()
        super().__init__(make, model)
        # Инициализация атрибута battery_capacity для подкласса ElectricCar
        self.battery_capacity = battery_capacity

    def charge(self):
        # Вывод сообщения о зарядке с использованием марки, модели и емкости батареи
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

# Создание объекта my_electric_car класса ElectricCar с маркой "Tesla", моделью "Model S" и емкостью батареи 75
my_electric_car = ElectricCar("Tesla", "Model S", 75)
# Вызов метода drive для объекта my_electric_car
my_electric_car.drive()
# Вызов метода charge для объекта my_electric_car
my_electric_car.charge()

```
  ### Результат
  ![3](https://github.com/Mikhail867/Software_Engineering/assets/144737787/f3476747-1c4c-4119-98ea-0c4adf0194bf)

 
## Краткий вывод:
В этом коде определен класс Car с методами __init__ и drive. Затем создается объект my_car класса Car с маркой "Toyota" и моделью "Corolla", и вызывается метод drive, что приводит к выводу "Driving the Toyota Corolla".

Затем определен подкласс ElectricCar, который наследует от класса Car. В конструкторе __init__ этого подкласса вызывается конструктор родительского класса с помощью super().__init__(make, model), чтобы унаследовать атрибуты make и model. Затем у подкласса ElectricCar добавляется новый атрибут battery_capacity.

Создается объект my_electric_car класса ElectricCar с маркой "Tesla", моделью "Model S" и емкостью батареи 75. Затем вызываются методы drive() и charge()


   ## Лабараторная работа 4


  ```python
# Определение класса Car
class Car:
    def __init__(self, make, model):
        # Инициализация атрибута _make с использованием единого подчеркивания (неявно указывает на "protected")
        self._make = make
        # Инициализация атрибута __model с использованием двух подчеркиваний (имеет защищенный доступ)
        self.__model = model

    def drive(self):
        # Вывод сообщения о вождении с использованием марки и модели
        print(f"Driving the {self._make} {self.__model}")

# Создание объекта my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")

# Вывод значения атрибута _make (в общем случае, неявно считается защищенным)
print(my_car._make)

# Вызов метода drive для объекта my_car
my_car.drive()

```
  ### Результат
  ![4](https://github.com/Mikhail867/Software_Engineering/assets/144737787/2b7309c2-6993-419d-879c-7a4eeb6bcf62)

 
## Краткий вывод:
Этот код определяет класс Car с атрибутами _make и __model. Использование одного подчеркивания перед именем атрибута (_make) обычно сигнализирует о том, что атрибут является "protected" (защищенным), что подразумевает, что его лучше не использовать вне класса, но это не является строгим правилом.

Использование двух подчеркиваний перед именем атрибута (__model) делает его "private" (приватным), что означает, что он не должен напрямую использоваться за пределами класса. Однако, в Python его все равно можно получить, но с другим именем (например, _Car__model). Но так делать не рекомендуется из-за нарушения инкапсуляции.

Затем создается объект my_car класса Car с маркой "Toyota" и моделью "Corolla". Выводится значение атрибута _make, и вызывается метод drive(), демонстрируя использование атрибутов и методов класса.


   ## Лабараторная работа 5


  ```python
# Определение базового класса Shape
class Shape:
    def area(self):
        # Этот метод не имеет конкретной реализации, поскольку содержит оператор pass
        pass

# Определение подкласса Rectangle, наследующего от класса Shape
class Rectangle(Shape):
    def __init__(self, width, height):
        # Инициализация атрибутов width и height
        self.width = width
        self.height = height

    def area(self):
        # Переопределение метода area для расчета площади прямоугольника
        return self.width * self.height

# Определение подкласса Circle, также наследующего от класса Shape
class Circle(Shape):
    def __init__(self, radius):
        # Инициализация атрибута radius
        self.radius = radius

    def area(self):
        # Переопределение метода area для расчета площади круга
        return 3.14 * self.radius * self.radius

# Создание объекта Rectangle
rectangle = Rectangle(5, 10)
# Вычисление и вывод площади прямоугольника
print("Rectangle Area:", rectangle.area())

# Создание объекта Circle
circle = Circle(7)
# Вычисление и вывод площади круга
print("Circle Area:", circle.area())

```
  ### Результат
  ![5](https://github.com/Mikhail867/Software_Engineering/assets/144737787/476b35f1-8768-42ca-87f2-401231cb572f)

 
## Краткий вывод:
Этот код создает иерархию классов для расчета площадей различных форм (прямоугольника и круга). Каждый подкласс (Rectangle и Circle) наследует метод area от базового класса Shape и переопределяет его, чтобы предоставить конкретную реализацию для каждой формы. Затем создаются объекты каждого подкласса, и их методы area вызываются для расчета и вывода площадей.


   


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
  
 
