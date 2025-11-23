Read Multiple Numbers
==================================

How to read multiple integers in one line?
Let's take a look at an example of reading and printing two integers from a single line of input using ``scanf()`` and ``printf()``.

Read multiple number in one line
----------------------------------

Source code
~~~~~~~~~~~

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

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   42 24                   # User types '42 24' and presses Enter
   You input: 42 24        # Program output

Explanation
~~~~~~~~~~~

- ``scanf("%d %d", &input_a, &input_b)``: reads two integers from standard input and stores them in ``input_a`` and ``input_b`` (returns the number of items read); ``%d`` is the format specifier for integers.
- ``printf("You input: %d %d\n", input_a, input_b)``: prints the stored integers followed by a newline.

Read multiple numbers in multiple lines
----------------------------------------

You can also use the same code as above to read numbers from multiple lines. The difference is the way you provide the input.

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   42                      # User types '42' and presses Enter,
   24                      # then '24' and presses Enter
   You input: 42 24        # Program output

Another approache is to call ``scanf()`` multiple times to read each number separately.

Source code
~~~~~~~~~~~
.. code-block:: c

   #include <stdio.h>

   int main() {

       float input_a = 0;
       float input_b = 0;

       /* read first integer from stdin */
       scanf("%f", &input_a);

       /* read second integer from stdin */
       scanf("%f", &input_b);

       /* print the integers to stdout */
       printf("You input: %0.2f %0.2f\n", input_a, input_b);

       return 0;
   }

Console output
~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   25.305                        # User types '25.305' and presses Enter,
   20.198                        # then '20.198' and presses Enter
   You input: 25.31 20.20        # Program output