Sphinx Hints
============

While the `official sphinx documentation <http://www.sphinx-doc.org/en/master/>`__ should be your go-to resource for "how should I do a certain thing in Sphinx," this page offers a list of common features that MRWolf projects will likely need:

Code Blocks
-----------

Code blocks are usually handled with the ``code-block`` directive:

.. code-block:: text

  .. code-block:: java

    System.out.println("Hello World!");

.. code-block:: java

  System.out.println("Hello World!");

Occasionally, it is convenient to sample code multiple code blocks from a single source file.  If the file is included in the project directory, then this can be done with the `literalinclude <https://www.sphinx-doc.org/en/1.5/markup/code.html#Includes>`__ directive.

If the source file is not present in the project directory, but is hosted on the web, the `remoteliteralinclude <https://pypi.org/project/sphinxcontrib-remoteliteralinclude/>`__ extension can be used.

.. TODO:: Can this work with code hosted on private repos?

Tabs
----

Tabbed content can be included by using the ``tabs`` directive (the tabs extension for Sphinx is already included in the project template):

.. code-block:: text

  .. tabs::

    .. tab:: Tab 1

      Here's some tab content!

    .. tab:: Tab 2

      Here's some other tab content!

.. tabs::

  .. tab:: Tab 1

    Here's some tab content!

  .. tab:: Tab 2

    Here's some other tab content!

Admonitions
-----------

Admonitions (such as notes and warnings), and should be used often:

.. code-block:: text

  .. note:: This is a note!

.. note:: This is a note!

The following is a list of available admonitions:

* ``attention``
* ``caution``
* ``danger``
* ``error``
* ``hint``
* ``important``
* ``note``
* ``tip``
* ``warning``
