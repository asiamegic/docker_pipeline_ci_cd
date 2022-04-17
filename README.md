# PROJECT DOCKER

<b>Today one of the most useful and best ways to package applications are Containers because they allows us to package the application together with it dependencies and runtime in a single artifact.
</b> <br>
* <b>Briefly about the project: </b> <br>
the task is to create an application image at the CI stage, save it in the Azure container repository and at the CD stage deploy the container into two environments, staging and production using environment groups. groups of variables were also used in the project for convenience and automation

![image](https://user-images.githubusercontent.com/85096533/163695009-18cc301d-7542-4ee8-ae8f-cf7dffd3f17b.png)
This is how the structure of the project deployment stages looks like

<hr>
In order to create a docker container, first of all we need to write a DOCKERFILE in which is a template according to which an image with the most necessary will be created. in the future, this image can be used many times for convenience in our project, I will use the azure container repository.

![image](https://user-images.githubusercontent.com/85096533/163694993-257886f6-5e44-483c-afca-3e4b71a6cdc8.png)


<hr>

![image](https://user-images.githubusercontent.com/85096533/163694999-79f8c12d-49ea-4868-a3ff-4f5d7857b818.png)

In this project we will manage the code of our application using one of the most common and simple Git workflow usually called the “Feature Branch Workflow” in which branches named with the prefix “feature/” are used to work on the code independently and then the code is integrated into the master/main branch to be deployed in the target environments.
<hr>




<hr>

Sample, an example of what a group of variables looks like that can be loaded into projects
![2](https://user-images.githubusercontent.com/85096533/163695213-f946659f-bbce-43f6-ab43-79b790f8ae02.jpg)
<hr>

An example of what the working environment looks like, the advantage is that virtual machines can be easily loaded into it, with just one command. And in the future, projects can be deployed on these machines, which is very convenient as well as managing process confirmation (a kind of trigger)

![3](https://user-images.githubusercontent.com/85096533/163695253-37f6c919-ffbe-4c9b-b89d-0aececca5d36.jpg)

<hr>

Useful docker commands that will always come in handy:


after installation first steps
* systemctl start docker - starts the docker service
* systemctl enable docker - enable it
* systemctl restart docker - if necessary, you can restart the service

* systemctl status docker - shows docker activity status


* docker run hello-world - after the first installation, you can check how the demo container starts
* docker ps - shows all running containers by id , name and image

* docker images - shows all images registered in the system
* docker rm <id> - remove image by id

* docker run -d <id> - run image in background
* docker stop <id> - stop container

* docker run -it <id> /bin/sh - connect inside the active container via directories

* docker pull <id> - download the required image from remote repositories
  
  <hr>
  
  you can also see my previous project on building SI DI pipeline azure devops, by the link
  https://github.com/asiamegic/azure_devops_pipeline

<br><br>
Good luck! I was glad to see you here ;)


