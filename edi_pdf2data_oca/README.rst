===============
Pdf2data Import
===============

.. !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-LGPL--3-blue.png
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fedi-lightgray.png?logo=github
    :target: https://github.com/OCA/edi/tree/14.0/edi_pdf2data_oca
    :alt: OCA/edi
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/edi-14-0/edi-14-0-edi_pdf2data_oca
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runbot-Try%20me-875A7B.png
    :target: https://runbot.odoo-community.org/runbot/226/14.0
    :alt: Try me on Runbot

|badge1| |badge2| |badge3| |badge4| |badge5| 

This module allows to define templates used to process pdfs.
It could be used to import invoices or other kinds of PDFs.

**Table of contents**

.. contents::
   :local:

Configuration
=============

In order to create a new template type, we need to create a new module that adds a new
kind of component

.. code-block:: python

    class MyComponent(Component):
        _name = "component.name"
        _inherit = "edi.input.process.pdf2data.base"
        _exchange_type = "My template code"

        def process_data(self, data, template, file):
            "To implement what it should do"

Usage
=====

You can use the wizard to import a specific a document, it will detect automatically
which is the best template and process it accordingly.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/edi/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed
`feedback <https://github.com/OCA/edi/issues/new?body=module:%20edi_pdf2data_oca%0Aversion:%2014.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* CreuBlanca

Contributors
~~~~~~~~~~~~

* Alba Riera
* Enric Tobella

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

.. |maintainer-etobella| image:: https://github.com/etobella.png?size=40px
    :target: https://github.com/etobella
    :alt: etobella

Current `maintainer <https://odoo-community.org/page/maintainer-role>`__:

|maintainer-etobella| 

This module is part of the `OCA/edi <https://github.com/OCA/edi/tree/14.0/edi_pdf2data_oca>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
