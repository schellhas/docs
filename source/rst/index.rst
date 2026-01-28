reStructuredText
================

Table of Contents
-----------------

Code:

.. code-block:: rst

	.. toctree::
		:maxdepth: 2
		:caption: reStructuredText

		dir/file1
		dir/file2
		dir2/file1
		dir3/file

I can't build a toc here because it's a single document, just trust.

Note
----

Code:

.. code-block:: rst

	.. note::
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

Code:

.. code-block:: rst

	.. list-table:: Caption
		:header-rows: 1

		* - Logical resource
		  - Real (physical) resource
		* - "thought up" for organizational reasons realized by real resources. Examples: file, window, ...
		  - real existence, to be touched. Examples: disc, keyboard, ...

Output:

.. list-table:: Caption
	:header-rows: 1

	* - Logical resource
	  - Real (physical) resource
	* - "thought up" for organizational reasons realized by real resources. Examples: files, window, ...
	  - real existence, to be touched. Examples: disc, keyboard, ...

Code:

.. code-block:: rst

	.. list-table:: Caption
		:header-rows: 1

		* - Column 1
		  - Column 2
		  - Column 3
		* - Row 1, Column 1
		  - Row 1, Column 2
		  - Row 1, Column 3
		* - Row 2, Column 1
		  - Row 2, Column 2
		  - Row 2, Column 3
		* - Row 3, Column 1
		  - Row 3, Column 2
		  - Row 3, Column 3

Output:

.. list-table:: Caption
	:header-rows: 1

	* - Column 1
	  - Column 2
	  - Column 3
	* - Row 1, Column 1
	  - Row 1, Column 2
	  - Row 1, Column 3
	* - Row 2, Column 1
	  - Row 2, Column 2
	  - Row 2, Column 3
	* - Row 3, Column 1
	  - Row 3, Column 2
	  - Row 3, Column 3

Monospaced
----------

Code:

.. code-block:: rst

	``I am written in monospaced font``

Output:

``I am written in monospaced font``

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

Available languages/syntax-highlightings:

Langs:

- ``c``
- ``cpp``, ``c++``
- ``asm``, ``nasm``
- ``rust``
- ``go``
- ``kotlin``
- ``java``
- ``scala``
- ``python``

Script:

- ``bash``,  ``sh``
- ``lua``

Web:

- ``html``
- ``css``
- ``javascript``, ``js``
- ``typescript``
- ``json``
- ``xml``
- ``yaml``, ``yml``

Also:

- ``sql``
- ``toml``
- ``docker``, ``dockerfile``
- ``make``, ``makefile``
