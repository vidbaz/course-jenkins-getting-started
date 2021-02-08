# pipeline notes

## ACE Editor Shortcuts

- This is the editor used for pipeline scripts as such it has shortcuts that are useful (some of the ones listed work):
  - <https://ace.c9.io/demo/keyboard_shortcuts.html>

## To get the initial password from Jenkins

On the vagrant vm execut the following
```
#Get the container name
vagrant@buster:~$ docker ps
CONTAINER ID   IMAGE                    COMMAND                  CREATED          STATUS         PORTS                               NAMES
0e1f901305a2   jenkins/jenkins:latest   "/sbin/tini -- /usr/…"   10 seconds ago   Up 7 seconds   50000/tcp, 0.0.0.0:7080->8080/tcp   vagrant_jenkins_1
387bdbac4b2e   mailhog/mailhog          "MailHog"                10 seconds ago   Up 7 seconds   1025/tcp, 0.0.0.0:7025->8025/tcp    vagrant_mails_1
vagrant@buster:~$

#Use the name below: vagrant_jenkins_1
vagrant@buster:/vagrant$ docker exec -it vagrant_jenkins_1 cat /var/jenkins_home/secrets/initialAdminPassword
4530d54291be4d0890d83cd4fd744ea8
vagrant@buster:/vagrant$
```