.. _hieroglyph-configuration:

=======================
 Configuration Options
=======================

.. ifslides::

   .. figure:: /_static/hieroglyphs.jpg
      :class: fill

      CC BY-SA http://www.flickr.com/photos/tamburix/2900909093/

.. ifnotslides::

   Hieroglyph supports several configuration settings, which can be set
   in the project's `Sphinx configuration file`_. If you used
   ``sphinx-quickstart`` to begin your project, this will be ``conf.py``
   in the project directory.

   .. _`Sphinx configuration file`: http://sphinx-doc.org/config.html

Basic Configuration
===================

.. confval:: autoslides

   Default: ``True``

   When ``autoslides`` is True, Hieroglyph will generate slides from
   the document sections. If autoslides is set to False, only generate
   slides from the :rst:dir:`slide` directive.

   This can be overridden on a per-document basis using the
   :rst:dir:`slideconf` directive.

.. confval:: slide_theme

   Default: ``slides``

   The theme to use when generating slides. Hieroglyph includes two
   themes, ``slides`` and ``single-level``.

   This can be overridden on a per-document basis using the
   :rst:dir:`slideconf` directive.

   See :ref:`hieroglyph-themes` for more information.

.. confval:: slide_levels

   Default: ``3``

   Number of Sphinx section_ levels to convert to slides; note that the
   document title is level 1. Heading levels greater than slide levels
   will simply be treated as slide content.

.. _section: http://sphinx-doc.org/rest.html#sections

Slide Numbers
=============

.. confval:: slide_numbers

   Default: ``False``

   If set to ``True``, slide numbers will be added to the HTML output.

Slide Footer
============

.. confval:: slide_footer

   Default: ``None``

   Text that will be added to the bottom of every slide.


Themes
======

.. confval:: slide_theme_options

   Default: ``{}``

   Theme specific options as a ``dict``.

   See :ref:`custom-css` for more information.

.. confval:: slide_theme_path

   Default: ``[]``.

   A list of paths to look for themes in.

For more information on styling and themes, see
:ref:`hieroglyph-themes`.


.. _configuring-interlinking:

Interlinking HTML Output
========================

:ref:`interlinking-html` can be enabled for slides, HTML, or both.

.. confval:: slide_link_to_html

   Default: ``False``

   Link from slides to HTML.

.. confval:: slide_link_html_to_slides

   Default: ``False``

   Link from HTML to slides.

.. confval:: slide_link_html_sections_to_slides

   Default: ``False``

   Link individual HTML sections to specific slides.

   .. ifnotslides::

      Note that :confval:`slide_link_html_to_slides` must be enabled
      for this to have any effect.

Relative Paths
--------------

The slide/HTML interlinking needs to know how to find the slide and
HTML output from the other side. There are two configuration
parameters for this. They're configured to work with Sphinx and
Hieroglyph's standard configuration (output in sub-directories of a
common build directory) by default .

.. confval:: slide_relative_path

   Relative path from HTML to slides; default: ``../slides/``

.. confval:: slide_html_relative_path

   Relative path from slides to HTML; default: ``../html/``

Additional Parameters
---------------------

.. confval:: slide_html_slide_link_symbol

   Default: §

   Text used to link between HTML sections and slides.

   This text is appended to the headings, similar to the section links
   in HTML output.
