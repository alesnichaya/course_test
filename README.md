# Курс тест по Java

Цель курса
----------

Проверить логические и алгоритмические способности ученика заниматься профессиональным программированием. 
Кандидаты полностью выполнившие все задания могут смело продолжать изучать программирование, 
т.к. у них есть хороший потенциал стать высококвалифицированными разработчиками ПО.
Кандидатам, которые испытывают сложности в выполнении данных задач, следует обратить внимание 
на смежные области разработки ПО, такие как: QA Automation, аналитик, функциональный программист, support.

Описание
--------

В курсе собраны 20 задач возрастающей сложности. Каждая задача состоит из подготовленного каркаса классов и 
полность написанных автоматических тестов. То есть все задания будут автоматически проверены. 
В данном курсе используется подход TDD. Инструменты необходимые для прохождения курса: Maven, Git, Java 8.

Для получения исходного кода нужно выполнит команду 

*git clone git@github.com:peterarsentev/course_test.git*

Проект собрать через maven. Задания курса находится в каждом пакетах 

*/src/main/java/ru/parsentev/task_XXX/package-info.java*

а так же продублированы ниже.

Ученик должен ознакомиться c заданием и перейти к реализации недостающего кода и классов. 
После завершения реализации ученик должен зайти в папку 

*/src/test/java/ru/parsentev/task_XXX/*

и в каждом классе убрать аннотацию 

*@Ignore* - это аннотация используется для игнорирования тестов.

после этого ученик должен перейти в корень проекта и выполнить команду

*mvn clean test*

Система сборки должна успешно пройти все тесты. Если тесты упали, необходимо поправить ваш код.
Код тестов править нельзя. 

В репозитории есть две ветки

- master - каркас заданий с тестами.
- solution - полностью выполненые задания с тестами.

Смотреть решения рекомендуется после успешной реализации кода и успешно пройденных тестов.

В качестве теоретического материала для подготовки к курсe следует прочитать книгу.

*Head First Java, 2nd Edition: Kathy Sierra, Bert Bates*

Темы необходимые для прохождения курса.

- Типы данных
- Арифметические операции
- Операторы условия
- Циклы
- Массивы
- Наследование
- Полиморфизм
- Инкапсуляция
- Исключения

Задания
-------

1. Реализовать программу калькулятор. Калькулятор должен выполнять операции:
   сложения, вычистания, умножение, деление, возведение в степень.
   При операции деление ввести проверку на деление на 0.
   Если второй аргумент 0 нужно выкинуть исключение java.lang.IllegalStateException
   
2. Реализовать класс точку, описывающий точку в системе коордионат x, y - Point(x, y).
   объект точка должна иметь методы double Point#distanceTo(Point point) - метод должен вычислять расстояния
   между двумя точками.

3. Реализовать класс треугольник. Треугольник должен описываться через точки в системе коордионат.
   Объект треугольник должен иметь методы:
   boolean isExits() - проверяет существует ли треугольник или нет.
   double area() - вычисляет площать треугольника. 
   Если треугольник не существует выбросить исключение java.lang.IllegalStateException
   
4. Реализовать класс равносторонний треугольник наследуя класс треугольник из задания 3.
   Дополнить поведение метода boolean isExists() - true, если треугольник равносторонний. 
   Остальное поведение оставить.

5. Реализовать класс прямоугольный треугольник наследуя класс треугольник из задания 3.
   Дополнить поведение метода boolean isExists() - true, если треугольник равносторонний. 
   Остальное поведение оставить.

6. Реализовать класс квадрат основанный на четырех точках Point(x, y).
   boolean isExits() - проверяет существует ли квадрат или нет.

7. Реализовать класс СalcExpression. Класс должен принимать строку из просто математического выражения 
   и методы double calc(). Должен поддерживать операции + - / * exp.
   Например, "2+2" - 4, "2-2" - 0 

8. Реализовать класс вычислящий простые числа до N.

9. Реализовать метод подсчета уникальных символов в строке.

10. Реализовать методы проверки корректности открытых и закрытых скобок.
    Например, ()(()((()))) - true, ()) - false
 
11. Задан массив чисел со значениями 0 и 1. Нужно проверить, что все значения в массиве равны 1.
    Например.

12. Задан массив чисел со значениями 0 и 1. 
    Нужно проверить, что в массиве есть последовательности из трех и больше единиц.
    Например.

13. Задан числовой массив. Нужно проверить, что все значения в массиве одинаковые.
    Например.

14. Задан числовой массив. Нужно проверить, что в массиве есть последовательности из трех и больше одинаковых чисел.
    Например.

15. Задан числовой массив. Нужно реализовать метод кольцевого двига на N. int[] shift(). 
    Не использовать дополнительный массив.
    Например, [1, 2, 3, 4, 5] - shift(2) - [4, 5, 1, 2, 3]

16. Задан квадратный массив. Нужно проверить. что в нем есть выгрышные варианты для игры крестики-нолики.

17. Реализован банкомат размена денег. Автомат примает бумажную купюру и обменивает на монеты. 
    Метод должен возращать список всех возможных вариатов размены купюры.

18. Задан двойной массив заполненный нулями и единицами. Нужно определить самое большое множество единиц. 
    Множеством считается обединение единиц, которые соприкосаются друг с другом. 
    Диагональное соприкосновение не учитывать.

19. Задан двойной массив из единиц и нулей. Нужно найти минимальный путь от точки А до точки В. 
    Двигаться можно только по единицам и только по вертикали или горизонтали. 

20. Задана одномерный массив. Нужно найти все возможные варианты перестановок этого массива.
