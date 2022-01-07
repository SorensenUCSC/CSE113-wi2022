---
title: "Homework Setup"
layout: single
classes: wide
---

This guide walks you through developing and running your homeworks using a Docker container running Ubuntu.

## Install Docker
Follow instructions [here](https://docs.docker.com/get-docker/).

## Download the container
Run the following command:
```
docker pull reeselevine/cse113:latest
```
When running, the container includes everything necessary for the homework to work correctly, namely `python3`, a C++ compiler, and `make`. It also includes two text editors, `vim` and `emacs`. If you'd like another text editor included in the image, please let us know.

Make sure that you regularly pull before running. We may update the container as the class goes on and pulling ensures you'll have the most up-to-date environment when developing.

## Development
You have two options for running code inside the docker container, depending on whether you'd like to develop inside the container using a text editor like vim, or outside the container using an IDE like Visual Studio and only use the container to verify your code will work when submitted.

## Develop outside the container
Develop normally. When you're ready to run your code inside the container, make sure you're in the top level homework directory (for example, for homework 1 your current directory should be "homework1_packet", or wherever you extracted the code to). Then, run the following command:

```
 docker run -v "$(pwd)":/assignments -it reeselevine/cse113:latest
```
Note: If you're using CMD on Windows (not Powershell), replace this command with:
```
docker run -v %cd%:/assignments -it reeselevine/cse113:latest
```
You should be running inside the container at this point. Running `ls` should list your files. At any point, to exit the container just type `exit`.

At this point, you can test that your code works correctly by following the instructions on the homework to run it.

## Develop entirely inside the container
Skip this section if you do not want to develop entirely inside the container.

### Create a volume
Docker containers do not persist their data when closed. Therefore, we need to create a volume so that any modifications we make in the container will persist across restarts. To create the volume used in this course's official image, run the following command:
```
docker volume create assignments
```

### Run the container
Run the following commands:

```
docker run -v assignments:/assignments -it reeselevine/cse113:latest
``` 

### Develop inside the container
You'll notice that the container places you in the `/assignments` directory when started. Any data saved in this directory or any of its subdirectories will persist when you exit the container. Note that data placed in any other directory will not be persisted, so make sure you're in the right place when writing your code!

Homework skeletons will be available to download using `wget`. Look for instructions on how to do this when the homework is released. The container supports vim and emacs by default, but please let us know if you'd like us to install any other text editors. Additionally, git is installed if you want to keep your work under source control.

### Getting code out of the container
While running your container, use another terminal session and find the id of the container by running `docker ps`. Copy either the container id or the name, and run `docker cp <container-id>:/assignments/<path_to_code> .`. This will copy the file (or directory), to the current directory on your machine.

Another option, if you are using git, is to push your code to a remote repository such as GitHub or GitLab.

## More details about Docker
While the details of running docker containers are unnecessary for this course, it might be helpful to understand what each part of the above commands are doing.
- `docker pull` downloads the specified container, which in this case is `reeselevine/cse113:latest`, where `reeselevine/cse113` is the image name and `latest` is the tag. Docker allows multiple tags for the same image, but for this course we will most likely only be using the default `latest` tag for images.
- `docker run` runs the specified container.
- `-v` mounts a volume from the host (your computer) to the docker container. We are mounting either the docker volume we created or the current host machine directory to the directory `/assignments` inside the container, depending on your setup above.
- `-it` gives us an interactive, terminal based session. Without this, the container would immediately exit.

