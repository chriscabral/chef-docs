.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This configuration file has the following settings:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``couchdb['batch_save_interval']``
     - The time in milliseconds within which we will save documents to disk, regardless of how many have been written. Default value: ``1000``.
   * - ``couchdb['batch_save_size']``
     - The number of documents that will trigger a batch save. Default value: ``1000``.
   * - ``couchdb['bind_address']``
     - The address that CouchDB will bind to. Default value: ``"127.0.0.1"``.
   * - ``couchdb['data_dir']``
     - Where CouchDB will store its on-disk data. While this attribute can be changed, we recommend you do not deviate from our typical, supported layout. Default value: ``"/var/opt/opscode/couchdb/db"``.
   * - ``couchdb['delayed_commits']``
     - Whether commits are delayed. For performance, we tune CouchDB to batch commits according to the ``batch_save_interval`` and ``batch_save_size`` options above. Default value: ``"true"``.
   * - ``couchdb['dir']``
     - The base directory for CouchDB data. While this attribute can be changed, we recommend you do not deviate from our typical, supported layout. Default value: ``"/var/opt/opscode/couchdb"``.
   * - ``couchdb['enable']``
     - Whether the CouchDB service is enabled on this server or not. Usually managed by the ``role`` a server has in its ``server`` entry. Default value: ``true``.
   * - ``couchdb['ha']``
     - Whether CouchDB is running in an HA configuration. Typically managed by the ``topology`` of the cluster and the ``role`` this server plays. Causes the CouchDB service to be ``down`` by default. Default value: ``false``.
   * - ``couchdb['log_directory']``
     - The base directory for CouchDB log data. While this attribute can be changed, we recommend you do not deviate from our typical, supported layout. Default value: ``"/var/log/opscode/couchdb"``.
   * - ``couchdb['log_level']``
     - The verbosity of the CouchDB logs. Options: ``error`` (default): Only log errors; ``info``: Log high level connection information; ``debug``: Low level debugging information. Default value: ``"error"``.
   * - ``couchdb['log_rotation']``
     - Default value: ``xxxxx``.
   * - ``couchdb['max_attachment_chunk_size']``
     - The maximum attachment size. Default value: ``"4294967296"``.
   * - ``couchdb['max_dbs_open']``
     - The maximum number of open databases. Default value: ``10000``.
   * - ``couchdb['max_document_size']``
     - The maximum size of a document. Default value: ``"4294967296"``.
   * - ``couchdb['os_process_timeout']``
     - How long before timing out external processes, in milliseconds. Default value: ``"300000"``.
   * - ``couchdb['port']``
     - The port CouchDB will listen on. Default value: ``5984``.
   * - ``couchdb['svlogd_num']``
     - For the svlogd-managed 'current' log set a retention policy based on the number of logfiles retained. Default value: ``10``.
   * - ``couchdb['svlogd_size']``
     - For the svlogd-managed 'current' log set a rotation policy based on the size, in bytes, of the logfile. Default value: ``1000000``. 
   * - ``couchdb['reduce_limit']``
     - Disable limiting the number of reduces. Default value: ``"false"``.
   * - ``couchdb['vip']``
     - The IP address that other services needing access to CouchDB should use. This option is typically set by the ``topology`` and ``role`` a server plays. Default value: ``"127.0.0.1"``.