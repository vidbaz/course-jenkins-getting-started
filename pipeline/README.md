# pipeline notes

## ACE Editor Shortcuts

- This is the editor used for pipeline scripts as such it has shortcuts that are useful (some of the ones listed work):
  - <https://ace.c9.io/demo/keyboard_shortcuts.html>

## To get the initial password from Jenkins

On the vagrant vm execut the following
```
vagrant@buster:/vagrant$ docker exec -it vagrant_jenkins_1 cat /var/jenkins_home/secrets/initialAdminPassword
4530d54291be4d0890d83cd4fd744ea8
vagrant@buster:/vagrant$
```