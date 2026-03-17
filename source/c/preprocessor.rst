Preprocessing Directives
========================

Overview [1]_
~~~~~~~~~~~~~

Preprocessing processes the program before the actual compilation. They are seprate from compilation and modify the code before it.

The 4 types of preprocessing are:

- Macros
- File inclusions
- Conditional Compilation
- Other Directives

Macros
~~~~~~

Macros are used to define constants or create functions that are substituted by the preprocessor before the code is compiled. The two preprocessors ```#define``` and ```#undef``` are used to create and remove macros in C.

.. code-block:: c

	#define token value
	#undef token

where after preprocessing, the token will be expanded to its value in the program.

.. code-block:: c

	#include <stdio.h>

	#define LIMIT 5

	int main() {
		for(int i = 0; i < LIMIT; i++) {
			printf("%d\n", i);
		}
		return 0;
	}



File inclusions
~~~~~~~~~~~~~~~

Conditional Compilation
~~~~~~~~~~~~~~~~~~~~~~~

Other Directives
~~~~~~~~~~~~~~~~

.. rubric:: References

	[1] https://www.geeksforgeeks.org/c/cc-preprocessors/