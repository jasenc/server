# Server

I am currently developing my own server to host my Catalog App. This server will
use Apache, Postgres, and some other things that are yet undetermined.

## IP Address

`52.88.32.23`

## URL to Catalog App

`soon`

## Installed Software

## Reference Docs

[Remove `sudo: unable to resolve host`](http://askubuntu.com/questions/59458/error-message-when-i-run-sudo-unable-to-resolve-host-none)  
[Disable `root` ssh](http://www.howtogeek.com/howto/linux/security-tip-disable-root-ssh-login-on-linux/)  
[Change SSH Port](https://help.ubuntu.com/community/SSH/OpenSSH/Configuring)  
[fail2ban](https://www.digitalocean.com/community/tutorials/how-to-protect-ssh-with-fail2ban-on-ubuntu-14-04)  
[Cron-apt](https://help.ubuntu.com/community/AutoWeeklyUpdateHowTo)  
[UTC](http://askubuntu.com/questions/138423/how-do-i-change-my-timezone-to-utc-gmt)  
[PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04)  

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

## Authors

Jasen Carroll  
jasen.c@icloud.com  
Aug 31st, 2015
