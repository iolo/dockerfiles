# docker image for tomcat8 with oracle java8 

## getting started

```
$ docker run --name=tomcat [-it] [-d] -p 18080:8080 -p 18009:8009 -v /path/to/webapps/on/host:/tomcat/webapps:ro iolo/tomcat:latest
```

> NOTE: with boot2docker,
> You should notice `/Users` is shared between VirtualBox Host(Windows or Mac OS X) and VirtualBox Guest(Linux; Docker Host).

## directory layout

```
/tomcat
      /webapps -- to deploy webapps
      /logs
      /work
      /temp
      /bin
          /setenv.sh -- to override environment variables and java system properties
      /conf
          /server.xml -- to override tomcat server configurations
          /Catalina
```
