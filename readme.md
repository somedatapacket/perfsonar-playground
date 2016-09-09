<strong>Useful Commands:</strong>

/usr/lib/perfsonar/bin/build_json -o /var/www/html/perfsonar_config.json perfsonar_config.conf

/usr/lib/perfsonar/bin/generate_configuration

/usr/lib/perfsonar/bin/generate_gui_configuration

/etc/init.d/perfsonar-regulartesting restart

/etc/init.d/maddash-server restart

/etc/init.d/bwctl-server restart

<strong>Method for adding hosts to IP auth for esmond:</strong>

cd /usr/lib/esmond
sudo -s
source /opt/rh/python27/enable
/opt/rh/python27/root/usr/bin/virtualenv --prompt="(esmond)" .
. bin/activate
./configure_esmond

python esmond/manage.py add_user_ip_address example_user 10.0.1.1 10.0.2.0/24

<strong>Useful Documentation:</strong>

http://docs.perfsonar.net/multi_mesh_server_config.html

http://docs.perfsonar.net/multi_mesh_agent_config.html

http://docs.perfsonar.net/multi_mesh_autoconfig.html

http://docs.perfsonar.net/multi_ma_install.html#multi-ma-install-auth-ip

http://software.es.net/maddash/config_server.html

<strong>Useful Advice:</strong>

https://lists.internet2.edu/sympa/arc/perfsonar-user/2016-08/msg00038.html

https://lists.internet2.edu/sympa/arc/perfsonar-user/2015-07/msg00078.html

https://lists.internet2.edu/sympa/arc/perfsonar-user/2015-07/msg00073.html

<strong>Useful Examples:</strong>

http://ps-dashboard.es.net/

<strong>Horrible Detail:</strong>

When querying the local esmond instance, the following could be returned:
 
HTTP/1.1 301 MOVED PERMANENTLY
Date: Sat, 18 Apr 2015 01:05:19 GMT
Server: Apache/2.2.15 (CentOS)
Location: http://localhost/esmond/perfsonar/archive/
Content-Length: 0
Connection: close
Content-Type: text/html; charset=utf-8
 
Check all configs and make sure the URL is: 
http://localhost/esmond/perfsonar/archive/ 
and not http://localhost/esmond/perfsonar/archive
