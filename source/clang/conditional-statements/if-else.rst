If-Else Statements in C
===============================

If-Else statements are used to perform different actions based on different conditions. The syntax for an if-else statement in C is as follows:

.. code-block:: c

   if (condition A) {
      /* code to be executed if condition A is true */
   } 
   else if (condition B) {
      /* code to be executed if condition B is true */
   } 
   ...
   else {
      /* code to be executed if all above conditions are false */
   }

In this structure:

- The ``if`` block checks the first condition (condition A). If it evaluates to true the code inside the ``if`` block is executed.

- The ``else if`` (optional) block checks the second condition (condition B) only if condition A is false. If condition B is true, the code inside the ``else if`` block is executed.

- The ``else`` (optional) block is executed if none of the previous conditions are true.

Comparision Conditions with If-Else
----------------------------------

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>

   int main() {

      int a = 10;
      int b = 20;

      if (a > b) {
          printf("a is greater than b\n");
      } 
      else if (a < b) {
          printf("a is less than b\n");
      }
      else {
          printf("a is equal to b\n");
      }

      return 0;
   }

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   a is less than b

Explanation
~~~~~~~~~~~
- ``if (a > b)``: checks if ``a`` is greater than ``b``. If true, it prints "a is greater than b".
- ``else if (a < b)``: checks if ``a`` is less than ``b``. If true, it prints "a is less than b".
- ``else``: executed if neither of the above conditions are true, meaning ``a``

Logical Conditions with If-Else
---------------------------------------------

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>
   #include <stdbool.h>

   int main() {

      bool flag_A = true;
      bool flag_B = false;

      if (flag_A && flag_B) {
          printf("Both Condition A and Condition B are true\n");
      }
      else if (flag_A || flag_B) {
          printf("At least one of Condition A or Condition B is true\n");
      }
      else {
          printf("Both Condition A and Condition B are false\n");
      }

      return 0;
   }

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   Condition A is true and Condition B is false

Explanation
~~~~~~~~~~~

- ``if (flag_A && flag_B)``: checks if both ``flag_A`` and ``flag_B`` are true. If true, it prints "Both Condition A and Condition B are true".
- ``else if (flag_A || flag_B)``: checks if at least one of ``flag_A`` or ``flag_B`` is true. If true, it prints "At least one of Condition A or Condition B is true".
- ``else``: executed if neither of the above conditions are true, meaning both ``flag