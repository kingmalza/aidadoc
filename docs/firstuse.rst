Using Aida as a Test Suite
===========================

Aida is a test suite based on robotframework and selenium that allows you to perform almost any type of test on any environment you want.
To test with Aida you must first create a template that can then be run by different users and with different values from the Aida testing engine.

Once logged in to the system, to go to configure a test you need to use the **Templates Manager** link from the main menu:

.. figure:: img/template_main.png
   :scale: 50 %
   :alt: Aida login page


1-Main Templates
-----------------

Once you have selected the step to be created for creating the template, you will be presented with the form containing the list of data present in that session, simply go to select the **ADD ..** button to add a new record or select a value existing to be able to manage it.

.. figure:: img/template1.png
   :scale: 50 %
   :alt: Aida login page

* **Description**: Template name that is being created
* **Note**: Additional information regarding the template you are going to create

.. warning::
   * **API Owner**: User to the interaction rights will be assigned through API to the specific table. Only the selected user can manage API calls to that specific data


2-Test Cases
-----------------

The page dedicated to the creation / modification of the tet cases allows authirized users to create and associate all the test cases that you want to include to a main template.

.. figure:: img/test_cases.png
   :scale: 50 %
   :alt: Aida test cases

By selecting an existing test case it's possible to modify the data (Template id, description of the test case and API owner), while using the "**ADD 2-TEST CASE**" button it will be possible to insert a new test case.


3-Test Variables
-----------------

The variable management mask allows to associate to the main template key / value associations that can be managed by the main test execution mask by the tester in charge

.. figure:: img/test_variables.png
   :scale: 50 %
   :alt: Aida test variables


.. note::
   These settings influence the display of the frontend side template and manage the possibility of inserting and modifying the values in execution of the test.
If you need to insert data that can not be modified during the test execution phase, these should not be inserted in this form.

.. figure:: img/frontend_variables.png
   :scale: 50 %
   :alt: Aida test variables

The template for managing / inserting the variables provides for selecting the main template to which the data is to be linked, the name of the variable and any value (it is also possible to leave it null)

.. figure:: img/variables_add.png
   :scale: 50 %
   :alt: Aida test variables


4-Test Settings
-----------------


5-Test Cases Main Chain
-----------------


6-Keywords Link Chain
-----------------
