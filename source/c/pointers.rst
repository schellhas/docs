Pointers
========

A pointer is a variable that contains the address of a variable. [KR]_

Storing variable addresses
~~~~~~~~~~~~~~~~~~~~~~~~~~

A datatype becomes a pointer to a value of that type by adding a ``*``. We receive the address of a value by adding ``&`` in front of it. [#]_


.. code-block:: c

	int main() {
		int a = 1;

		int* b = &a;

IN this example, ``b`` stores the memory address of the variable ``a``. We call it "``b`` points to ``a``".

Dereferencing
~~~~~~~~~~~~~

To get the value of the variable a pointer points to, we can add a ``*`` in front of the pointer. [#]_

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

.. [#] K&R
