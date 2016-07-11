# ansible-guacamole

Current guacamole version: 0.9.9

Current tomcat version: tomcat6 (Ubuntu), tomcat (CentOS)

### ISSUES:
----------------
- Need to find a way to configure clients and servers with shared credentials/connections
- The login page shows up but does not accept the credentials "user":"password"
- Login page does not show up on ubuntu

[From "Configuring Guacamole":](http://guacamole.incubator.apache.org/doc/gug/configuring-guacamole.html)
> Guacamole reads files from its own configuration directory by default, resorting to the classpath only when this directory cannot be found. When locating this directory, Guacamole will try, in order:

>	- The directory specified within the system property guacamole.home.
>	- The directory specified within the environment variable GUACAMOLE_HOME.
>	- The directory .guacamole, located within the home directory of the user running the servlet container.

We will use the third option, with the configuration directory `/var/lib/tomcat/.guacamole`