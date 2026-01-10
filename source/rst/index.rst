reStructuredText
================

Table of Contents
-----------------

.. code-block:: rst

    .. toctree::
        :maxdepth: 2
        :caption: Caption

Code-Block
----------

.. code-block:: rst

    .. code-block:: c

        #include <stdio.h>

        int main() {
            printf("Hello, world!\n");

            return 0;
        }
    
    .. code-block:: bash
        sudo apt install gcc
    
    .. code-block:: sql
        SELECT * 
        FROM table;

Note
----

.. code-block:: rst

    .. warning::
        This is a note.
        It can span multiple lines.

.. code-block:: rst

    .. warning:: This is a shorter note.

Warning
-------

.. code-block:: rst

    .. warning::
        This is a warning!
        It can span multiple lines!

.. code-block:: rst

    .. warning:: This is a shorter warning!

List
----

.. code-block:: rst

    - You can display
    - things in a list
    - like this

Monospaced
----------

.. code-block:: rst
    
    `I am written in monospace font`