.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

This resource has the following properties:
   
``clear_sources``
   **Ruby Types:** TrueClass, FalseClass

   |clear_sources| Default value: ``false``.

   .. note:: .. include:: ../../includes_notes/includes_notes_chef_gem_use_gem_package.rst
   
``compile_time``
   **Ruby Types:** TrueClass, FalseClass

   |chef_gem compile_time| Recommended value: ``false``. The |chef client| will emit a warning when this setting is ``true``. Use a ``respond_to?`` check to ensure backward compatibility. For example:

   .. code-block:: ruby

      chef_gem 'aws-sdk' do
        compile_time false if respond_to?(:compile_time)
      end

   .. warning:: .. include:: ../../includes_notes/includes_notes_chef_gem_chef_sugar.rst
   
``ignore_failure``
   **Ruby Types:** TrueClass, FalseClass

   |ignore_failure| Default value: ``false``.
   
``notifies``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   .. include:: ../../includes_resources_common/includes_resources_common_notification_notifies.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_timers.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_notifies_syntax.rst
   
``options``
   **Ruby Type:** String

   |command options|
   
``package_name``
   **Ruby Types:** String, Array

   |name package| |resource_block_default| |see syntax|
   
``provider``
   **Ruby Type:** Chef Class

   Optional. |provider resource_parameter| |see providers|
   
``retries``
   **Ruby Type:** Integer

   |retries| Default value: ``0``.
   
``retry_delay``
   **Ruby Type:** Integer

   |retry_delay| Default value: ``2``.
   
``source``
   **Ruby Type:** String

   Optional. |source resource package|
   
``subscribes``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   .. include:: ../../includes_resources_common/includes_resources_common_notification_subscribes.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_timers.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_subscribes_syntax.rst
   
``timeout``
   **Ruby Types:** String, Integer

   |timeout|
   
``version``
   **Ruby Types:** String, Array

   |version package|
