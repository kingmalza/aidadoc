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



**System Load Chart**

The system load management graph monitors the situation related to the activity on the central system in relation to the load of the your dedicated test engine.

.. figure:: img/active_load.png
   :scale: 50 %
   :alt: Aida test keywords



**Preview**

The preview area allows you to view, once the template to be executed is selected, a representation of the test structure that will be created dynamically created by the template settings.

.. figure:: img/active_preview.png
   :scale: 50 %
   :alt: Aida test preview



History
-----------------

The management of the history in aida includes all the completed tests.
From the summary table you can go to view all the information about the tests performed and their subchilds (in case of multiple executions).
Selecting a column name automatically the whole table will be sorted by this value, first click ascending order, second one descending order. To return to original table view, simply order by ID (first column)

.. figure:: img/history.png
   :scale: 50 %
   :alt: Aida test history
  
  
Selecting a line you will be able to see the details of the whole process.

.. figure:: img/history_tline.png
   :scale: 50 %
   :alt: Aida test history
   
From this position it will be possible to view the HTML representation of the test performed using the "**RAW Html**" key, the log file of each execution using the "**Log details**" button, the details of the variables and their values used during the test execution; In case the integration with Jira is active, it will be possible to send directly to a Jira Issue, the detail of test execution and the relative log created.
   

Libraries
-----------------

Currently aida has implemented several libraries to implement test templates on practically most of the software / firmware aspects that can be tested.
The aida's built-in libraries allow to perform tests on different aspects such as:

   - Web applications
   - Mobile applications
   - Different types of files
   - FTP server
   - HTTP Requests
   - REST APIs
   - SFTP applications
   - TFTP services
   - Third-party framework like Django
   - Any GUI component

... and so on

The libraries currently installed in aida are:

.. figure:: img/lib_list.png
   :scale: 50 %
   :alt: Aida libraries

**It is possible to load custom libraries** to be used inside your templates using the "**Libraries**" link in the lateral management menu or in the "**Template Manager**" through the "ADD" function next to "LIBRARIES"

.. figure:: img/lib_add.png
   :scale: 50 %
   :alt: Aida libraries


.. note::
   Currently only libraries written in python and packaged according to the python standard (https://packaging.python.org/tutorials/packaging-projects/) are accepted.
   The loaded libraries will remain in the PENDING state until they are approved by the aida control staff.
   Once approved, they can be incorporated into the templates.
   
   
   
Keywords
-----------------
