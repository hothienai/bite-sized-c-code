Read a Single Character
===============================

C provides built-in functions for character I/O. The common ones are ``getchar()``, ``putchar()``, ``scanf()``, and ``printf()``.

Read and print a single character with ``scanf()`` and ``printf()``
---------------------------------------------------------------------------

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>

   int main() {

      char input_char = 'A';

      /* read one character from stdin */
      scanf("%c", &input_char);

      /* print the character to stdout */
      printf("You input: %c\n", input_char);

      return 0;
   }

Console Output
~~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   A                    # User types 'A' and presses Enter
   You input: A         # Program output

Explanation
~~~~~~~~~~~

- ``scanf("%c", &chr)``: reads one character from standard input and stores it in ``chr`` (returns the number of items read); ``%c`` is the format specifier for characters.
- ``printf("Character: %c\n", chr)``: prints the stored character followed by a newline.


Read and print a single character with ``getchar()`` and ``putchar()``
--------------------------------------------------------------

Source code
~~~~~~~~~~~

.. code-block:: c

   #include <stdio.h>

   int main() {
   
      char input_char = 'A';

      /* read one character from stdin */
      input_char = getchar();

      /* print the character to stdout */
      putchar(input_char);
      putchar('\n');

      return 0;
   }

Console Output
~~~~~~~~~~~~~~~

.. code-block:: console

   $ ./a.exe
   A                    # User types 'A' and presses Enter
   A                    # Program output (putchar prints 'A' then newline)

Explanation
~~~~~~~~~~~

- ``chr = getchar()``: reads one character from standard input and stores it in ``chr``.
- ``putchar(chr)``: prints the stored character to standard output.
- ``putchar('\n')``: prints a newline character to standard output.