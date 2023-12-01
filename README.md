# Тема 9. Концепции и принципы ООП
Отчет по Теме #9 выполнил:
- Боркичев Данила Артемович
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + |  |
| Задание 3 | + |  |
| Задание 4 | + |  |
| Задание 5 | + |  |
| Задание 6 |  | |
| Задание 7 |  | |
| Задание 8 |  |  |
| Задание 9 |  |  |
| Задание 10 |  |  |

# Лабараторные работы 
   ## Лабараторная работа 1


  ```python
class Ivan:
    __slots__ = ['name']

    def __init__(self,name):
        if name == 'Иван':
            self.name = f"Да, я {name}"
        else:
            self.name = f"Я не {name}, a Иван"

person1 = Ivan('Алексей')
person2 = Ivan('Иван')
print(person1.name)
print(person2.name)

person2.surrname = 'Петров'

```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/759eaf25-cc26-4934-a568-8f5d4eb81c94)


 
## Краткий вывод:
Код определяет класс Ivan с использованием слотов (slots), что означает, что объекты этого класса могут иметь только атрибуты, указанные в __slots__. В данном случае разрешен только атрибут 'name'.

В конструкторе __init__ проверяется переданное имя. Если оно равно 'Иван', то атрибут 'name' инициализируется строкой "Да, я Иван", иначе - "Я не {name}, а Иван".

Затем создаются два объекта класса Ivan - person1 с именем "Алексей" и person2 с именем 'Иван'. Затем выводятся значения атрибута 'name' для обоих объектов.

Однако, последняя строка person2.surname = "Петров" вызовет ошибку, так как атрибут 'surname' не был объявлен в __slots__ и поэтому не может быть добавлен к объекту данного класса


   ## Лабараторная работа 2


  ```python
class Icecream:
    def __init__(self,ingredient=None):
        if isinstance(ingredient,str):
            self.ingredient = ingredient
        else:
            self.ingredient=None
    def composition(self):
        if self.ingredient:
            print(f"Мороженое с {self.ingredient}")
        else:
            print("Обычное мороженое")

icecream = Icecream()
icecream.composition()
icecream = Icecream('Шоколадом')
icecream.composition()
icecream= Icecream(5)
icecream.composition()
```
  ### Результат
  ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/85ebfd98-00b3-43a8-8a7a-06618f502519)


 
## Краткий вывод:

Этот код определяет класс Icecream, который имеет конструктор __init__ и метод composition

   ## Лабараторная работа 3


  ```python
class MyClass:
    def __init__(self,value):
        self._value = value
    def set_value(self,value):
        self._value = value
    def get_value(self):
        return self._value
    def del_value(self):
        del self._value
    value = property(get_value,set_value,del_value,"cвойство value")

obj = MyClass(42)
print(obj.del_value())
obj.set_value(45)
print(obj.del_value())
obj.set_value(100)
print(obj.del_value())
obj.set_value()
print(obj.del_value())
```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/52c2d281-3c89-4188-bdc3-8cbade94b8f9)


 
## Краткий вывод:

В предоставленном коде определен класс MyClass с использованием свойства (property). Давайте рассмотрим, что происходит в коде:

Создается объект obj класса MyClass с начальным значением 42.
Вызывается метод del_value() объекта obj. Этот метод удаляет атрибут _value, но поскольку это действие не возвращает значение, выводиться None. Однако, метод del_value() не должен возвращать значение, а вместо этого просто удалять атрибут.

   ## Лабараторная работа 4


  ```python
class Mammal:
    className ="Mammal"
class Dog(Mammal):
    species = 'canine'
    sounds = 'wow'
class Cat(Mammal):
    species = 'feline'
    sounds='meow'

dog = Dog()
print(f"Dog is {dog.className}, but they say{dog.sounds}")
cat= Cat()
print(f"Cat is {cat.className}, but they say {cat.sounds}")
```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/1bc5a472-e4bf-4b78-8d91-95792c5a12c9)


 
## Краткий вывод:
В данном коде определены два класса: Mammal, Dog и Cat, которые наследуются от Mammal
Определение класса Mammal:
У класса Mammal есть атрибут className, установленный в строку "Mammal".
Определение класса Dog:
Класс Dog наследует атрибут className от класса Mammal.
У класса Dog есть атрибут species, установленный в строку "canine", и атрибут sounds, установленный в строку "wow"
   ## Лабараторная работа 5


  ```python
class Russian:
    @staticmethod
    def greeting():
        print('Привет')

class English:
    @staticmethod
    def greeting():
        print('Hello')
def greet(language):
        language.greeting()

ivan = Russian()
greet(ivan)
john=English()
greet(john)
```
  ### Результат
  ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/eefbedc6-c538-403d-b1d8-98cdcf04e5fa)


 
## Краткий вывод:
Этот код определяет два класса, Russian и English, каждый из которых имеет статический метод greeting(). Затем определена функция greet(language), которая принимает объект языкового класса и вызывает его метод greeting().

Далее создаются объекты ivan и john для классов Russian и English соответственно. Затем вызывается функция greet(language) для каждого объекта.




