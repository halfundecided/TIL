### Install mySQL on Mac 

#### how to install mySQL by homebrew
1. install homebrew 
2. or check homebrew `$ brew -v`
3. install mySQL: `$ brew install mysql`
4. start mySQL server: `$ mysql.server start`
5. set password: `$ mysql_secure_installation`

#### start mySQL
- `$ mysql.server start`
- `$ mysql -u root -p`

#### set new password
`mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY 'newpassword';

 
