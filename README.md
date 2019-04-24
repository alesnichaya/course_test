# Java Test Course

Course purpose
----------

Check the logical and algorithmic abilities of the student to engage in professional programming.
Candidates who have completed all the tasks can safely continue to learn programming,
because they have a good potential to become highly skilled software developers.
Candidates who have difficulty performing these tasks should pay attention
to related areas of software development, such as: QA Automation, analyst, functional programmer, support.

Description
--------

The course contains 20 tasks of increasing complexity. Each task consists of a prepared class framework and
fully written automatic tests. That is, all tasks will be automatically checked.
This course uses the TDD approach. Tools required to complete the course: Maven, Git, Java 8.

To get the source code you need to run the command

*git clone git@github.com:peterarsentev/course_test.git*

Project to collect through maven. Course assignments are in separate packages.

*/src/main/java/ru/parsentev/task_XXX/package-info.java*

as well as duplicated below.

The student should familiarize himself with the task and proceed to the implementation of the missing code and classes.
After completion of the implementation, the student should go to the folder

*/src/test/java/ru/parsentev/task_XXX/*

and remove annotation in each class

*@Ignore* - This annotation is used to ignore tests.

after that the student must go to the root of the project and execute the command

*mvn clean test*

The build system must pass all tests successfully. If tests have fallen, you need to fix your code.
Test code cannot be edited.

There are two branches in the repository.

- master - skeleton assignments with tests.
- solution - fully completed tasks with tests.

Watch the solution is recommended after the successful implementation of the code and successfully passed tests.

As a theoretical material to prepare for the course should read the following books:

*Head First Java, 2nd Edition: Kathy Sierra, Bert Bates*

*Algorithms. Design Guide, Stephen S. Skien*

Topics required to complete the course.

- Data types
- Arithmetic operations
- Condition Operators
- Cycles
- Arrays
- Inheritance
- Polymorphism
- Encapsulation
- Exceptions

Tasks
-------

1.Implement a program calculator. The calculator must perform the following operations:
   addition, subtraction, multiplication, division, exponentiation.
   When performing a division, enter a check to 0.
   If the second argument 0 needs to throw a java.lang.IllegalStateException exception
   
2. Implement a class point describing a point in the x, y coordinate system - Point (x, y).
   the object point must have methods double Point # distanceTo (Point point) - the method must calculate the distance
   between two points.

3. Implement a class triangle. The triangle should be described through points in the coordinate system.
   The triangle object must have methods:
   boolean exists () - checks whether a triangle exists or not.
   double area () - calculates the area of ​​a triangle.
   If the triangle does not exist, throw a java.lang.IllegalStateException exception.
   
4. Implement the class isosceles triangle inheriting the class triangle from the task 3.
   Supplement the behavior of the boolean exists () method - true if the triangle is isosceles.
   Remaining behavior to remain the same.

5. Implement the class of a right triangle by inheriting the class of a triangle from task 3.
   Supplement the behavior of the boolean exists () method - true if the triangle is equilateral.
   Remaining behavior to remain the same.

6. Implement the class square based on the four points Point (x, y).
   boolean exists () - checks whether the square exists or not.

7. Implement the Expression class. The class must accept a string from a simple mathematical expression.
   and methods double calc (). Must support + - / * exp operations.
   For example, "2 + 2" - 4, "2-2" - 0
   If the expression is not correct, throw a java.lang.IllegalStateException exception.

8. Implement a class that computes prime numbers up to N.

9. Implement the method of counting unique characters in a string.

10. Implement the validation methods for open and closed brackets.
    For example, () (() ((()))) - true, ()) - false
 
11. An array of numbers is given with values ​​of 0 and 1. It is necessary to check that all values ​​in the array are equal to 1.
    For example, [0, 1] - false, [1, 1] - true,

12. An array of numbers is specified with the values ​​0 and 1.
    It is necessary to check that the array has a sequence of three or more units.
    For example, [0, 1, 1] is false, [1, 1, 1] is true,

13. A numeric array is specified. We need to check that all the values ​​in the array are the same.
    For example, [0, 0, 0] is true, [1, 1, 1] is true, [0, 1, 1] is false,

14. The proposal is given. Need to rearrange the words in the reverse order.
    For example, "program and earn" -> "earn and program"

15. A numeric array is specified. You need to implement a ring-shift method on N. int [] shift ().
    Do not use additional array.
    For example, [1, 2, 3, 4, 5] - shift (2) - [4, 5, 1, 2, 3]

16. Set a square array. You need to check that it has winning options for playing tic-tac-toe.

17. Implemented ATM money exchange. The machine accepts a paper bill and exchanges for coins.
    The method should return a list of all possible options for exchanging bills.

18. A double array filled with zeros and ones is set. It is necessary to determine the largest set of units.
    Considered to be a combination of units that are in contact with each other.
    Diagonal contact is not considered.

19. A double array of ones and zeros is set. We need to find the minimum path from point A to point B.
    You can only move on units and only vertically or horizontally.

20. Set one-dimensional array. It is necessary to find all possible variants of permutations of this array.
