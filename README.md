# osticket-helpdesk-lab
This is an Ubuntu-based virtualization lab showcasing the importance of a Tier 1 help desk workflow through osTicket.

# Overview
I built an Ubuntu-based help desk ticketing system using Ubuntu Server, Apache2 web server, MySQL, PHP, and osTicket. I used Oracle VirtualBox (Version 7.2.16) as the hypervisor, configured with NAT networking and port forwarding to enable host-to-VM connectivity. Through osTicket, I demonstrated the ticket workflow required to excel as a Tier 1 Help Desk/IT Operations Specialist, processing and resolving five tickets across all priority levels: one Low/P4, two Medium/P3, one High/P2, and one Critical/P1.

# Stack
- Ubuntu Server(24.04.4)
- Apache web server(2.4.58)
- MySQL (8.0.46.0)
- PHP 8.3.6 (cli)

# Setup Procedures
  * Within the Hypervisor of chose(Ubuntu 24.04 LTS- Noble Numbat), allocate 3162 MB to the Base Memory for sufficient storage.

  * Set adapter 1 to NAT forwarding for host-to-VM connectivity

  * Run <sudo apt update && sudo apt upgrade> within Linux OS terminal for security patch

  * Install LAMP Stack and functionalities through <sudo apt install apache2 mysql-server php php-my php-gd php-mbstring php-imap php-intl php-xml php-cli libapache2-mod-php>

  * Create the MYSQL database <sudo mysql_secure_installation> then set root password and default settings.

  * Log into MYSQL by running <sudo mysql>. Within MYSQL, create a database and user through the following command:
    CREATE DATABASE osticket;
    CREATE USER 'osTicket'@'localhost' IDENTIFIED BY 'password';
    GRANT ALL ON osticket.* TO 'osTicket'@'localhost';
    FLUSH PRIVILEGES;
    EXIT;

  * Download osTicket from official site and copy the extracted files into 'var/www/html/osticket'. Copy 'include/ost-sampleconfig.php' to 'include/ost-config.php' then set ownership to 'www-data' and permission to read+write for Owner, Group, and Others temporarily <sudo chown -R www-data:www-data /var/www/html/osticket> and <chmod 0666 include/ost-config.php>.
    (Must change privileges to read only for security purposes).

  * Set up Apache virtual host so Apache knows which folder to serve. Create a new config file <sudo nano /etc/apache2/sites-available/osticket/osticket.conf>

  * Enable the site with the required modules, then restart Apache <sudo a2ensite osticket.conf> <sudo a2enmod rewrite>
  <sudo systemctl restart apache2>

  * Find the OS IP address with <ip a> then enter the following protocol into browser: http://<OS IP address>/

  * Allow pre-installation to run then enter credentials for admin account and use previous database credentials for database section

  * Once installation is completed, turn the read+write permissions from earlier to only read for Group and Others. <sudo chmod 0644 /var/www/html/osticket/include/ost-config.php>

  * Log into staff panel and configure osTicket to liking

# Configuration

# Sample Tickets

# Lesson learned
