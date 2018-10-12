# Database_installs

##MySQL install

#### Update your system
`sudo yum update`

#### Download wget
`yum install wget`

#### Download the package
`wget https://dev.mysql.com/get/mysql80-community-release-el7-1.noarch.rpm`

#### Update system dependencies again
`sudo yum update`

#### Install the package
`sudo rpm -ivh mysql80-community-release-el7-1.noarch.rpm`

#### Install MySQL
`sudo yum install mysql-server`

#### Start MySQL
`systemctl start mysqld`

#### Check status
`systemctl status mysqld`

#### To see the daemon running
`ps -ef | grep mysqld`

#### Stop service
`systemctl stop mysqld`



#### To login to mysql
`mysql --user=root -p`
#### Enter password



#### Error loging in: ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: YES)

#### Reveal temporary password
`sudo grep 'temporary password' /var/log/mysqld.log`
#### Copy password

#### Login with temporary password
`mysql -uroot -p` 

#### Change password
`ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass5!';`

#### How install extra packages
`sudo  yum install epel-release -y`

#### Ho to install MySQL Workbench
`sudo yum install mysql-workbench -y`