# Самостоятельные работы
   ## Самотоятельная работа 1


  ```python
class Tomato:
    states = {'Отсутствует': 0, 'Цветение': 1, 'Зеленый': 2, 'Красный': 3}

    def __init__(self, index):
        self._index = index
        self._state = self.states['Отсутствует']

    def grow(self):
        if self._state < 3:
            self._state += 1

    def is_ripe(self):
        return True if self._state == 3 else False


class TomatoBush:

    def __init__(self, num):
        self.tomatoes = [Tomato(index) for index in range(1, num + 1)]

    def grow_all(self):
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):
        return all([tomato.is_ripe() for tomato in self.tomatoes])

    def give_away_all(self):
        self.tomatoes = []


class Gardener:

    def __init__(self, name, plant):
        self.name = name
        self._plant = plant

    def work(self):
        self._plant.grow_all()

    def harvest(self):
        if self._plant.all_are_ripe():
            print('Урожай собран!')
            self._plant.give_away_all()
        else:
            print('Томаты еще не дозрели')

    @staticmethod
    def knowledge_base():
        print('Справка по садоводству:')
        print('1. Не забывайте регулярно поливать и подкармливать растения')
        print('2. Определите правильное расстояние между растениями, чтобы они не мешали друг другу в росте')
        print('3. Удалите поврежденные листья и плоды, чтобы предотвратить распространение болезней')


# Вызов справки по садоводству
Gardener.knowledge_base()

# Создание объектов классов TomatoBush и Gardener
bush = TomatoBush(5)
gardener = Gardener('Михаил', bush)

# Уход за кустом с помидорами
gardener.work()
gardener.work()
gardener.work()

# Сбор урожая
gardener.harvest()

# Продолжение ухода за кустом, пока томаты не дозреют
gardener.work()
gardener.harvest()
gardener.work()
gardener.harvest()
gardener.work()
gardener.harvest()
# Сбор урожая после дозревания всех томатов
gardener.work()
gardener.harvest()

```
  ### Результат
 ![image](https://github.com/Simon4747/Software_Engineeing/assets/147588966/92d8a643-17f9-4a8e-b467-a71749e19d91)

 
## Краткий вывод:
Класс Tomato:

Имеет статический словарь states, представляющий состояния томата.
Конструктор __init__ инициализирует индекс и состояние томата (начально установлено в 'Отсутствует').
Метод grow увеличивает состояние томата на единицу (если оно меньше 3).
Метод is_ripe возвращает True, если состояние томата достигло 3, иначе False.
Класс TomatoBush:

Конструктор __init__ создает список томатов на основе переданного числа.
Метод grow_all вызывает метод grow для каждого томата в кусте.
Метод all_are_ripe возвращает True, если все томаты в кусте дозрели, иначе False.
Метод give_away_all очищает список томатов.
Класс Gardener:

Конструктор __init__ принимает имя садовода и объект TomatoBush.
Метод work вызывает метод grow_all у объекта TomatoBush.
Метод harvest проверяет, все ли томаты дозрели. Если да, то выводит сообщение и вызывает give_away_all, иначе выводит, что томаты еще не дозрели.
Статический метод knowledge_base выводит справку по садоводству.
Вызов справки и создание объектов:

Выводится справка по садоводству.
Создается объект TomatoBush с 5 томатами и объект Gardener с именем "Михаил" и этим кустом томатов.
Уход за кустом и сбор урожая:

Выполняется несколько циклов ухода за кустом (work) и попыток сбора урожая (harvest).
После определенного числа уходов томаты дозревают, и происходит успешный сбор урожая.
Продолжение ухода и сбор урожая:

Процесс ухода и попыток сбора урожая продолжается, но томаты уже все дозрели, поэтому каждый раз сбор урожая успешен.
 
 
# Общий вывод вывод:
Использование классов и объектов:

В каждой программе определены классы, представляющие сущности: Tomato, TomatoBush, и Gardener.
Создаются объекты этих классов, такие как томаты, кусты томатов и садовод.
Инкапсуляция:

В классе Tomato используется инкапсуляция, где состояние томата (_index и _state) скрыто от внешнего доступа, а доступ осуществляется через методы grow и is_ripe.
Наследование:

Классы TomatoBush и Gardener наследуют функциональность от классов Tomato и object соответственно.
Полиморфизм:

Методы grow_all и harvest взаимодействуют с различными объектами (томатами и кустом томатов) без необходимости знать их конкретный тип.
Статические методы и переменные класса:

Используются статические методы и переменные класса, такие как knowledge_base и states в классе Gardener и Tomato.
Принципы ООП в коде:

Создание объектов, использование классов для моделирования реальных сущностей.
Инкапсуляция данных и функциональности внутри классов.
Наследование для повторного использования кода и создания иерархии классов.
Полиморфизм для обработки объектов разных типов через общий интерфейс.
Общий вывод заключается в том, что код демонстрирует успешную реализацию принципов объектно-ориентированного программирования, что облегчает структурирование кода, повышает его читаемость и обеспечивает более гибкую и поддерживаемую архитектуру программы.
