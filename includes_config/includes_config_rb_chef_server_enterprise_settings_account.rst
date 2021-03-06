.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This configuration file has the following settings:

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Setting
     - Description
   * - ``opscode_account['backlog']``
     - Default value: ``1024``.
   * - ``opscode_account['dir']``
     - Default value: ``"/var/opt/opscode/opscode-account"``.
   * - ``opscode_account['enable']``
     - Default value: ``true``.
   * - ``opscode_account['environment']``
     - Default value: ``"privatechef"``.
   * - ``opscode_account['ha']``
     - Default value: ``false``.
   * - ``opscode_account['listen']``
     - Default value: ``"127.0.0.1:9465"``.
   * - ``opscode_account['log_directory']``
     - Default value: ``"/var/log/opscode/opscode-account"``.
   * - ``opscode_account['port']``
     - Default value: ``9465``.
   * - ``opscode_account['proxy_user']``
     - Default value: ``"pivotal"``.
   * - ``opscode_account['session_secret_key']``
     - Default value: ``"change-by-default"``.
   * - ``opscode_account['svlogd_num']``
     - For the svlogd-managed 'current' log set a retention policy based on the number of logfiles retained. Default value: ``10``.
   * - ``opscode_account['svlogd_size']``
     - For the svlogd-managed 'current' log set a rotation policy based on the size, in bytes, of the logfile. Default value: ``1000000``. 
   * - ``opscode_account['tcp_nodelay']``
     - Default value: ``true``.
   * - ``opscode_account['umask']``
     - Default value: ``"0022"``.
   * - ``opscode_account['url']``
     - Default value: ``"http://127.0.0.1:9465"``.
   * - ``opscode_account['validation_client_name']``
     - Default value: ``"chef"``.
   * - ``opscode_account['vip']``
     - Default value: ``"127.0.0.1"``.
   * - ``opscode_account['worker_processes']``
     - Default value: ``4``.

   * - ``opscode_account['worker_timeout']``
     - Default value: ``3600``.