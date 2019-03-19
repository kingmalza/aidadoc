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


List of browseable tables
-----------------
