Switch-Case Statements in C
===============================

Switch-Case statements are used to perform different actions based on the value of a variable or expression. The syntax for a switch-case statement in C is as follows:

.. code-block:: c

   switch (expression) {
      case constant1:
          /* code to be executed if expression equals constant1 */
          break;
      case constant2:
          /* code to be executed if expression equals constant2 */
          break;
      ...
      default:
          /* code to be executed if expression doesn't match any case */
   }

In this structure:

- The ``switch`` statement evaluates the ``expression`` once and compares its value against the values specified in each ``case``.
- If a match is found, the code block associated with that ``case`` is executed.
- The ``break`` statement is used to exit the switch-case structure after executing a case block. If ``break`` is omitted, execution will continue to the next case (this is known as "fall-through").
- The ``default`` case is optional and is executed if none of the specified cases match the expression's value.

A simple example of using switch-case
----------------------------------

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>

   int main() {

      int day = 3;

      switch (day) {
          case 1:
              printf("Monday\n");
              break;
          case 2:
              printf("Tuesday\n");
              break;
          case 3:
              printf("Wednesday\n");
              break;
          case 4:
              printf("Thursday\n");
              break;
          case 5:
              printf("Friday\n");
              break;
          case 6:
              printf("Saturday\n");
              break;
          case 7:
              printf("Sunday\n");
              break;
          default:
              printf("Invalid day\n");
      }

      return 0;
   }

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   Wednesday

Explanation
~~~~~~~~~~~
- ``switch (day)``: evaluates the variable ``day``.
- ``case 1:`` to ``case 7:``: checks if ``day`` matches any of these values (1 to 7). If it matches, the corresponding code block is executed.
- ``break;``: exits the switch-case structure after executing the matched case block.

Example of fall-through behavior
---------------------------------

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>

   int main() {

      int number = 2;

      switch (number) {
          case 1:
              printf("One\n");
          case 2:
              printf("Two\n");
          case 3:
              printf("Three\n");
              break;
          default:
              printf("Number not in range 1-3\n");
      }

      return 0;
   }

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   Two
   Three

Explanation
~~~~~~~~~~~

- In this example, since there are no ``break;`` statements after cases 1 and 2, when ``number`` is 2, it prints "Two" and then continues to execute the code in case 3, printing "Three" as well. This demonstrates the fall-through behavior of switch-case statements in C.
