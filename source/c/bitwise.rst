Bitwise Operators
=================

Example: [1]_

.. code-block:: c

	#include <stdio.h>

	int main() {
		unsigned int a = 5;	/* a = 00000101 */
		unsigned int b = 9;	/* b = 00001001 */

		/* a = 00000101 *
		 * b = 00001001 *
		 * &   ________ *
		 *   = 00000001 -> 1 */
		printf("a & b = %u\n", a & b);

		/* a = 00000101 *
		 * b = 00001001 *
		 * |   ________ *
		 *   = 00001101 -> 13 */	
		printf("a | b = %u\n", a | b);

		/* a = 00000101 *
		 * b = 00001001 *
		 * ^   ________ *
		 *   = 00001100 -> 12 */
		printf("a ^ b = %u\n", a ^ b);
		
		/* ~a is the NOT operator, so flips all bits */
		printf("~a = %d\n", ~a);

		/* shifts all bits "1" to the left */
		printf("b << 1 = %u\n", b << 1);

		/* shifts all bits "2" to the right */
		printf("b >> 2 = %u\n", b >> 2);

		return 0;

.. note::

	Bitwise operation are different from logical operations in that they return integer values, not boolean values. [1]_

	Left-shift by 1 is equivalent to multiplication by 2, whilst right-shift by 1 is equivalent to division by 2 for positive values respectively. [1]_

Using the & operator we can check wether a value is odd or even in O(1) time. [1]_

.. code-block:: c

	#include <stdio.h>

	int main() {
		int x = 19;
		(x & 1) ? printf("odd") : printf("even");
		return 0;
	}

.. rubric:: References

.. [1] https://www.geeksforgeeks.org/c/bitwise-operators-in-c-cpp/