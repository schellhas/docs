Pointers and Arrays
===================

A pointer is a variable that contains the address of a variable. [KR]_

Pointers and Addresses [KR]_
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The unary operator ``&`` gives the address of an object, so the statement ``p = &c`` assigns the address of ``c`` to the variable ``p``, and ``p`` is said to *point* to ``c``. The ``&`` operator only applies to objects in memory: variables and array elements. It cannot be applied to expressions, constants, or register values.

The unary operator ``*`` is the *indirection* or *dereferencing* operator; it accesses the value of the address the pointer stores.

Example:

.. code-block:: c

	int x = 1;
	int y = 2;
	int z[10];
	int* ip;	/* ip is a pointer to an int */

	ip  = &x;	/* ip now points to x */
	y   = *ip;	/* y is now 1 */
	*ip = 0;	/* x is now 0 */
	ip  = &z[0];	/* ip now points to z[0] */



.. rubric:: References

.. [KR] Kernighan, Ritchie - The C Programming Language
