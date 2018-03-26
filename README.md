# Summary
My own customization of [Zabbix](https://www.zabbix.com/) Docker images. These images are based on the [Alpine](https://alpinelinux.org/) flavor of the [official Zabbix images](https://hub.docker.com/u/zabbix/) using built-in [PostgreSQL](https://www.postgresql.org/) support.
Many thanks to the Zabbix team for the great job) with a fery few fixes and customizations.
For more refer to [zabbix-server-pgsql](https://hub.docker.com/r/zabbix/zabbix-server-pgsql/) docs.

The environment is made of three containers:
1. a vanilla [official PostgreSQL](https://hub.docker.com/_/postgres/) container
2. a custom Zabbix server built on top of an official [Zabbix server](https://hub.docker.com/r/zabbix/zabbix-server-pgsql/) container. This container has [curl](https://curl.haxx.se/) fixed as it appears to be broken in the parent [Alpine](https://alpinelinux.org/) image
1. a custom Zabbix web server built on top of an official [Zabbix web-nginx](https://hub.docker.com/r/zabbix/zabbix-web-nginx-pgsql/) container. At the time no customization is done on this image so it's just the same as the parent image.

# Set up
The set up is just the same described at the official [Zabbix server container](https://hub.docker.com/r/zabbix/zabbix-server-pgsql/) page, so just point to that.
