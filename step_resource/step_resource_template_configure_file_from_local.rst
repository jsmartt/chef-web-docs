.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

.. To configure a file from a local template:

.. code-block:: ruby

   template '/tmp/config.conf' do
     local true
     source '/tmp/config.conf.erb'
   end
