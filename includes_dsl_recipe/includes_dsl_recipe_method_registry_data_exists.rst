.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

Use the ``registry_data_exists?`` method to find out if a |windows| registry key contains the specified data of the specified type under the value. 

.. note:: .. include:: ../../includes_notes/includes_notes_registry_key_not_if_only_if.rst

The syntax for the ``registry_data_exists?`` method is as follows:

.. code-block:: ruby

   registry_data_exists?(
     KEY_PATH, 
     { :name => 'NAME', :type => TYPE, :data => DATA }, 
     ARCHITECTURE
   )

where:

* ``KEY_PATH`` is the path to the registry key value. |key_name resource registry_key hives|
* ``{ :name => 'NAME', :type => TYPE, :data => DATA }`` is a hash that contains the expected name, type, and data of the registry key value
* |values resource registry_key types|
* ``ARCHITECTURE`` is one of the following values: ``:x86_64``, ``:i386``, or ``:machine``. |architecture registry_key machine|

This method will return ``true`` or ``false``. 

.. note:: .. include:: ../../includes_notes/includes_notes_registry_key_architecture.rst
