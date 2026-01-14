apt (Package Manager)
=====================

Normal/Intended way of removing applications
--------------------------------------------

Fast Overview
~~~~~~~~~~~~~

.. code-block:: bash

	sudo apt purge packet-name
	sudp apt autoremove
	sudo apt clean

Overview
~~~~~~~~

See installed packages

.. code-block:: bash

	apt list --installed | grep name
	# or
	dpkg -i | grep name

Remove program (config stays)

.. code-block:: bash

	sudo apt remove packet-name

Remove completely (with config)

.. code-block:: bash

	sudo apt purge packet-name

Remove unused dependencies

.. code-block:: bash

	sudo apt autoremove

Clean cache

.. code-block:: bash

	sudo apt clean