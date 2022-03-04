# Epitech-development-environment

A devlopment environment for epitech student based on the official **epitechcontent/epitest-docker** Docker. Work with **Docker Desktop** on **Windows**, **Mac** and **Linux**.

Don't forget to **star this repository** if you liked it !

---

# Table of content

- [Docker Desktop](#docker-desktop)
- [New project in Epitech environment](#your-project-in-epitech-marvin-environment)
- [Problems](#problems)

# Docker desktop

You first need to install **Docker Desktop** on you pc. You can follow the instructions [here](https://www.docker.com/products/docker-desktop).

---

# Your project in Epitech (Marvin) environment

## 1) Put the .docker file in your project

You need to put the **.docker** file, **from this repository**, in **your project**. A simple way to do that is to execute this script:

```bash
# Go in your project local repository
cd YourProject

# Add this repository as remote and pull from it
git remote add dockenv git@github.com:Brancieq-Paul/Epitech-development-environment.git
git pull dockenv

#Don't forget to remove the remote when it's done
git remote rm dockenv
```

## 2) Create a new Dev Environment from Docker Desktop

Create a new Dev Environment.

![Alt text](.docker/readme-images/docker_env_main_page.png?raw=true "Dev environment main page")

Use your project repository as base. The .docker will be read and the Epitech environment set.

![Alt text](.docker/readme-images/setup_env.png?raw=true "Dev environment setup")

#### An error may occur about your ssh-key. Execute the following script in your shell (work for all os) if that happen:

```bash
ssh-agent
ssh-add <path to your private ssh key>
```

You can now open this environment in Visual Studio Code  !

![Alt text](.docker/readme-images/env_set.png?raw=true "Dev environment set")

---
# Problems

## ssh-add is not working

Docker Desktop may ask you to add your ssh key before pulling your repository. Sometimes, you need to activate your ssh-agent before that (see [here](#an-error-may-occur-about-your-ssh-key-execute-the-following-script-in-your-shell-work-for-all-os-if-that-happen))

## I need to get the name of the docker container

Clic on the docker container in Docker Desktop then you can select and copy the name:

![Alt text](.docker/readme-images/clic_on_container.png?raw=true "Clic on container container")

![Alt text](.docker/readme-images/copy_name.png?raw=true "Select and copy the name")

## I need an external shell in my project directory

First, you need to get the name of the container your project is in (see [here](#i-need-to-get-the-name-of-the-docker-container)).

You can open a new terminal in the same container as your project with this docker command:

```bash
docker exec -it <mycontainer> bash
```

## I need to import files into my docker

First, you need to get the name of the container your project is in (see [here](#i-need-to-get-the-name-of-the-docker-container)).

Then, you can execute this command in your shell:
```bash
docker cp /(path to your file)  (container_id):/(to_the_place_you_want_the_file_to_be)
```

