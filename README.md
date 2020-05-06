# flask-base-app
Includes login and registration. Passwords are hashed and stored in mysql db. Users can visit their home and profile page. Users can also logout and re-login..

### Few requirements - enter these commands

pip install flask
<br>
pip install flask-mysqldb
<br>
pip install passlib

### Creating database - using MySql Workbench. You can also enter values manually.

```
CREATE DATABASE IF NOT EXISTS `userdb` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
USE `userdb`;

CREATE TABLE IF NOT EXISTS `accounts` (
	`id` int(11) NOT NULL AUTO_INCREMENT,
  	`username` varchar(20) NOT NULL,
    `email` varchar(100) NOT NULL,
  	`password` varchar(150) NOT NULL,
    PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

INSERT INTO `accounts` (`id`, `username`, `email`, `password`) VALUES (1, 'test', 'test@test.com', 'password');

select * from accounts;
```
