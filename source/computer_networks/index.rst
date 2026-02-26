Computer Networks
=================

This documentation roughly follows the structure of Jochen Schiller's lecture on telematics.

https://www.mi.fu-berlin.de/inf/groups/ag-tech/teaching/resources/Course-Material.html

.. toctree::
	:maxdepth: 2

	application_layer/index
	transport_layer/index
	network_layer/index
	link_layer/index
	physical_layer/index

The root directory and internet communication in general can be decomposed in either the OSI or the TCP/IP way.

+-----------------------+-----------------------+
| OSI			| TCP/IP		|
+=======================+=======================+
| 7: Application	| Application		|
+-----------------------+-----------------------+
| 6: Presentation	|			|
+-----------------------+ Not present in model	|
| 5: Session		|			|
+-----------------------+-----------------------+
| 4: Transport		| Transport		|
+-----------------------+-----------------------+
| 3: Network		| Internet		|
+-----------------------+-----------------------+
| 2: Data link		|			|
+-----------------------+ Host-to-network	|
| 1: Physical		|			|
+-----------------------+-----------------------+