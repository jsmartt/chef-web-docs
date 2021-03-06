.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

This resource has the following properties:
   
``atomic_update``
   **Ruby Types:** TrueClass, FalseClass

   |atomic_update| Default value: ``true``.
   
``backup``
   **Ruby Types:** FalseClass, Integer

   |backups_kept| Default value: ``5``.
   
``cookbook``
   **Ruby Type:** String

   |cookbook file_location| The default value is the current cookbook.
   
``force_unlink``
   **Ruby Types:** TrueClass, FalseClass

   |force_unlink| Default value: ``false``.
   
``group``
   **Ruby Types:** Integer, String

   |windows group_identifier|
   
``ignore_failure``
   **Ruby Types:** TrueClass, FalseClass

   |ignore_failure| Default value: ``false``.
   
``inherits``
   **Ruby Types:** TrueClass, FalseClass

   |windows| only. |inherits windows security| Default value: ``true``.
   
``manage_symlink_source``
   **Ruby Types:** TrueClass, FalseClass, NilClass

   |manage_symlink_source| Possible values: ``nil``, ``true``, or ``false``. When this value is set to ``nil``, the |chef client| will manage a symlink's source file and emit a warning. When this value is set to ``true``, the |chef client| will manage a symlink's source file and not emit a warning. Default value: ``nil``. The default value will be changed to ``false`` in a future version.
   
``mode``
   **Ruby Types:** Integer, String

   |mode resource_file|
       
   The behavior is different depending on the platform.
       
   |unix|- and |linux|-based systems: |mode *nix|
       
   |windows|: |mode windows security|
   
``notifies``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   .. include:: ../../includes_resources_common/includes_resources_common_notification_notifies.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_timers.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_notifies_syntax.rst
   
``owner``
   **Ruby Types:** Integer, String

   |owner windows security|	
   
``path``
   **Ruby Type:** String

   |path cookbook_file| |resource_block_default| For example: ``file.txt``.

   |windows|: A path that begins with a forward slash (``/``) will point to the root of the current working directory of the |chef client| process. This path can vary from system to system. Therefore, using a path that begins with a forward slash (``/``) is not recommended.
   
``provider``
   **Ruby Type:** Chef Class

   Optional. |provider resource_parameter|
   
``retries``
   **Ruby Type:** Integer

   |retries| Default value: ``0``.
   
``retry_delay``
   **Ruby Type:** Integer

   |retry_delay| Default value: ``2``.
   
``rights``
   **Ruby Types:** Integer, String

   |windows| only. |rights windows security|
   
``source``
   **Ruby Types:** String, Array

   |source cookbook_file| Can be used to distribute specific files to specific platforms. |see file_specificity| |see syntax|
   
``subscribes``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   .. include:: ../../includes_resources_common/includes_resources_common_notification_subscribes.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_timers.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_subscribes_syntax.rst
   
``verify``
   **Ruby Types:** String, Block

   |verify_file|

   .. include:: ../../includes_resources/includes_resource_cookbook_file_attributes_verify.rst

.. note:: .. include:: ../../includes_notes/includes_notes_resource_properties_use_owner_and_right.rst
