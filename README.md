# Epitech-development-environment

A devlopment environment for epitech student based on the official **epitechcontent/epitest-docker** Docker. Work with **Docker Desktop** on **Windows**, **Mac** and **Linux**.

Don't forget to **star this repository** if you liked it !

---

# Table of content

- [Docker Desktop](#docker-desktop)
- [New project in Epitech environment](#your-project-in-epitech-marvin-environment)

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

![Alt text](.docker/readme-images/docker_env_main_page.png?raw=true "Dev environment")

Use your project repository as base. The .docker will be read and the Epitech environment set.

![Alt text](.docker/readme-images/setup_env.png?raw=true "Dev environment")

You can now open this environment in Visual Studio Code  !

![Alt text](.docker/readme-images/env_set.png?raw=true "Dev environment")