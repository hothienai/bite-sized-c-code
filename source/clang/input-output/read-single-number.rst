Read a Single Number
===============================

How to read and print a single number?

Below is an example of reading and printing a single number using ``scanf()`` and ``printf()``.

Read and print a single integer
----------------------------------

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>

   int main() {

      int input_int = 0;

      /* read one integer from stdin */
      scanf("%d", &input_int);

      /* print the integer to stdout */
      printf("You input: %d\n", input_int);

      return 0;
   }

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   42                      # User types '42' and presses Enter
   You input: 42           # Program output

Explanation
~~~~~~~~~~~

- ``scanf("%d", &input_int)``: reads one integer from standard input and stores it in ``input_int`` (returns the number of items read); ``%d`` is the format specifier for integers.
- ``printf("You input: %d\n", input_int)``: prints the stored integer followed by a newline.


Read and print a single floating-point number
---------------------------------------------

The difference between reading an integer and a floating-point number lies in the format specifiers used in ``scanf()`` and ``printf()``. For floating-point numbers, we use ``%f``.

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>

   int main() {

      float input_float = 0;

      /* read one floating-point number from stdin */
      scanf("%f", &input_float);

      /* print the floating-point number to stdout */
      printf("You input: %0.2f\n", input_float);

      return 0;
   }

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   42.523                     # User types '42.523' and presses Enter
   You input: 42.52           # Program output

Explanation
~~~~~~~~~~~

- ``scanf("%f", &input_float)``: reads one floating-point number from standard input and stores it in ``input_float`` (returns the number of items read); ``%f`` is the format specifier for floating-point numbers.
- ``printf("You input: %0.2f\n", input_float)``: prints the stored floating-point number formatted to 2 decimal places, followed by a newline.
