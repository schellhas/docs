Pointers
========

Storing variable addresses
~~~~~~~~~~~~~~~~~~~~~~~~~~

A datatype becomes a pointer to a value of that type by adding a ``*``. We receive the address of a value by adding ``&`` in front of it. [#]_


.. code-block:: c

	int main() {
		int a = 1;

		int* b = &a;

Dereferencing
~~~~~~~~~~~~~

To get the value of a pointer, we can add a ``*`` in front of the pointer. [#]_

.. code-block:: c

	#include <stdio.h>

	int main() {
		int a = 1;

		int* b = &a;

		printf("%d\n", *b);

		return 0;
	}

returns:

.. code-block:: bash

	1


Sources
~~~~~~~

.. rubric:: References

.. [#] https://www.geeksforgeeks.org/c/c-pointers/
