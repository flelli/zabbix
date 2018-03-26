FROM zabbix/zabbix-server-pgsql:alpine-latest

# Copy the custom alert script and make it accessible and executable
ADD --chown=100:1000 https://raw.githubusercontent.com/flelli/slack-integrations/master/slack-zabbix-alert.sh /usr/lib/zabbix/alertscripts/
RUN chmod 755 /usr/lib/zabbix/alertscripts/slack-zabbix-alert.sh

RUN apk add --no-cache curl-dev libcurl
