Coding Practice
---------------

.. tabbed:: cp_5_1

    .. tab:: Question

        Write a function called ``calculator`` which takes two ``double``\s, ``first`` and
        ``second``, and a ``char operation`` as parameters. ``calculator`` performs
        addition, subtraction, multiplication, or division with the two ``double``\s 
        depending on what operation is passed in (+, -, *, /). It then returns the result.
        Test your function in ``main``.

        .. activecode:: cp_5_AC_1q
           :language: cpp
           :practice: T

           #include <iostream>
           using namespace std;

           double calculator (double first, double second, char operation) {
               // Write your implementation here.
           }

           int main() {
               cout << "Your output: " << calculator (3, 6, '+') << ", Correct output: 9" << endl;
               cout << "Your output: " << calculator (19, 2, '-') << ", Correct output: 17" << endl;
               cout << "Your output: " << calculator (5, 8, '*') << ", Correct output: 40" << endl;
               cout << "Your output: " << calculator (16, 4, '/') << ", Correct output: 4" << endl;
           }


    .. tab:: Answer

        Below is one way to implement the ``calculator`` function. Using conditionals,
        we return the correct result depending on which operation was given.

        .. activecode:: cp_5_AC_1a
           :language: cpp
           :optional:

           #include <iostream>
           using namespace std;

           double calculator (double first, double second, char operation) {
               if (operation == '+') {
                   return first + second;
               }
               else if (operation == '-') {
                   return first - second;
               }
               else if (operation == '*') {
                   return first * second;
               }
               else {
                   return first / second;
               }
           }

           int main() {
               cout << "Your output: " << calculator (3, 6, '+') << ", Correct output: 9" << endl;
               cout << "Your output: " << calculator (19, 2, '-') << ", Correct output: 17" << endl;
               cout << "Your output: " << calculator (5, 8, '*') << ", Correct output: 40" << endl;
               cout << "Your output: " << calculator (16, 4, '/') << ", Correct output: 4" << endl;
           }

.. activecode:: cp_5_AC_2q
    :language: cpp
    :practice: T

    A binary number is one that is expressed in the base-2 numeral system.
    Write a function ``convertToBinary`` which takes a ``decimal`` as
    a parameter. ``convertToBinary`` takes the number in decimal, converts
    it into a binary number, and returns the binary number. Test your function
    in ``main``.
    ~~~~
    #include <iostream>
    using namespace std;

    int convertToBinary (int decimal) {
        // Write your implementation here.
    }

    int main() {
        cout << "Your output: " << convertToBinary (1) << ", Correct output: 1" << endl;
        cout << "Your output: " << convertToBinary (5) << ", Correct output: 101" << endl;
        cout << "Your output: " << convertToBinary (16) << ", Correct output: 10000" << endl;
        cout << "Your output: " << convertToBinary (31) << ", Correct output: 11111" << endl;
    }

.. tabbed:: cp_5_3

    .. tab:: Question

        An interior angle of a polygon is the angle between two adjacent 
        sides of the polygon. Each interior angle in an equilateral triangle
        measures 60 degree, each interior angle in a square measures 90 degrees,
        and in a regular pentagon, each interior angle measures 108 degrees.
        Write the function ``calculateIntAngle``, which takes a ``numSides``
        as a parameter and returns a ``double``. ``calculateIntAngle`` finds the 
        interior angle of a regular polygon with ``numSides`` sides. The formula
        to find the interior angle of a regular ngon is (n - 2) x 180 / n.

        .. activecode:: cp_5_AC_3q
           :language: cpp
           :practice: T

           #include <iostream>
           using namespace std;

           double calculateIntAngle (int numSides) {
               // Write your implementation here.
           }

           int main() {
               cout << "Your output: " << calculateIntAngle (3) << ", Correct output: 60" << endl;
               cout << "Your output: " << calculateIntAngle (4) << ", Correct output: 90" << endl;
               cout << "Your output: " << calculateIntAngle (5) << ", Correct output: 108" << endl;
               cout << "Your output: " << calculateIntAngle (8) << ", Correct output: 135" << endl;
           }


    .. tab:: Answer

        Below is one way to implement the program. Using the formula given,
        we can find the interior angle and return it. Notice how we use 180.0
        instead of 180 to avoid integer division. 

        .. activecode:: cp_5_AC_3a
           :language: cpp
           :optional:

           #include <iostream>
           using namespace std;

           double calculateIntAngle (int numSides) {
               return (numSides - 2) * 180.0 / numSides;
           }

           int main() {
               cout << "Your output: " << calculateIntAngle (3) << ", Correct output: 60" << endl;
               cout << "Your output: " << calculateIntAngle (4) << ", Correct output: 90" << endl;
               cout << "Your output: " << calculateIntAngle (5) << ", Correct output: 108" << endl;
               cout << "Your output: " << calculateIntAngle (8) << ", Correct output: 135" << endl;
           }

