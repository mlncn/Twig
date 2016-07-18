``striptags``
=============

The ``striptags`` filter strips SGML/XML tags and replace adjacent whitespace
by one space:

.. code-block:: jinja

    {{ some_html|striptags }}

.. note::

    Internally, Twig uses the PHP `strip_tags`_ function.

.. _`strip_tags`: http://php.net/strip_tags

This means that you can pass "allowable tags" to *not* strip, like so:

.. code-block:: jinja

    {{ some_html|striptags('div,p,table,span,a') }}

This will strip all tags from the some_html string *except* div, p, table, span, and a tags.
