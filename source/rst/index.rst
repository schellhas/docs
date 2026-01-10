reStructuredText
================

Table of Contents
-----------------

Code:

.. code-block:: rst

	.. toctree::
		:maxdepth: 2
		:caption: reStructuredText

		Code-Block
		Note
		Warning
		List
		Monospaced

Output:

.. toctree::
	:maxdepth: 2
	:caption: reStructuredText

		Code-Block
		Note
		Warning
		List
		Monospaced

Code-Block
----------

Code:

.. code-block:: rst

	.. code-block:: c

		#include <stdio.h>

		int main() {
			printf("Hello, world!\n");

			return 0;
		}

Output:

.. code-block:: c

	#include <stdio.h>

	int main() {
		printf("Hello, world!\n");

		return 0;
	}

Code:

.. code-block:: rst

	.. code-block:: bash
		sudo apt install gcc

Output:

.. code-block:: bash
	sudo apt install gcc

Code:

.. code-block:: rst

	.. code-block:: sql
		SELECT * 
		FROM table;

Output:

.. code-block:: sql
	SELECT * 
	FROM table;

Note
----

Code:

.. code-block:: rst

	.. wnote::
		This is a note.
		It can span multiple lines.

Output:

.. note::
	This is a note.
	It can span multiple lines.

Code:

.. code-block:: rst

	.. note:: This is a shorter note.

Output:

.. note:: This is a shorter note.

Warning
-------

Code:

.. code-block:: rst

	.. warning::
		This is a warning!
		It can span multiple lines!

Output:

.. warning::
	This is a warning!
	It can span multiple lines!

Code:

.. code-block:: rst

	.. warning:: This is a shorter warning!

Output:

.. warning:: This is a shorter warning!

List
----

Code:

.. code-block:: rst

	- You can display
	- things in a list
	- like this

Output:

- You can display
- things in a list
- like this

Monospaced
----------

Code:

.. code-block:: rst
	
	``I am written in monospaced font``

Output:

``I am written in monospaced font``