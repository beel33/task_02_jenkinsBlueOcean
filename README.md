# Task 2 - Michael Raidel
(Author: Bianca Leitner, Lukas Aichbauer)
* implement the Concourse example from task 1 in Jenkins Blue Ocean
* describe the differences and advantages/disadvantages of the CI system compared to Concourse (concerning only your implementation of the task 1 in the CI system, as a PDF)

## Install with Homebrew

```shell
$ brew update
$ brew install jenkins
$ jenkins #now visit http://localhost:8080
```

>Note: If you use a docker-image for your build make sure your host system has docker up and running


## Setting up Jenkins

When you go to localhost/port-you-mapped-jenkins-to you see the following screen:
<img src="http://blog.alexellis.io/content/images/2016/04/Screen-Shot-2016-04-30-at-21-18-05.png" alt="Unlock-Jenkins-screen" />
<br/>Image source: http://blog.alexellis.io/content/images/2016/04/Screen-Shot-2016-04-30-at-21-18-05.png


Check your console for the initial password:
<img src="https://i.stack.imgur.com/kNhMQ.png" alt="Console output" />
<br/> Image source: https://i.stack.imgur.com/kNhMQ.png

Follow the instructions and install the plugins you need.

## Install Blue Ocean

* Click on `Manage Jenkins`
* Click `Manage Plugins`
* Search for available plugins `blue ocean`
* Click `Download now and install after restart`gst

## Set up Blue Ocean

* Open Blue Ocean
* Choose between git or github
* connect to github via access token (generate @ github)
* choose organization
* choose  create pipeline from single repo
* select the desired repo
* create pipeline

## Advantages compared to Concourse CI

* The installation of Jenkins is way easier compared to Concourse.
  * installation via brew
* The configuration of the pipeline is easier compared to Concourse.
  * it is a simple UI
  * concourse uses fly-cli
* The Jenkins configuration file is easier to read compared to Concourse.

## Disadvantages compared to Concourse CI

* Jenkins Blue Ocean pipeline is less intuitive compared to Concourse CI.
  * Concourse is minimalistic, which can be a good thing sometimes
  * Jenkins Blue Ocean UI is not as satisfying as Concourse CI.
  * Jenkins without Blue Ocean has an old fashioned UI.

