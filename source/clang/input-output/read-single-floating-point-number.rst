Read a single floating-point number
===============================
How to read and print a single floating-point number?
It's similar to reading and printing an integer. Below is an example of reading and printing a single floating-point number using ``scanf()`` and ``printf()``.

Source code
-----------------------------------------------------------

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

Console Output
-----------------------------------------------------------

.. code-block:: console

   $ ./a.exe
   42.523                     # User types '42.523' and presses Enter
   You input: 42.52           # Program output

Explanation
-----------------------------------------------------------

- ``scanf("%f", &input_float)``: reads one floating-point number from standard input and stores it in ``input_float`` (returns the number of items read); ``%f`` is the format specifier for floating-point numbers.
- ``printf("You input: %0.2f\n", input_float)``: prints the stored floating-point number formatted to 2 decimal places, followed by a newline.
