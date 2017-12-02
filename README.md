influxdb
========


What is does this role do?
--------------------------

This role installs and configures an influxdb server.  Because the
influxdb support in ansible is rather thin as of the time of writing
the server is installed without substantial security measures in place
and instead the firewall is relied on to limit access.  This is a
known limitation of the role.

Meta
----

Files Managed:
  * /etc/influxdb/influxdb.conf

Defaults Provided:
  * influxdb.reporting_disabled: true

Variables Required:
  * None

Optional Variables:
  * influxdb.reporting_disabled: report statistics to the influxdb mothership
  * influxdb.remote_sources: list of hosts that will push metrics to this server

Files Required:
  * None

Optional Files:
  * None

Conflicting Roles:
  * None

Depends On:
  * network
