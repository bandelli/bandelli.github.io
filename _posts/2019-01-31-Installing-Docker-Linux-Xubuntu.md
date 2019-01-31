---
layout: post
title: Install Docker CE on Xubuntu
author: Mariana Martin
---

Installing  the latest version of Docker CE (Community Edition) on Linux Xubuntu from their official repository

---

The intention is to show a quickly away to install the latest version of Docker CE.


# Now let's begin:


update the apt package index.

    $ sudo apt-get update

   
Install the latest version of Docker CE and containerd:

      $ sudo apt-get install docker-ce docker-ce-cli containerd.io

> **NOTE:** *If you want to remove an old version before installing:*
>>$ sudo apt-get remove docker docker-engine docker.io

    

Add Docker's GPG key:
   
    $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

Add Docker's repository:
    
    $ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"


At this time is until necessary  run the command with sudo so:

    $ sudo docker version

   
To run docker commends without sudo, add your user to the docker group:

    $ sudo usermod -aG docker $(whoami)
  

 Link of documentation: 

 [https://docs.docker.com/install/linux/docker-ce/ubuntu/](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
 
-----
