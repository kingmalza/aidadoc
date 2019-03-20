API Documentation
==============

Aida integrates the ability to interact with its database through API interface.
Using methods calls like GET, POST, DELETE, PUT, it is possible to interface with external programs or to perform extractions, insertions, table updates directly from code.

Using the link in the main menu "**Schema API**" it will be possible to display the page relative to the published schema of the aida tables, the manageable fields and their type and methods.

.. figure:: img/schema.png
   :scale: 50 %
   :alt: Aida test keywords
   
.. warning::
  **Methods such as INSERT, DELETE, PUT make table changes without requiring confirmation.**
  The use of this type of interaction should only be used in cases where it is absolutely safe not to cause damage to the entire system, incorrect use could lead to the impossibility of using aida with the consequent risk of irreversible data loss.
  
  Here an example of a GET call from a GUI tools (postman) to the template description table
  
.. figure:: img/postman.png
   :scale: 50 %
   :alt: Aida test keywords


A python GET call example for reteive the same data and manage its as a json object.

.. code-block:: python
   
   import requests
   
   # api-endpoint 
   URL = "http://demo.myaida.io/temp_mainapi/"

   # param defined here
   user_name = "demo"
   pass = "xxxxxxx"

   # defining a params dict for the parameters to be sent to the API 
   PARAMS = {'username':user_name, 'password':pass} 

   # sending get request and saving the response as response object 
   r = requests.get(url = URL, params = PARAMS) 

   # extracting data in json format 
   data = r.json() 
   

and with Java:

.. code-block:: java

   String urlString = "http://demo.myaida.io/temp_mainapi/?username=demo&password=xxxxx....";
   URL url = new URL(urlString);
   URLConnection conn = url.openConnection();
   InputStream is = conn.getInputStream();
   // Do what you want with that stream


In this way you can carry out any type of operation on every Aida table from external programs or sources, allowing you to interface virtually any application to your test suite.

-----------------
List of browseable tables
-----------------


temp_main
-----------------

Table containing the basic configuration data of the template such as name, notes, etc.

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_mainapi/"
   


temp_case
-----------------

Table containing all the test cases defined in aida and their association with the template.

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_caseapi/"
   
   
temp_keywords
-----------------

Table containing all the keywords defined at the level of the aida system for the creation of test cases; among the various fields are the name of the key, its most "human" definition and whether it is a standard or customized key

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_keywordsapi/"
   
   

temp_variables
-----------------

Table for mapping the key / value association with the defined variables and their connection to the main template

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_variablesapi/"
   
   

temp_pers_keywords
-----------------

Table that keeps the memory relatively the association of several keywords between them so as to be able to create complex "Keywords" sections of the test

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id
  
  standard_id -> temp_keywords.id
  
  pers_id -> temp_keywords.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_pers_keywordsapi/"
   
   
temp_test_keywords
-----------------

Table containing the data for the creation of the internal structure of the Test Case, a value / key grouping for each template

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id
  
  test_id -> temp_case.id
  
  key_id -> temp_keywords.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_test_keywordsapi/"
   
   
temp_library
-----------------

Table containing all the data entered in the Test settings session, includes type of setting (Library, Resource, Test setup, Test Teardown, etc.), the value and the associated template.

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_libraryapi/"
   
    
t_group
-----------------

Table containing data relating to the test groups created.

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_groupapi/"
   
   
t_group_test
-----------------

Table containing the group template association

.. note::
  **Foreign keyword in table:**
  
  id_grp -> t_group.id
  
  id_temp -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_group_testapi/"
   
   
t_history
-----------------

One of the main tables contains all the data relating to the execution of the tests, including the outputs in the xml and html formats of the results.

.. note::
  **Foreign keyword in table:**
  
  test_main -> temp_main.id
  
  group_id -> t_group.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_historyapi/"
   
   
t_threads
-----------------

Contains all the data relating to the threads that have been executed or are still running. Combined with the t_history table, it provides a complete overview of each test run process

.. note::
  **Foreign keyword in table:**
  
  id_test -> t_history.id
  
  id_time -> t_time.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_threadsapi/"
   
   
t_tags
-----------------

Table containing all user-defined tags

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_tagsapi/"
   
   
t_tags_route
-----------------

Table showing the Tag / Templates association

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id
  
  tag_id -> t_tags.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_tags_routeapi/"
   

