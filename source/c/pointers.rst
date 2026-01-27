Pointers
========

Storing variable addresses
~~~~~~~~~~~~~~~~~~~~~~~~~~

A datatype becomes a pointer to a value of that type by adding a ``*``. We receive the address of a value by adding ``&`` in front of it. [#]_


.. code-block:: c

	int main() {
		int a = 1;

		int* b = &a;


Sources
~~~~~~~

.. rubric:: References

.. [#] https://www.geeksforgeeks.org/c/c-pointers/
