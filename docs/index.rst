.. AidaDocs documentation master file, created by
   sphinx-quickstart on Mon Sep 10 11:12:51 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to AidaDocs's documentation!
====================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   intro
   strings
   datatypes
   numeric


Intro section
==============

.. toctree::
   :maxdepth: 2
   :caption: intro:

This application enables Django powered websites to have multiple tenants via PostgreSQL schemas. A vital feature for every Software-as-a-Service website.

Django provides currently no simple way to support multiple tenants using the same project instance, even when only the data is different. Because we don’t want you running many copies of your project, you’ll be able to have:

- Multiple customers running on the same instance
- Shared and Tenant-Specific data
- Tenant View-Routing

What is Aida
-------------------
A schema can be seen as a directory in an operating system, each directory (schema) with it’s own set of files (tables and objects). This allows the same table name and objects to be used in different schemas without conflict. For an accurate description on schemas, see PostgreSQL’s official documentation on schemas.


Strings section
==============

.. toctree::
   :maxdepth: 2
   :caption: strings:
   
  Test strings 

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`


Welcome
==============

Subsection Header
-----------------
- A bullet list item
- Second item

  - A sub item

- Spacing between items creates separate lists

- Third item

1) An enumerated list item

2) Second item

   a) Sub item that goes on at length and thus needs
      to be wrapped. Note the indentation that must
      match the beginning of the text, not the 
      enumerator.

      i) List items can even include

         paragraph breaks.
         
Using Aida Test Suite
==============

Testset
-----------------

Templates
-----------------

Files
-----------------

Advanced Usage
==============

Support
==============

Ticketing system
-----------------

Get Involved!
==============