.. activecode:: cp_5_AC_4q
    :language: cpp
    :practice: T

    The astronomical start and end dates of the four seasons are based on the position of
    the Earth relative to the Sun. As a result, it changes every year and can be difficult to
    remember. However, the meteorological start and end dates are based on the Gregorian calendar
    and is easier to remember. Spring starts on March 1, summer starts on June 1, fall starts on 
    September 1, and winter starts on December 1. Write a function called ``birthSeason``, which takes
    two parameters, ``month`` and ``day``. ``birthSeason`` calculates which season
    the birthday falls in according to the meteorological start and returns a ``string`` with the correct season.
    For example, ``birthSeason (7, 5)`` returns "summer" since July 5 is in the summer.
    ~~~~
    #include <iostream>
    using namespace std;

    string birthSeason (int month, int day) {
        // Write your implementation here.
    }

    int main() {
        cout << "Your output: " << birthSeason (5, 3) << ", Correct output: spring" << endl;
        cout << "Your output: " << birthSeason (7, 5) << ", Correct output: summer" << endl;
        cout << "Your output: " << birthSeason (11, 24) << ", Correct output: fall" << endl;
        cout << "Your output: " << birthSeason (2, 20) << ", Correct output: winter" << endl;
    }

.. tabbed:: cp_5_5

    .. tab:: Question

        Dog owners will know that figuring out a dog's age is more complicated
        than just counting age directly. Dogs mature faster than humans do,
        so to get a more accurate calculation of a dog's age, write the
        ``dogToHumanYears`` function, which takes an ``dogAge`` as a parameter.
        ``dogToHumanYears`` converts and returns the dog's age to human years. 
        A one year old dog is 15 years old in human years; a two year old dog is 24 years old in human years. 
        Each year after the second year counts as 4 additional human years. For example, a dog that is
        3 years old is actually 28 years old in human years.

        .. activecode:: cp_5_AC_5q
           :language: cpp
           :practice: T

           #include <iostream>
           using namespace std;

           int dogToHumanYears (int dogAge) {
               // Write your implementation here.
           }

           int main() {
               cout << "Your output: " << dogToHumanYears (1) << ", Correct output: 15" << endl; 
               cout << "Your output: " << dogToHumanYears (2) << ", Correct output: 24" << endl; 
               cout << "Your output: " << dogToHumanYears (3) << ", Correct output: 28" << endl; 
               cout << "Your output: " << dogToHumanYears (5) << ", Correct output: 36" << endl; 
           }


    .. tab:: Answer

        Below is one way to implement the program. We can use a conditional to 
        check to see if the dog is one year old. If it is older than one, then 
        we can use the formula to return the correct age in human years.

        .. activecode:: cp_5_AC_5a
           :language: cpp
           :optional:

           #include <iostream>
           using namespace std;

           int dogToHumanYears (int dogAge) {
               if (dogAge == 1) {
                   return 15;
               }
               return 24 + (dogAge - 2) * 4;
           }

           int main() {
               cout << "Your output: " << dogToHumanYears (1) << ", Correct output: 15" << endl; 
               cout << "Your output: " << dogToHumanYears (2) << ", Correct output: 24" << endl; 
               cout << "Your output: " << dogToHumanYears (3) << ", Correct output: 28" << endl; 
               cout << "Your output: " << dogToHumanYears (5) << ", Correct output: 36" << endl; 
           }

