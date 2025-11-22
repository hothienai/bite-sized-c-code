Read multiple integers in one line
==================================

How to read multiple integers in one line?
Let's take a look at an example of reading and printing two integers from a single line of input using ``scanf()`` and ``printf()``.

Source code
---------------------------

.. code-block:: c

   #include <stdio.h>

   int main() {
       int input_a = 0;
       int input_b = 0;

       /* read two integers from stdin */
       scanf("%d %d", &input_a, &input_b);

       /* print the integers to stdout */
       printf("You input: %d %d\n", input_a, input_b);

       return 0;
   }

Console Output
---------------------------

.. code-block:: console

   $ ./a.exe
   42 24                   # User types '42 24' and presses Enter
   You input: 42 24        # Program output

Explanation
---------------------------

- ``scanf("%d %d", &input_a, &input_b)``: reads two integers from standard input and stores them in ``input_a`` and ``input_b`` (returns the number of items read); ``%d`` is the format specifier for integers.
- ``printf("You input: %d %d\n", input_a, input_b)``: prints the stored integers followed by a newline.