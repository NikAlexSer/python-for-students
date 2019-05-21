# Python
#### Установка
Инструкция по установки для Windows - ставить нужно 3 версию питона
* [Инструкция по установке](https://pythonworld.ru/osnovy/skachat-python.html)
* ВАЖНО! - в ходе установки будет место для вставки галки с текстом примерного вида Add to PATH, необходимо, чтобы галка стояла

#### Запуск "блокнота" для написание кода
* В меню Пуск ввести IDLE, нажать на Idle (Python 3)
* File >>> New File
* В этом файле можно писать код, который потом можно запускать: 
  * нажатием клавиши F5 
  * через меню Run >>> Run Module

Альтернативой для написания кода могут являться специлизированные программы
* [Pycharm Community](https://www.jetbrains.com/pycharm/download/#section=windows)
* Любой удобный для вас редактор (Sublime, VS Code, Блокнот (лол)), запуск скрипта будет производиться через папку с файлом двойным кликом

#### Первая программа
* Создайте новый файл с расширением .py (через IDLE оно само так создается)
* Введите ```print('Hello world!')```
* Сохраните и запустите (клавиша F5)
* В консоль питона (окно с именем Shell) должно вывестись "Hello world!"
* Если заработало - Поздравляю, вы великолепны!

#### Самоучитель
Для понимания човащепроисходит необходимо ознакомиться с пунктами 3-11

При непонимании човащепроисходит после прочтения - задавайте вопросы https://vk.com/nikalexser

[Самоучитель](https://pythonworld.ru/samouchitel-python)

### Домашняя работе №1
* Необходимо, чтобы программа считала сумму чисел вашей даты рождения и выводила при выполнении строку, например "Имя - дата - сумма"

### Домашняя работа №2
* Необходимо решить, используя Python, любые 5 задач, не идущих подряд - например, 1, 3, 5, 7, 9
* Список задач - http://euler.jakumo.org/problems.html

### Создаем свой блэкджэк с 👯‍♀️
[![N|Solid](https://memepedia.ru/wp-content/uploads/2017/08/%D0%B1%D0%B5%D0%BD%D0%B4%D0%B5%D1%80-%D1%84%D1%83%D1%82%D1%83%D1%80%D0%B0%D0%BC%D0%B0.png)]()

Ну, точнее, не блэкджек, а его мини-вариант под названием очко.
Для реализации нам понадобится колода карт, из которой каждый раз мы будем вынимать по карте и прибавлять к результату.
Далее, сами "карты": шестерка, семерка, восьмерка, девятка, десятка, валет (достоинством 2), дама (3), король (4), и туз (11).

```
koloda = [6,7,8,9,10,2,3,4,11] * 4
```
Случайным образом перемешаем карты, используя функцию shuffle из модуля random.
```
import random
random.shuffle(koloda)
```

Ща будет жестко, если вы не ознакомились с пунктами 3-11 из самоучителя и не делали дз :)))

Собственно, начинаем играть:
```
print('Поиграем в очко?')
count = 0

while True:
    choice = input('Будете брать карту? y/n\n')
    if choice == 'y':
        current = koloda.pop()
        print('Вам попалась карта достоинством %d' %current)
        count += current
        if count > 21:
            print('Извините, но вы проиграли')
            break
        elif count == 21:
            print('Поздравляю, вы набрали 21!')
            break
        else:
            print('У вас %d очков.' %count)
    elif choice == 'n':
        print('У вас %d очков и вы закончили игру.' %count)
        break

print('До новых встреч!')
```

##### Пояснение човащепроисходит
Изначально у пользователя 0 очков. Мы его спрашиваем, будет ли он брать карту, на что он должен ответить y или n. Если пользователь ответил n, то мы говорим ему, сколько очков он набрал, и завершаем программу. Если он изъявил желание взять карту (ух, какой нехороший пользователь :)), то мы снимаем ему карту из списка (с помощью метода pop). Мы снимаем последнюю карту, хотя вообще без разницы, какую снимать, ведь они перемешаны.

Прибавляем к числу очков достоинство снятой карты, а дальше смотрим, сколько всего очков у пользователя. Если количество очков больше 21, то извиняйте, пользователь проиграл. Если число очков равно 21, то пользователь выиграл. Если меньше - еще раз спросим пользователя, будет ли он брать карту.

В конце игры прощаемся с пользователем.

### Домашняя работа №3
* Необходимо улучшить наш Блэкджек, чтобы программа тоже играла и в случае всех исходов говорила кто выиграл
* Пример: Я набрал 18 очков, программа 20, я зассал и программа выведет "Я выиграла, кожанный ублюдок 😛 бебебе"

### Время приключений 🍻
⛔⛔⛔Продолжение следует, но это не точно ⛔⛔⛔

При возникновении трудностей и непонимания можно обращаться ко мне в личку https://vk.com/nikalexser
