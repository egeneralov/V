# V - easy VPS managment

V project was created to automate routine activities to automate work with the server based on Linux Debian. Can be used in lxc container. The script is a turnkey solution and provides the following functionality:

- Installing:
    - [NGINX](https://www.nginx.com)
    - [acme.sh](https://github.com/Neilpang/acme.sh) - let`s enctypt on bash
    - PHP version [5](http://php.net/archive/2017.php#id2017-01-19-3) and [7.0](http://php.net/archive/2017.php#id2017-03-16-1)
    - [MySQL](https://www.mysql.com)
    - [ProFTPD](http://www.proftpd.org)
- Provide auto setup nginx configurations for html *(static)*, php5, php7, based on my [MTA](http://github.com/egeneralov/mta/) and **will** provide proftpd installation.
- Provide functional for MTA managment **(current only basic functions)**

## Why V?

The project is the easiest solution in its category. Clear and silient installation MySQL, NGINX and acme.sh. After a clean installation, it will take ~ 200 MB in RAM.

### Warning

1. Wasn`t tested with sudo. Please, run as root. Without root privileges, it will not work - they are required to manage services and configurations.
2. All MySQL users will allow connect from all hosts. **But** you must edit mysql config to bind to port.
3. Currently will install PHP *5 and 7* together.

### Functional

- V **install**     *# perform installation*
- V **ls**      *# list of enabled and disabled sites.*
- V **add_site** domain.org       *# add site in interactive mode*
- V **del_site** domain.org       *# remove site in interactive mode*
- V **add_mail_user**       *# add mailuser to exist mail domain in interactive mode*
- V **del_mail_user**       *# add mailuser to exist mail domain in interactive mode*


## ToDo

- V **info**    - get info about site. Main [Q] - security.
- Modify PHP configurations
- (?) add PostgreSQL 3.6 support (?) (trouble in config generation)
