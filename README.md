**This repository is obsolete. Docker images are created by [GitHub CI scripts](https://github.com/Mahmoudalziem) from a [Dockerfile](https://github.com/Mahmoudalziem/jenkins-docker/Dockerfile) that is in the main [Mahmoudalziem/jenkins-docker](https://github.com/Mahmoudalziem/jenkins-docker) repository now.**

# Containers for Azima

This repository contains a Dockerfile that allow you to install docker 

into jenkins contianer and (README) file to explain how using it.

The container are available on [dockerhub](https://hub.docker.com/r/azima/jenkins-docker/).

### Installation

docker pull azima/jenkins-docker

or simply continue to the next step.

### Running jenkins-docker & co with a console interface

To run jenkins-docker:

    docker run -it azima/jenkins-docker

### Running the notebook interfaces

To run the jenkins-docker Notebook interface (for public access, ...):

    docker run -p 8080:8080 azima/jenkins-docker

You can then connect your web browser to the printed out typically,

namely `http://localhost:8080` webbrowser will ask for 

a login and password which are stored at  `/var/jenkins_home/secrets/initialAdminPassword`.

### username and password hang server Or skip

if hang server or skip enter username and password

you can enter username `admin` and password stored 

at `/var/jenkins_home/secrets/initialAdminPassword`.

### run Docker with Jenkins

    docker run -it -d -p 8080:8080 --name jenkins -v /var/run/docker.sock:/var/run/docker.sock azima/jenkins-docker

