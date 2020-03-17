Mautic is a marketing tool to realize the scenario of the actual market. It is backed up by power symfony framework and maintained and backed by PHP mautic community

## Github Repository
https://github.com/mautic/mautic

Mautic installation is a clean and simple process. Mautic can be set up on Xampp Windows or on Linux platform Lampp. It is a open source PHP project, it requires	php latest version 7.2 to run and database support for Mysql.

##### For installation follow the following steps added

1) Install Composer in computer
2) Install Xampp 7.2.28
3) Download Mautic and extract in xampp/htdocs
4) run composer install in xampp/htdocs/mautic using git command
5) After this, Run "http://localhost/mautic" and it shows the message that 
   "Ready to Install" and click "Next Step".
6) After that, set Database Setup to fill Database Name, Database Table Prefix, 
   Database Username and click "Next Step".
7) After that, set Administrative Tools to fill Admin Username, Admin Password, First
   Name, Last Name and Email Address and click "Next Step".
8) After that, It shows Email Configuration and click "Next".
9) Then, It shows Admin Login Page to fill Username and Password in which you have set.
10) After Admin Logged in, It will open Admin Dashboard Page.
11) And Set Permissions for Mautic:-
    find . -type d -exec chmod 755 {} \;
    find . -type f -exec chmod 644 {} \;
    chmod -R g+w app/cache/
    chmod -R g+w app/logs/
    chmod -R g+w app/config/
    chmod -R g+w media/files/
    chmod -R g+w media/images/
    chmod -R g+w translations/


## Mautic at 1Touch
Github repository for Mautic is at following url
https://github.com/1-Touch/mautic

Branches master


### Github server setup:

1)	Download and Install Gitscm on PC
https://git-scm.com/downloads

2)	Run git bash and run the following Command
	Git clone https://github.com/1-Touch/mautic.git	
	And enter username and password for your github account


### Composer Installation:

1)	Download and install composer from https://getcomposer.org/download/


OR run following command

#### Run following command 

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e0012edf3e80b6978849f5eff0d4b4e4c79ff1609dd1e613307e16318854d24ae64f26d17af3ef0bf7cfb710ca74755a') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"


### Mautic Setup

1)	Now Run 
“composer install” command into your matic copy cloned from github
2)	Run localhost and go to 

	http://localhost/mautic-installation-setup

	After this step
3)	Installation wizard will prompt you to instal the mautic locally
4)	Now as mentioned above 11 steps install and setup Mautic.



### Mautic Configuration Manual


(1)Mautic database config -app/config/local.php

(2)Mautic needs to remove cache  from app/cache ,and find log app/log  

(3)Mautic is based on Symphony and databased based on  Doctrine, a database object relational mapper (ORM)

(4)Following Table specifies

leads: contacts
lead_lists: segments
lead_lists_leads: membership of contacts within segments
lead_tags: tags
lead_tags_xrefs: associations of tags with contacts
migrations: tracks which database migrations have been applied

(5) to find all route information php app/console debug:router

(6)To call the views inside the views  $view->render('BundleName:ViewName:template.html.php', array('parameter' => 'value'));

(7)The api controller(s), should extend Mautic\ApiBundle\Controller\CommonApiController to leverage the helper methods provided and to utilize the REST views.





