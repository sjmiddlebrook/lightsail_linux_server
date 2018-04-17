# Lightsail Ubuntu Server
This project set up a ubuntu server to run the catalog item application. The server has been set up with a firewall and serves a flask application.

## IP Address
52.56.239.153

## SSH Port
2200

## URL
[http://ec2-52-56-239-153.eu-west-2.compute.amazonaws.com/](http://ec2-52-56-239-153.eu-west-2.compute.amazonaws.com/)

## Summary of software installed
* postgresql
* virtualenv
* flask
* bootstrap
* sqlalchemy

## Summary of configuration

Updated all currently installed packages with `sudo apt-get update` and `sudo apt-get upgrade`

Changed the SSH port from 22 to 2200 by updating /etc/ssh/sshd_config

Configured the Uncomplicated Firewall (UFW):
* `sudo ufw default deny incoming`
* `sudo ufw default allow incoming`
* `sudo ufw allow 2200/tcp`
* `sudo ufw allow www`
* `sudo ufw allow ntp`
* `sudo ufw enable`

Installed software required for the application

## Resources used
https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
https://wixelhq.com/blog/how-to-install-postgresql-on-ubuntu-remote-access
https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
http://docs.sqlalchemy.org/en/latest/core/engines.html
http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/

