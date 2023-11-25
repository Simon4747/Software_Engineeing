# Тема 8. Введение в ООП
Отчет по Теме #8 выполнил:
- Боркичев Данила Артемович
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |


# Лабараторные работы 
   ## Лабараторная работа 1


  ```python
class Car:
    def __init__(self,make,model):
        self.make = make
        self.model = model

my_car = Car("Toyota","Corolla")
```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/94b861cc-46a9-4c22-81e6-d3ee0602107a)



## Краткий вывод:
тот код создает класс Car с конструктором __init__, который принимает два аргумента: make (марка) и model (модель). Внутри конструктора эти значения присваиваются атрибутам self.make и self.model объекта класса.

Затем создается экземпляр класса my_car с аргументами "Toyota" и "Corolla". Таким образом, my_car становится объектом типа Car с маркой "Toyota" и моделью "Corolla".


   ## Лабараторная работа 2


  ```python
class Car:
    def __init__(self,make,model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car("Toyota","Corolla")
my_car.drive()
```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/57e547eb-ceaa-43b0-9aeb-0c75caf17e93)


 
## Краткий вывод:
Этот код также создает класс Car с конструктором __init__, который принимает два аргумента: make (марка) и model (модель). Внутри конструктора эти значения присваиваются атрибутам self.make и self.model объекта класса.

Однако в этом случае класс также имеет метод drive. Метод drive выводит сообщение о том, что происходит при вождении данного автомобиля, используя значения марки и модели, сохраненные в атрибутах.

Затем создается экземпляр класса my_car с аргументами "Toyota" и "Corolla". После этого вызывается метод drive() для объекта my_car, что приводит к выводу сообщения "Driving the Toyota Corolla".


   ## Лабараторная работа 3


  ```python
class Car:
    def __init__(self,make,model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car("Toyota","Corolla")
my_car.drive()

class ElectricCar(Car):
    def __init__(self, make,model,battery_capacity):
        super().__init__(make,model)
        self.battery_capacity = battery_capacity

    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

my_electric_car = ElectricCar("Tesla", "Model s",75)
my_electric_car.drive()
my_electric_car.charge()

```
  ### Результат
  ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/e897a575-f7a7-4ee2-8acb-f92d765b0772)


 
## Краткий вывод:
В этом коде определен класс Car с методами __init__ и drive. Затем создается объект my_car класса Car с маркой "Toyota" и моделью "Corolla", и вызывается метод drive, что приводит к выводу "Driving the Toyota Corolla".

Затем определен подкласс ElectricCar, который наследует от класса Car. В конструкторе __init__ этого подкласса вызывается конструктор родительского класса с помощью super().__init__(make, model), чтобы унаследовать атрибуты make и model. Затем у подкласса ElectricCar добавляется новый атрибут battery_capacity.

Создается объект my_electric_car класса ElectricCar с маркой "Tesla", моделью "Model S" и емкостью батареи 75. Затем вызываются методы drive() и charge()


   ## Лабараторная работа 4


  ```python
class Car:
    def __init__(self,make,model):
        self._make = make
        self.__model = model

    def drive(self):
        print(f"Driving the {self._make} {self.__model}")

my_car = Car("Toyota","Corolla")
print(my_car._make)
my_car.drive()

```
  ### Результат
![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/ae8cb5c7-180f-488d-bf15-495a642acf6e)


 
## Краткий вывод:
Этот код определяет класс Car с атрибутами _make и __model. Использование одного подчеркивания перед именем атрибута (_make) обычно сигнализирует о том, что атрибут является "protected" (защищенным), что подразумевает, что его лучше не использовать вне класса, но это не является строгим правилом.

Использование двух подчеркиваний перед именем атрибута (__model) делает его "private" (приватным), что означает, что он не должен напрямую использоваться за пределами класса. Однако, в Python его все равно можно получить, но с другим именем (например, _Car__model). Но так делать не рекомендуется из-за нарушения инкапсуляции.

Затем создается объект my_car класса Car с маркой "Toyota" и моделью "Corolla". Выводится значение атрибута _make, и вызывается метод drive(), демонстрируя использование атрибутов и методов класса.


   ## Лабараторная работа 5


  ```python
class Shape:
    def area(self):
        pass


class Rectangle(Shape):
    def __init__(self,width,height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height


class Circle(Shape):
    def __init__(self,radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius


d = Rectangle(11,5)
print("Прямоугольник ",d.area())

a = Circle(11)
print("Круг ",a.area())
```
  ### Результат
  ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/4b701f4c-0fe1-44d6-a373-ef927f27688f)


 
