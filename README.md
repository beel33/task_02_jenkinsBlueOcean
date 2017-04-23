# Task 2 - Michael Raidel
* implement the Concourse example from task 1 in Jenkins Blue Ocean
* describe the differences and advantages/disadvantages of the CI system compared to Concourse (concerning only your implementation of the task 1 in the CI system, as a PDF)

## Install and run Jenkins with Docker

Pull the official Jenkins-Image from Docker
```shell
$ docker pull jenkins
```

Run the Image
```shell
$ docker run -p 8080:8080 -p 50000:50000 jenkins
```
>Note: This will store the workspace in /var/jenkins_home. All Jenkins data lives in there - including plugins and configuration.

If you want to make that a persistent volume (recommended):
```shell
$ docker run -p 8080:8080 -p 50000:50000 -v ~/Users/<your-home-name>:/var/jenkins_home jenkins
```
>Note: This will store the jenkins data in /your/home on the host. Ensure that /your/home is accessible by the jenkins user in container (jenkins user - uid 1000) or use -u some_other_user parameter with docker run. 

## Setting up Jenkins

When you go to localhost/port-you-mapped-jenkins-to you see the following screen:
<img src="http://blog.alexellis.io/content/images/2016/04/Screen-Shot-2016-04-30-at-21-18-05.png" alt="Unlock-Jenkins-screen" />
<br/>Image source: http://blog.alexellis.io/content/images/2016/04/Screen-Shot-2016-04-30-at-21-18-05.png


Check your console for the initial password:
<img src="https://i.stack.imgur.com/kNhMQ.png" alt="Console output" />
<br/> Image source: https://i.stack.imgur.com/kNhMQ.png

Follow the instructions and install the plugins you need.