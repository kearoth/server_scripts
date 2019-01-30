# server_scripts
These bash scripts are used on shared hosting webservers. To ease management.

install-site
This can be used to create a user in a shared hosting setup. 

At the moment it needs the following,
Ubuntu 16.04
Webmin
Mysql-server
Wget
Unzip

It's meant to use with nginx & php-fpm

It creates a user without shell access. 
Creates a database for the user.
Add database backup to webmin for the user. And installs a cronjob for the backup. A backup is made of your cronjobs before the new is installed.
Creates a php pool for the user. The pool uses a common settings file, which needs to exist beforehand.  

Use --wordpress as argument to download latest wordpress to the users directory. This will unzip and chown all files in the wordpress archive. Then delete the archive.

Use --restore-cron to restore the latest backup of your cronjobs.
