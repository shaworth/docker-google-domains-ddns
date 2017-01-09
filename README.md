docker-google-domains-ddns
============

This is a simple Docker container for running the [Google Domains](http://domains.google/) dynamic DNS update script. It will keep your domain.ddns.net DNS alias up-to-date as your home IP changes. 

It is heavily based on David Coppit's work (https://github.com/coppit/docker-no-ip), since Google Domains DDN API is pretty much the same as No-IP's.

The script runs every 5 minutes.

Usage
-----

Run:

`sudo docker run --name=google-domains-ddns -d -v /etc/localtime:/etc/localtime -v /config/dir/path:/config dragoncube/google-domains-ddns`

When run for the first time, a file named google-domains-ddns.conf will be created in the config dir, and the container will exit. Edit this file, adding your username, password, and domains. Then rerun the command.

To check the status, run `docker logs google-domains-ddns`.
