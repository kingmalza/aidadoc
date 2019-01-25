Manage Aida frontend
==================  


Active 
-----------------

From the active processes management window it is possible to execute, monitor and manage the created templates and the public variables associated to them.

.. figure:: img/active.png
   :scale: 50 %
   :alt: Aida test keywords

The window consists of the following main areas:

**General elements**

  In this area it is possible to make the type of selection with regard to the tests to be performed, the possible choices are:
  -Single Template
  -Test Group
  -TAG Aggregation
  -Project Aggregation
  
  Once selected the Test Type choice the test are will automatically filled according to the choice made in the preview section.
  Once an item has been selected, the description entered during the configuration phase will appear above the selection.
  
  The Variables session appears as soon as the selection of the test / group to be launched is carried out and contains all those data/value keys defined in the design phase of the template in the "Test Variables" area.
  
  .. note::
   For each variable at the frontend it is possible to use three different types of data management:
   
   **Scalar**: The value of the associated variable remains that for each test run
   
   **Random (Num)**: By inserting a range of numerical values in the format "<Minimum number> - <Maximum number>" each time the test is   performed, the system will enter a random numerical value contained within the specified intervals.
   
   **Random (String)**: By entering the number of characters of which the string should be composed, the system automatically at each run cycle will insert a random string with the number of characters defined in the test


   At the base of the section it is possible to go and schedule the repetitiveness of the execution; this can be set to:

   **Once**: The test is performed only once
   **Every Minutes**: specifying the value of the minutes of waiting between one execution and another the test is performed until the manual stop by the user every n minutes defined.
   **Every hour**: No input value requested by the user; The test is performed until the user stops every hour starting from the first execution.
   **Every Day**: By entering the time in the format HH: MM the test is repeated until the manual syop by the user at the same time every day.
   
   .. figure:: img/active_general.png



History
-----------------


.. _using2-label:

Libraries
-----------------


.. _using3-label:

Keywords
-----------------
