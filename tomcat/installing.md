#### Installing Tomcat
1. Download a binary distribution of the core module: tar.gz/ Core section
2. move the unarchived distribution to /usr/local 
`sudo mkdir -p /usr/local`
`sudo mv ~/Downloads/apache-tomcat-x.x.x /usr/local`
3. create a symbolic link that we are going to use when referring to Tomcat
`sudo rm -f /Library/Tomcat`
`sudo ln -s /usr/local/apache-tomcat-x.x.x /Library/Tomcat`
4. make all scripts excutable:
`sudo chmod +x /Library/Tomcat/bin/*.sh`



