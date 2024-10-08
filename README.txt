kubens
======

``kubens`` is a command line tool to interactively select and set
Kubernetes namespaces.

.. code:: bash

   ~$ kubens
   Current namespace: my-namespace
   Pick your namespace:

   => default
      kube-system
      my-namespace
      another-namespace
      exit

Install
-------

.. code:: bash

   pip install kubens

Clone the repo:

.. code:: bash

   $ git clone https://github.com/roubles/kubens
   $ cd kubens
   $ pip install .

Copy Code

Usage
-----

.. code:: bash

   usage: kubens [-h] [--list] [substring]


   interactively pick a k8s namespace


   positional arguments:
   substring substring to filter namespaces (must match from the beginning)


   optional arguments:
   -h, --help show this help message and exit
   -l, --list list namespaces instead of launching interactive menu

Examples
~~~~~~~~

Selecting namespaces
^^^^^^^^^^^^^^^^^^^^

To run ``kubens`` and select a namespace interactively:

.. code:: bash

   $ kubens

To run ``kubens`` and set the namespace directly if there is an exact
(or partial) match:

::

   $ kubens my-namespace

If there are multiple matches, it will show a menu to select from.

Listing namespaces
^^^^^^^^^^^^^^^^^^

To list namespaces:

.. code:: bash

   $ kubens --list

To list namespaces with a filter:

.. code:: bash

   $ kubens --list ku

This will list namespaces that start with “ku”.

Features
~~~~~~~~

-  Interactively select a Kubernetes namespace from the terminal.
-  Displays the current namespace.
-  Sets the selected namespace as the current context.
-  Lists namespaces with the ``-l`` or ``--list`` argument.
-  Filters namespaces based on a substring that must match from the
   beginning.

Requirements
~~~~~~~~~~~~

-  Python 2.7 or later
-  ``kubectl`` installed and configured
-  ``pick`` library (installed automatically with
   ``pip install kubens``)

License
~~~~~~~

This project is licensed under the Creative Commons
Attribution-Noncommercial-Share Alike license.
