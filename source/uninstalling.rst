.. _pdp.uninstalling:

Uninstalling |pdp|
********************************************************************************

To uninstall |pdp|, remove all the installed packages and data / configuration files. 

.. note::

   Should you need the data files later, back up your data before uninstalling |pdp|.


On Debian and Ubuntu using ``apt``
================================================================================
  
To uninstall |pdp| on platforms that use |apt| package manager such as Debian
or Ubuntu, complete the following steps.

Run all commands as root or via |sudo|.

1. Stop the |pdp| service.

   .. code-block:: bash

      $ sudo systemctl stop postgresql.service

#. Remove the |percona-postgresql| packages.

   .. code-block:: bash

      $ sudo apt-get remove percona-postgresql-13* percona-patroni percona-pgbackrest percona-pgbadger percona-pgbouncer
 
#. Remove configuration and data files.         

   .. code-block:: bash

      $ rm -rf /etc/postgresql/13/main

On |rhel| and |centos| using ``yum``
================================================================================

To uninstall |pdp| on platforms that use |yum| package manager such as 
|rhel| or |centos|, complete the following steps.

Run all commands as root or via |sudo|.

1. Stop the |pdp| service.

   .. code-block:: bash

      $ sudo systemctl stop postgresql-13

#. Remove the |percona-postgresql| packages

   .. code-block:: bash
 
      $ sudo yum remove percona-postgresql13* percona-pgbadger

#. Remove configuration and data files

   .. code-block:: bash

      $ rm -rf /var/lib/pgsql/13/data    



.. include:: .res/replace.txt 