# Cloudlist Server

In order for XBSLink to be usable, a cloudlist must be specified. Without it, you have to specify the host's IP and PORT, which can be troublesome.

Fortunately, you can easily host a cloud list.

## Installation (Linux)

This tutorial has been done using a Debian-Based distribution (Debian, Ubuntu, Linux Mint, ...). 

0) In order to make sure others will be able to join your service, open your Web Port (80 TCP)!

1) Install the required services:
apt-get update && apt-get upgrade -y && apt-get install apache2 php5 php-mysql -y

2a) Install MariaDB (more optimised than MySQL)
Please refer yourself to this link in order to install it:
https://downloads.mariadb.org/mariadb/repositories/#mirror=layerjet-fr

2b) Install MySQL
apt-get install mysql-server -y

Whatever the step taken, don't forget to take note of the account, password, and database you'll use.

3) Open index.php, and modify the following lines with the informations provided:
define('DB_SERVER', 	'INSERT_SERVER_NAME'); // Set it to localhost, or your remote SQL Database (if having any)
define('DB_NAME', 		'INSERT_DB_NAME');    // The name of the Database
define('DB_USERNAME', 	'INSERT_USERNAME'); // Your account's Name
define('DB_PASSWORD', 	'INSERT_PASSWORD'); // Your account's Password.

4) Put the file into /var/www .

5) Now, go to your web browser, and open the link (to make sure the database is installed).

6) Test XBSLink with the link, and it should work.
