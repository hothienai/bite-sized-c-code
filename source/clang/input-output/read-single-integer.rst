Read a single integer
===============================

How to read and print a single integer?

Below is an example of reading and printing a single integer using ``scanf()`` and ``printf()``.

Source code
---------------------------

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

Console Output
---------------------------

.. code-block:: console

   $ ./a.exe
   42                      # User types '42' and presses Enter
   You input: 42           # Program output

Explanation
---------------------------

- ``scanf("%d", &input_int)``: reads one integer from standard input and stores it in ``input_int`` (returns the number of items read); ``%d`` is the format specifier for integers.
- ``printf("You input: %d\n", input_int)``: prints the stored integer followed by a newline.