## Краткий вывод:
Этот код создает иерархию классов для расчета площадей различных форм (прямоугольника и круга). Каждый подкласс (Rectangle и Circle) наследует метод area от базового класса Shape и переопределяет его, чтобы предоставить конкретную реализацию для каждой формы. Затем создаются объекты каждого подкласса, и их методы area вызываются для расчета и вывода площадей.


   


# Самостоятельные работы
   ## Самотоятельная работа 1


  ```python
class Danil:
    def __init__(self,rost,ves):
        self.rost = rost
        self.ves = ves
    #def harakteristik(self):
        #print(f"Рост {self.rost} Вес {self.ves}"

Q = Danil(184,70)
#Q.harakteristik()

```
  ### Результат
  ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/f010972b-a6b9-4cb6-8f67-f89aff59ad3c)



  ## Самотоятельная работа 2


  ```python
class Danil:
    def __init__(self,rost,ves):
        self.rost = rost
        self.ves = ves
    def harakteristik(self):
        print(f"Рост {self.rost} Вес {self.ves}")

Q = Danil(184,70)
Q.harakteristik()

```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/c005b7ce-8d48-4dee-a9fd-3f0eb06df03e)


 

  ## Самотоятельная работа 3


  ```python
class Danil:
    def __init__(self,rost,ves):
        self.rost = rost
        self.ves = ves
    def harakteristik(self):
        print(f"Рост {self.rost} Вес {self.ves}")

Q = Danil(184,70)
Q.harakteristik()


class ASD(Danil):
    def __init__(self,rost,ves,vozrast):
        super().__init__(rost, ves)
        self.vozrast = vozrast
    def dosie(self):
        print(f"Теперь рост и вес {self.rost} {self.ves} в {self.vozrast} лет")

Novi_rost = ASD(200,90,21)
Novi_rost.harakteristik()
Novi_rost.dosie()
```
  ### Результат
![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/8b87ae3e-3e93-40b9-8511-91afd1314e96)


 

  ## Самотоятельная работа 4


  ```python
class Danil:
    def __init__(self,rost,ves):
        self._rost = rost
        self.__ves = ves
    def harakteristik(self):
        print(f"Рост {self._rost} Вес {self.__ves}")

Q = Danil(184,70)
Q.harakteristik()


class ASD(Danil):
    def __init__(self,_rost,__ves,vozrast):
        super().__init__(_rost, __ves)
        self.vozrast = vozrast
    def dosie(self):
        print(f"Теперь рост и вес {self._rost} {self.__ves} в {self.vozrast} лет")

Novi_rost = ASD(200,90,21)
Novi_rost.harakteristik()
Novi_rost.dosie()
```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/94af3299-2f68-402d-919b-7c7c1198959a)


 


  ## Самотоятельная работа 5


  ```python
class One:
    def __init__(self,ves,rost):
        self.ves = ves
        self.rost = rost

    def area(self):
        return self.rost / self.ves

class Two:
    def __init__(self,vozrast,kotleti):
        self.vozrast = vozrast
        self.kotleti = kotleti

    def area(self):
        return self.kotleti + self.vozrast


Otnoshenie = One(70,185)
print(f"Отношение Роста к Весу {Otnoshenie.area()}")
SkolkoLetStolkoKotlet = Two(20,0)
print(f"Нужно Котлет {SkolkoLetStolkoKotlet.area()}")
```
  ### Результат
![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/dd2d3348-aa07-4060-8f00-c21055681712)

  
  # Общий вывод:
  Введение в объектно-ориентированное программирование (ООП) представляет собой ключевой аспект в разработке программного обеспечения, который позволяет структурировать код вокруг объектов, представляющих реальные сущности, а также использовать концепции наследования, инкапсуляции и полиморфизма для создания более гибкого и понятного кода.

ООП базируется на следующих принципах:

Инкапсуляция: Скрывает внутреннюю реализацию объектов и предоставляет интерфейс для их взаимодействия. Атрибуты и методы объединяются в классы, что облегчает поддержку кода и сокрытие деталей реализации.

Наследование: Позволяет создавать новые классы на основе существующих, наследуя их атрибуты и методы. Это снижает дублирование кода и улучшает структуру программы.

Полиморфизм: Объекты разных классов могут обладать одинаковым интерфейсом, что позволяет использовать их взаимозаменяемо. Полиморфизм упрощает кодирование и повышает его гибкость.

ООП применяется для более эффективной организации кода, улучшения его читаемости, уменьшения сложности программ и обеспечения повторного использования кода. Он позволяет моделировать реальные объекты и их взаимодействие, что делает разработку программ более интуитивной и эффективной.

  
 
