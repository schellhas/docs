Overview
========

.. epigraph::

	Utter design is achieved not when there is nothing more to add, but rather there is nothing more to take away.

	-- Antoine de Saint-Exupéry

The two main tasks of an OS
---------------------------

1. Providing a virtual machine to abstract the hardware
2. Management of resources

What services does an OS usually provide?
-----------------------------------------

Inside the kernel in a microkernel system:

- process management
- process communication/IPC

Other services (could or could not be in the kernel):

- memory management
- file system
- networking
- security
- and many more: users, time, terminals, ...