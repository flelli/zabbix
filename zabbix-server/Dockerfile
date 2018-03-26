FROM zabbix/zabbix-server-pgsql:alpine-latest

# Copy the custom alert script and make it accessible and executable
#ADD https://github.com/flelli/slack-integrations/raw/master/slack-zabbix-alert.sh /usr/lib/zabbix/alertscripts/
#RUN /bin/bash -c 'chown 100:1000 /usr/lib/zabbix/alertscripts/slack-zabbix-alert.sh; chmod 755 /usr/lib/zabbix/alertscripts/slack-zabbix-alert.sh'

ADD https://github.com/flelli/slack-integrations/raw/master/slack-zabbix-alert.sh /tmp/
RUN chown 100:1000 /tmp/slack-zabbix-alert.sh && chmod 755 /tmp/slack-zabbix-alert.sh && mv /tmp/slack-zabbix-alert.sh /usr/lib/zabbix/alertscripts/

RUN apk add --no-cache curl curl-dev libcurl
