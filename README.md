vagrant-glassfish
=================
The project will create a Ubuntu based vm and provision the box with Glassfish and the necessary dependencies.  Additionally, various technologies have been installed to the stack.

Current Stack:

 * OS: Ubuntu LTS 10.2
 * Latest Open JDK
 * GlassFish V4 (installed as a service)

Vagrant
-------
Vagrant is a system used for creating and configuring virtual development environments.  To get started with this project you'll need to:

 * download [VirtualBox](https://www.virtualbox.org/wiki/Downloads) (used by Vagrant)
 * download [Vagrant](http://downloads.vagrantup.com/)

## Required manual steps after provisioning

1. change admin password of glassfish<br>
``$ sudo /opt/glassfish4/glassfish/bin/asadmin change-admin-password``
2. start glassfish<br>
``$ sudo /etc/init.d/glassfish start``
3. activate remote access / secure administration<br>
``$ sudo /opt/glassfish4/glassfish/bin/asadmin enable-secure-admin``
4. restart glassfish<br>
``$ sudo /etc/init.d/glassfish restart``

Glassfish should now serve on [http://localhost:8080/](http://localhost:8080/), admin console on [http://localhost:4848/](http://localhost:4848/)

Starting and using the Vagrant box
----------------------------------
1. Download the aforementioned software.
2. Clone this repository.
3. Run ```vagrant up``` from the cloned repo
4. In a few minutes you should have a clean GlassFish install

**Accessing the server:**

 * Glassfish console: http://localhost:4848
 * Default domain: http://localhost:8080
