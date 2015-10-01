# Server

I developed my own server to host my Catalog App. This server used Apache, Postgres, and some other technologies listed below.

Note: Since graduating from Udacity's Nanodegree program the server has been shut down. However I am leaving this on my GitHub as notes to configure the next one.

## IP Address

`52.88.32.23`

## URL to Catalog App

http://ec2-52-88-32-23.us-west-2.compute.amazonaws.com

## Installed Software

Cron-apt - automatic system updating  
Apache & mod_WSGI - HTTP Server for a Flask App  
PostgreSQL - database  
Glances - Real time performance monitoring  
Monit - Automated system monitoring

## Reference Docs

[Remove `sudo: unable to resolve host`](http://askubuntu.com/questions/59458/error-message-when-i-run-sudo-unable-to-resolve-host-none)  
[Disable `root` ssh](http://www.howtogeek.com/howto/linux/security-tip-disable-root-ssh-login-on-linux/)  
[Change SSH Port](https://help.ubuntu.com/community/SSH/OpenSSH/Configuring)  
[fail2ban](https://www.digitalocean.com/community/tutorials/how-to-protect-ssh-with-fail2ban-on-ubuntu-14-04)  
[Cron-apt](https://help.ubuntu.com/community/AutoWeeklyUpdateHowTo)  
[UTC](http://askubuntu.com/questions/138423/how-do-i-change-my-timezone-to-utc-gmt)  
[PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04)  
[Apache2 could not reliably determine](http://askubuntu.com/questions/256013/could-not-reliably-determine-the-servers-fully-qualified-domain-name)  
[Monit](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-monit)  
[Monit Status](http://stackoverflow.com/questions/28187786/monit-daemon-error-connecting-to-the-monit-daemon)  
[Monit - Where is the .pid?](http://serverfault.com/questions/395413/cant-get-monit-to-work)    


## Complete Checklist

* Created new user with sudo access and SSH login.
* Disabled root user SSH and ensured disabled PasswordAuthentication.
* Update & upgrade Ubuntu packages.
* Resolved sudo host name conflict.
* Changed listening port for SSH.
* Firewall:
  * Deny all incoming requests
  * Allow all outgoing requests
  * Allow custom SSH port
  * Allow www
  * Enabled
* Installed and configured fail2ban for unsuccessful login monitoring and attack banning.
* Installed Cron-apt to automatically manage package updates.
* Server on UTC
* Installed Apache2 and Apache2 Mod_WSGI lib.
* Installed and configured PostgreSQL.
* Deployed Catalog App
* Installed Glances
* Installed Monit

## Authors

Jasen Carroll  
jasen.c@icloud.com  
Aug 31st, 2015
