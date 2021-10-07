# A docker project for Symphony

## Overview 
This is a docker project, the goal is to create a simple CRUD with symfony using by docker

## Technical information 
- php
- apache
- symphony
- SQL 

(you should use mariadb if you have a M1 apple silicon processor beacause MySQL does not work with it)
## Requirements
- docker

## How to use

1. Download the github project.

2. Open a terminal at the root of the project and use this command : 
```bash
$ docker-compose up -d
```
And when all your container is build up like this : 

```bash
Creating network "docker-symphony_dev" with the default driver
Creating php_docker_symfony ... done
Creating db_docker_symfony  ... done
Creating phpmyadmin_docker_symfony ... done
```

3. Now you can use this command to create the symfony project 
```bash
$ docker exec www_docker_symfony composer create-project symfony/website-skeleton project
```

Unfortunately it's does'nt work at this point (asking for a zip extention) :

```bash
Creating a "symfony/website-skeleton" project at "./project"
Installing symfony/website-skeleton (v5.3.99)
    Failed to download symfony/website-skeleton from dist: The zip extension and unzip/7z commands are both missing, skipping.
The php.ini used by your command-line PHP is: /usr/local/etc/php/conf.d/docker-php-ext-sodium.ini
    Now trying to download from source

                                                            
  [RuntimeException]                                        
  git was not found in your PATH, skipping source download  
                                                            

create-project [-s|--stability STABILITY] [--prefer-source] [--prefer-dist] [--prefer-install PREFER-INSTALL] [--repository REPOSITORY] [--repository-url REPOSITORY-URL] [--add-repository] [--dev] [--no-dev] [--no-custom-installers] [--no-scripts] [--no-progress] [--no-secure-http] [--keep-vcs] [--remove-vcs] [--no-install] [--ignore-platform-req IGNORE-PLATFORM-REQ] [--ignore-platform-reqs] [--ask] [--] [<package>] [<directory>] [<version>]
```