.. activecode:: cp_5_AC_6q
    :language: cpp
    :practice: T

    A number is a common factor of two other numbers if it divides evenly into both of the
    other numbers. For example, 2 is a common factor of 4 and 18, because 2 goes evenly into 
    4 and 18. Write the function ``isCommonFactor``, which takes three parameters,
    ``num1``, ``num2``, and ``factor``. ``isCommonFactor`` returns ``true`` if ``factor`` is a
    factor of both ``num1`` and ``num2``, and returns ``false`` otherwise.
    ~~~~
    #include <iostream>
    using namespace std;

    bool isCommonFactor (int num1, int num2, int factor) {
        // Write your implementation here.
    }

    int main() {
        cout << "Your output: " << isCommonFactor (132, 42, 11) << ", Correct output: 0" << endl; 
        cout << "Your output: " << isCommonFactor (24, 8, 4) << ", Correct output: 1" << endl; 
        cout << "Your output: " << isCommonFactor (75, 20, 5) << ", Correct output: 1" << endl; 
        cout << "Your output: " << isCommonFactor (74, 23, 3) << ", Correct output: 0" << endl; 
    }

.. tabbed:: cp_5_7

    .. tab:: Question

        If a year is divisible by 4, then it is a leap year. However, if it is also divisible by 100,
        then it is not a leap year. However, if it is also divisible by 400, then it is a leap year.
        Thus, 2001 is not a leap year, 2004 is a leap year, 2100 is not a leap year, and 2000 is a leap year.
        Write the boolean function ``isLeapYear``, which takes a ``year`` as a parameter and returns ``true`` 
        if the year is a leap year and ``false`` otherwise. Test your function in ``main``.

        .. activecode:: cp_5_AC_7q
           :language: cpp
           :practice: T

           #include <iostream>
           using namespace std;

           bool isLeapYear (int year) {
               // Write your implementation here.
           }

           int main() {
               cout << "Your output: " << isLeapYear (2001) << ", Correct output: 0" << endl; 
               cout << "Your output: " << isLeapYear (2004) << ", Correct output: 1" << endl; 
               cout << "Your output: " << isLeapYear (2100) << ", Correct output: 0" << endl; 
               cout << "Your output: " << isLeapYear (2000) << ", Correct output: 1" << endl; 
           }


    .. tab:: Answer

        Below is one way to implement the program. We can use conditionals in this
        order to efficiently determine whether or not a given year is a leap year.

        .. activecode:: cp_5_AC_7a
           :language: cpp
           :optional:

           #include <iostream>
           using namespace std;

           bool isLeapYear (int year) {
               if (year % 400 == 0) {
                   return true;
               }
               else if (year % 100 == 0) {
                   return false;
               }
               else if (year % 4 == 0) {
                   return true;
               }
               else {
                   return false;
               }
           }

           int main() {
               cout << "Your output: " << isLeapYear (2001) << ", Correct output: 0" << endl; 
               cout << "Your output: " << isLeapYear (2004) << ", Correct output: 1" << endl; 
               cout << "Your output: " << isLeapYear (2100) << ", Correct output: 0" << endl; 
               cout << "Your output: " << isLeapYear (2000) << ", Correct output: 1" << endl; 
           }

