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

This bla bla bla

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_mainapi/"
   


temp_case
-----------------

This bla bla bla

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_caseapi/"
   
   
temp_keywords
-----------------

This bla bla bla

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_keywordsapi/"
   
   

temp_variables
-----------------

This bla bla bla

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_variablesapi/"
   
   

temp_pers_keywords
-----------------

This bla bla bla

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

This bla bla bla

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

This bla bla bla

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/temp_libraryapi/"
   
   
t_schedule
-----------------

This bla bla bla

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_scheduleapi/"
   
   
t_group
-----------------

This bla bla bla

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_groupapi/"
   
   
t_group_test
-----------------

This bla bla bla

.. note::
  **Foreign keyword in table:**
  
  id_grp -> t_group.id
  
  id_temp -> temp_main.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_group_testapi/"
   
   
t_history
-----------------

This bla bla bla

.. note::
  **Foreign keyword in table:**
  
  test_main -> temp_main.id
  
  group_id -> t_group.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_historyapi/"
   
   
t_threads
-----------------

This bla bla bla

.. note::
  **Foreign keyword in table:**
  
  id_test -> t_history.id
  
  id_time -> t_time.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_threadsapi/"
   
   
t_tags
-----------------

This bla bla bla

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_tagsapi/"
   
   
t_tags_route
-----------------

This bla bla bla

.. note::
  **Foreign keyword in table:**
  
  main_id -> temp_main.id
  
  tag_id -> t_tags.id

.. code-block:: python

   # api-endpoint 
   URL = "<your aida address>/t_tags_routeapi/"
   

