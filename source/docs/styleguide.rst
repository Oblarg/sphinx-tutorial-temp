MRWolf Sphinx Styleguide
========================

In order to ensure consistency across project documentation, all MRWolf Sphinx docs should follow the style guideslines described in this document.

Project Structure Guidelines
----------------------------

Filenames
^^^^^^^^^

Use only lowercase alphanumeric characters and the ``-`` (minus) symbol.

Example *legal* filenames:

* ``getting-started.rst``
* ``image-12.png``

Example *illegal* filenames:

* ``GettingStarted.rst``
* ``image_12.png``

Getting Started Page
^^^^^^^^^^^^^^^^^^^^

All documentation should include a "getting started" or "orientation" page, separate from the primary index page (which will likely be quite lengthy).  This should be the first page listed in the table of contents, and should serve to orient the reader as to the overall purpose of the project and structure of the documentation.

External Resources Page
^^^^^^^^^^^^^^^^^^^^^^^

All documentation should include an "external resources" page that links to any external documentation that is needed or helpful for understanding the project.

Contacts Page
^^^^^^^^^^^^^

All documentation should include a "contacts" page that contains company contact info for those people currently responsible for maintaining the project.  This page *must* be kept up-to-date as project personnel change.

RST Guidelines
--------------

All MRWolf Sphinx documentation should be written in reStructuredText (rst).  While Sphinx technically offers Markdown support, it is patchy and offers limited functionality, and so is not approved for MRWolf project documentation (though this may change in the future).

Paragraph Style
^^^^^^^^^^^^^^^

All paragraphs in rst documents should be single-line paragraphs.  While single linebreaks are ignored in rst parsing, it is exceedingly difficult to maintain consistent line length when modifying large blocks of existing prose; therefore, line breaks should not be used to enforce line length limits in rst source (except inside of code blocks).

Accordingly, users should configure their editor of choice to auto-wrap lines for display when working on a Sphinx documentation project.

Headings
^^^^^^^^

Headings should be in title case (all words capitalized except for articles, prepositions, and conjunctions; prepositions may be capitalized if they are effectively "part of" an idiomatic verb phrase).

The order of section heading indicators is as follows:

1. ``=`` for document titles. *Do not* use this more than *once* per article.
2. ``-`` for document sections
3. ``^`` for document sub-sections
4. ``~`` for document sub-sub-sections
5. There should be no nesting deeper than four levels; consider restructuring your document if you reach this point.

Images
^^^^^^

Images should be created with a single empty line separating text content and directive:

.. code-block:: text

  This is example text.

   .. image:: images/image-1.png

In files with large numbers of images, all images should be defined at the end of the rst file, as follows:

.. code-block:: text

  |image-1|

  |image-2|

  At the end of the document:

  .. |image-1| image:: images/image-1.png
  .. |image-2| image:: images/image-2.png

Image Files
~~~~~~~~~~~

Image files should be stored in the ``images`` subdirectory of whichever directory contains the rst file.

Image files should follow the naming scheme of ``document-title-1.png`` so on and so forth.

Image files should be of the ``.png`` or ``.jpg`` image extension. ``.gif`` is unsupported by Sphinx.

Code Blocks
~~~~~~~~~~~

Screenshots of code should *never* be used for code examples.  *Always* use a code block.

All code blocks should have their language specified for syntax highlighting.

Content Guidelines
------------------

Links to API Docs
^^^^^^^^^^^^^^^^^

Documentation should link to source-generated API docs whenever possible.  Every *new* mention of a class or method should be accompanied by a link to the class or method in the API docs.  Repeated mentions do not necessarily require repeated links - use your better judgment as to whether or not it is a good idea.  Remember, good documentation maks it *easy to find what you're looking for*.

Links to Source Code
^^^^^^^^^^^^^^^^^^^^

Direct links to source code are less-crucial than links to API docs, as example code can be shown with code blocks, however they are still appropriate in certain places.
