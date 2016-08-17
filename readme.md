Useful Commands:

/usr/lib/perfsonar/bin/build_json -o /var/www/html/perfsonar_config.json perfsonar_config.conf

/usr/lib/perfsonar/bin/generate_configuration

/usr/lib/perfsonar/bin/generate_gui_configuration

/etc/init.d/perfsonar-regulartesting restart

/etc/init.d/maddash-server restart

Useful Documentation:

http://docs.perfsonar.net/multi_mesh_server_config.html

http://docs.perfsonar.net/multi_mesh_agent_config.html

http://docs.perfsonar.net/multi_mesh_autoconfig.html

http://docs.perfsonar.net/multi_ma_install.html#multi-ma-install-auth-ip

http://software.es.net/maddash/config_server.html

Useful Advice:

https://lists.internet2.edu/sympa/arc/perfsonar-user/2016-08/msg00038.html

https://lists.internet2.edu/sympa/arc/perfsonar-user/2015-07/msg00078.html

https://lists.internet2.edu/sympa/arc/perfsonar-user/2015-07/msg00073.html

Useful Examples:

http://ps-dashboard.es.net/

Horrible Detail:

When querying the local esmond instance, the following could be returned:
 
HTTP/1.1 301 MOVED PERMANENTLY
Date: Sat, 18 Apr 2015 01:05:19 GMT
Server: Apache/2.2.15 (CentOS)
Location: http://localhost/esmond/perfsonar/archive/
Content-Length: 0
Connection: close
Content-Type: text/html; charset=utf-8
 
 
Check the script and make sure the URL is:
 
 
http://localhost/esmond/perfsonar/archive/ 

and not http://localhost/esmond/perfsonar/archive
