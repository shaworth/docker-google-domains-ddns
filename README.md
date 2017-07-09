docker-google-domains-ddns
============

This is a simple Docker container for running the [Google Domains](http://domains.google.com/) dynamic DNS update script on a ARM system or Raspberry Pi.

It is dragoncube's work (https://github.com/dragoncube/docker-google-domains-ddns) except created to run on a raspberry pi or ARM system.

The script runs every 5 minutes.

Usage
-----

Run:

`sudo docker run --name=google-domains-ddns -d -v /etc/localtime:/etc/localtime -v /config/dir/path:/config seanstaley/google-domains-ddns-pi`

When run for the first time, a file named google-domains-ddns.conf will be created in the config dir, and the container will exit. Edit this file, adding your username, password, and domains. Then rerun the command.

To check the status, run `docker logs google-domains-ddns`.