.. activecode:: cp_5_AC_8q
    :language: cpp
    :practice: T

    In the enchanted Mushroom Forest, there are many different types of 
    mushrooms as far as the eye can see. Most of these mushrooms
    can make delicious stews and dishes, but some of them are poisonous.
    Write the function ``isPoisonous``, which takes an ``char size``,
    ``int numSpots``, and ``bool isRed`` as parameters. If a mushroom is large
    ('L') and has fewer than 3 spots, it is poisonous. If a mushroom is small ('S')
    and is red, it is poisonous. If a mushroom has fewer than 3 spots or is not red,
    it is poisonous. Otherwise, it is not. ``isPoisonous`` should return ``true`` if 
    the mushroom is poisonous and ``false`` otherwise.
    ~~~~
    #include <iostream>
    using namespace std;

    bool isPoisonous (char size, int numSpots, bool isRed) {
        // Write your implementation here.
    }

    int main() {
        cout << "Your output: " << isPoisonous ('S', 10, 0) << ", Correct output: 1" << endl; 
        cout << "Your output: " << isPoisonous ('S', 2, 1) << ", Correct output: 1" << endl; 
        cout << "Your output: " << isPoisonous ('L', 1, 1) << ", Correct output: 1" << endl; 
        cout << "Your output: " << isPoisonous ('L', 4, 1) << ", Correct output: 0" << endl; 
    }

.. tabbed:: cp_5_9

    .. tab:: Question

        We know that a factorial is the product of an integer and all the integers below it.
        For example, four factorial (4!) is 24. A triangular number is the same as a factorial,
        except you add all the numbers instead of multiplying. For example, the 1st triangular
        number is 1, the 2nd is 3, the 3rd is 6, the 4th is 10, the 5th is 15, etc. You can imagine 
        rows of dots, where each successive row has one more dot, thus forming a triangular shape.
        Write the ``triangularNum`` function, which takes an ``int n`` as a parameter and returns
        the ``n``\th triangular number. Use recursion.

        .. activecode:: cp_5_AC_9q
           :language: cpp
           :practice: T

           #include <iostream>
           using namespace std;

           int triangularNum (int n) {
               // Write your implementation here.
           }

           int main() {
               cout << "Your output: " << triangularNum (1) << ", Correct output: 1" << endl; 
               cout << "Your output: " << triangularNum (3) << ", Correct output: 6" << endl; 
               cout << "Your output: " << triangularNum (6) << ", Correct output: 21" << endl; 
               cout << "Your output: " << triangularNum (17) << ", Correct output: 153" << endl; 
           }


    .. tab:: Answer

        Below is one way to implement the program. We can use conditionals to 
        separate the base case and recursive cases. Our base case is when ``n``
        is 1, and in that case we return 1. Otherwise, we recursively
        call ``triangularNum`` on ``n-1``.

        .. activecode:: cp_5_AC_9a
           :language: cpp
           :optional:

           #include <iostream>
           using namespace std;

           int triangularNum (int n) {
               if (n == 1) {
                   return 1;
               } 
               else {
                   return n + triangularNum(n - 1);
               }
           }

           int main() {
               cout << "Your output: " << triangularNum (1) << ", Correct output: 1" << endl; 
               cout << "Your output: " << triangularNum (3) << ", Correct output: 6" << endl; 
               cout << "Your output: " << triangularNum (6) << ", Correct output: 21" << endl; 
               cout << "Your output: " << triangularNum (17) << ", Correct output: 153" << endl; 
           }

.. activecode:: cp_5_AC_10q
    :language: cpp
    :practice: T

    Write the function ``digitSum`` which takes an ``int num`` as a parameter
    and returns the sum of all its digits. For example, ``digitSum (1423)``
    would return 10. Use recursion.
    ~~~~
    #include <iostream>
    using namespace std;

    int digitSum (int num) {
        // Write your implementation here.
    }

    int main() {
        cout << "Your output: " << digitSum (123) << ", Correct output: 6" << endl; 
        cout << "Your output: " << digitSum (8739) << ", Correct output: 27" << endl; 
        cout << "Your output: " << digitSum (440) << ", Correct output: 8" << endl; 
        cout << "Your output: " << digitSum (2) << ", Correct output: 2" << endl; 
    }