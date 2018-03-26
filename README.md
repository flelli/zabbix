# Summary
My own customization of Zabbix Docker images. These images are based on the [Alpine](https://alpinelinux.org/) flavor of the [official Zabbix images](https://hub.docker.com/u/zabbix/) (many thanks to the Zabbix team for the great job) with a fery few fixes:
1. my [custom alert scripts](https://www.zabbix.com/documentation/3.2/manual/config/notifications/media/script) are embedded into the image file
2. [curl](https://curl.haxx.se/) (which is needed by custom scripts) seems to be broken on the base Alpine image so I just fixed it

I'm using Zabbix images built for PostgreSQL so, when using these images, the [official PostgreSQL](https://hub.docker.com/_/postgres/) docker container is assumed to be running. For more refer to [zabbix-server-pgsql](https://hub.docker.com/r/zabbix/zabbix-server-pgsql/) docs.
