#### Start and stop scripts
`/Library/Tomcat/bin/startup.sh`
`/Library/Tomcat/bin/showdown.sh`

check http://localhost:8080 !

#### Serveral ports (8005, 8080, 8009) already in use
`kill $(ps -aef | grep java | grep apache | awk '{print $2}')`
